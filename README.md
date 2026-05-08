# VC fund evaluation primer

A Claude Skill that produces a confidence-tagged pre-call primer for VC fund evaluation. Single LLM call, deterministic, no external tools. Inputs: a fund deck PDF (required), an LP letter or AGM notes (optional), a paste of fund website content (optional). Output: a ~600-word self-citing memo plus a numbered "to ask on the call" gap list, with a structured JSON appendix for downstream systems.

The Skill is organised around a 3-question × 14-sub-criterion VC evaluation framework. Original credit: [How we evaluate VC funds at Titanium Birch](https://www.titaniumbirch.com/blog/how-we-evaluate-vc-funds-at-titanium-birch) by Valerie Tang (2026-04-17).

## What this is

A Claude Skill, not an agent. Inputs go in attached or pasted; a markdown memo plus a JSON appendix come out.

The Skill maps inputs to the framework's 14 sub-criteria. Each field carries a `value`, `source` (input + location), `confidence` (low/med/high/not_assessable), and a `what_would_change_the_call` counterfactual. The output ends with a numbered "to ask on the call" gap list pulled from the missing and low-confidence fields.

The Sanity-check pass (Step 4 of `SKILL.md`) adds two moves on top of straight extraction: cross-input consistency (flag claims that disagree across deck / LP letter / website) and metric stress-test (for each quantitative claim, generate one alternative interpretation the metric could mask). Both are pure reasoning, no tools needed.

## Memo vs JSON — what each is for

The Skill's response has two halves. They serve different audiences and earn their place separately.

| | Memo (top half) | JSON (bottom half) |
|---|---|---|
| Audience | The analyst, 5–10 min before the GP call | The future agent layer / record system; deep audits beyond what's inline |
| Optimised for | Skim-readability and decision-relevance | Field completeness and machine-parseability |
| Coverage | Curated — most decision-relevant ~70%, plus a top-10 gap list | All 14 sub-criteria, including the 4 conversational ones marked `"not present"` |
| Distinct content | Inline-cited prose, narrative grouping, prioritised gap list | Counterfactuals for fields beyond the top-10 gap list, structured `consistency_flags`, confidence as discrete labels |

The memo is **self-citing** — every factual claim from the inputs carries an inline `(deck p.X)` citation, and confidence is encoded in the prose itself (declarative for high-confidence, hedged for med/low). A reader can verify almost any memo claim without dropping into JSON.

The JSON's job is what the memo deliberately doesn't carry: the long tail of counterfactuals, the not-yet-decision-relevant `"not present"` fields, the structured consistency-flags array, and the API surface for the agent layer when it ships.

The output makes the boundary explicit: a reading-guide blockquote separates memo from JSON, and the JSON section header — *"Audit JSON — page citations + per-field confidence"* — names its role.

## Deck staleness — what the Skill does and doesn't do

VC pitch decks circulate for years after their `as_of_date`. The Skill detects this and is honest about it.

- **What the Skill does.** Step 1 extracts `as_of_date` from cover/headers/footers/footnotes. If the date is more than 12 months in the past, the JSON gets a top-level `staleness_warning` field, and the time-sensitive sub-criteria (`skill_signal`, `metrics_interpretation`, `portfolio_management`, `market_or_team_novelty`) get an explicit "verify against current public sources" line appended to their `what_would_change_the_call`.
- **What the Skill doesn't do.** Verify anything. The Skill has no web access. It flags what needs verifying; closing the gap is the agent layer's job (see [`roadmap.md`](roadmap.md) — the GP track-record cross-check tool).

This split is deliberate. A pure-Skill artifact stays deterministic and inspectable. Adding tools to verify time-sensitive claims pushes the artifact into agent territory, which the roadmap treats as a NEXT-tier addition.

## How to invoke

1. Zip this repo with the repo folder as the ZIP root — `SKILL.md` should sit at `<zip-root>/SKILL.md`, **not** `<zip-root>/<some-folder>/SKILL.md`. The most common installation error is one level of nesting.
2. Upload the ZIP via Claude Desktop (Settings → Skills → Add custom skill).
3. Open a new conversation, attach the fund deck PDF, optionally attach an LP letter, optionally paste website content. Invoke the Skill.
4. Output: memo + gap list + JSON in a single response.

The Skill loads to `~/.claude/skills/vc-fund-evaluation-primer/SKILL.md`. `framework.md` is referenced at runtime as a bundled context file and must sit alongside `SKILL.md` in the same folder.

## Examples

### susa-iv — Susa Ventures IV / Susa Opportunities II (Q1 2021)

**Source deck:** [Google Drive link](https://drive.google.com/file/d/1WZnQYPIVY6L_Vqe1-1eJBMdv0dLpQX2q/view)

**Output:** [`examples/output/susa-iv.md`](examples/output/susa-iv.md)

**Why this fund.** Susa was a deliberately stale pick — the deck is dated Q1 2021, so it tests whether the Skill's deck-only reasoning holds up against a 5-year-old document where the world has moved (Robinhood IPO'd July 2021; Flexport restructured 2022–2023). The result is the strongest validation of the Skill's design philosophy: catch what's stale, flag it for verification, don't pretend to verify.

**What the run validates.**

- **Footnote-level reading.** Caught the slide-10 footnote that the "Top 1%" Susa I claim relies on Robinhood / Flexport secondary market prices.
- **Redacted-metrics handling.** Flagged that every track-record metric (MOIC, TVPI, DPI, Gross / Net IRR) is redacted and demanded the unredacted set per fund separately.
- **Pure-reasoning passes.** Identified the back-tested Opp-Fund analysis on slides 25–26 as selection-on-the-dependent-variable — no external data needed.
- **Cross-input consistency.** The `consistency_flags` pass surfaced the slide-17-vs-slide-21 portfolio-count mismatch.
- **Conversational sub-criteria.** Marked `consistency`, `risk_acceptance`, and parts of `founder_relationships` as `"not present"` and routed them to the gap list as call topics.

**What it explicitly defers to the agent layer.**

- Verification of named portfolio companies' current state (Robinhood / Flexport / Stord / Viz.ai outcomes).
- Realised vs marked-up returns reconciliation against public exit data.
- Post-deck restructuring or regulatory events.

These belong in the NEXT tier — see [`roadmap.md`](roadmap.md).

## Roadmap

The Skill is the deterministic core. [`roadmap.md`](roadmap.md) lays out the system view in three tiers:

- **NOW** — the Skill (this repo).
- **NEXT** — agent layer wrapping the Skill: 3 tools (website fetcher, portfolio-company resolver, GP track-record cross-check) + write-confirmation gate.
- **LATER** — corrections-back-to-rubric loop, integration edges (Arch, SoftLedger, dbt), adjacent artifacts (post-call retrospective Skill, public-equity primer).

Includes a Mermaid system diagram.

## Files

- `SKILL.md` — system prompt with the six steps, schema spec, output format, guardrails. Required by the Skill loader.
- `framework.md` — the 14-sub-criterion reference, used as the keys for the structured output. Loaded by `SKILL.md` at runtime.
- `roadmap.md` — system view with Mermaid diagram and NOW / NEXT / LATER tier bullets.
- `examples/output/susa-iv.md` — verbatim Skill output against a real (5-year-stale) fund deck.
- `README.md` — this file.

## Out of scope

- PPTX input — convert to PDF first.
- Multi-fund batch / comparison mode — single-fund happy path only.
- Track-record verification, portfolio-company status checks, GP exit databases — agent-layer work.
- Founder reference calls, post-decision retrospectives — judgment workflows, not the Skill's job.
- No web augmentation, no live verification of deck claims. The Skill flags time-sensitive findings for verification but does not perform it.
