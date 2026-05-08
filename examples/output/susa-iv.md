# VC fund evaluation primer — Susa Ventures IV & Susa Opportunities II

> **Note.** This is a verbatim run of the v1 Skill against the Susa deck (Q1 2021). Source deck: [Google Drive link](https://drive.google.com/file/d/1WZnQYPIVY6L_Vqe1-1eJBMdv0dLpQX2q/view).

## 1. Can we trust this team?

Three co-founder GPs (Byers, Berman, Polovets) have been together since 2013 across three seed funds plus one opportunity fund. The deck attaches each GP to specific named investments — Byers to Robinhood and Stord, Berman to Flexport and Viz.ai, Polovets to Scalyr and Stedi — which is useful provenance and rare in pitch decks. Team has expanded with Partner Courtney Buie Lipkin (ex-First Round) and a 13-person Venture Fellows program launched September 2020. Founder NPS of 96 is cited but methodology and sample size are not disclosed.

The deck says nothing about mistakes from prior funds. The Susa I timeline (slide 21) shows clear failures faded into the background — Periscope, Vurb, Namo Media, Standard Treasury, Move Loot — with no commentary on what was learned, what changed, or how it informed Susa II/III decisions. The pitch explicitly states Susa IV will follow "the same strategy as Susa I, II, & III" — which reads either as confidence or as absence of evolution.

GP commitment to the new funds is not stated. No dollar figure or percentage for skin-in-the-game, no management fee, no carry structure. The summary terms page lists target size and term length but skips alignment economics entirely. This is a meaningful omission given the 1:2 stapled commitment ask.

## 2. How does their strategy work?

The strategy is a barbell: $100M Susa IV does seeds (40 companies, $1.25M average check, 1:1 reserves), and $200M Susa Opp II leads or co-leads Series B/C in best performers plus pro-rata at Series A (15 companies, $10M average check, 25% reserves). The seed approach is well-established across three prior funds. The opportunity fund is a 4x scale-up from Opp Fund I ($50M, 2019) into a strategy where the discretionary track record is two years young; prior growth-stage signal is from SPVs.

Skill signal is the load-bearing problem here. Every track-record metric in the deck — MOIC, TVPI, DPI, Gross IRR, Net IRR, called capital — is redacted ("#.##x", "##%"). The "Top 1%" Susa I claim is unaccompanied by the underlying number, and the footnote reveals the headline figure relies on secondary market prices for Robinhood and Flexport, which mark to private liquidity rather than realised cash. The back-tested Opp Fund analysis on slides 25-26 is selection-on-the-dependent-variable: it picks the Series Bs that happened to be led by top firms.

The 70% Series A graduation rate is real but is calculated only on Susa I (2013 vintage). The same metric is not shown for Susa II/III, where the cohort is younger and the rate is plausibly lower.

## 3. What are the risks, and can we live with them?

The biggest concentration risk is a single position. The slide 22 Pareto chart for Susa I shows what looks like one investment driving most fair value — almost certainly Robinhood at secondary prices. Susa II's distribution (slide 23) is flatter but the redacted scales make it impossible to judge. The "$19B+ aggregate enterprise value" headline on slide 17 is dominated by the same one or two outliers.

Strategy novelty risk on Opp II is genuine. LPs are being asked to back a $200M discretionary growth vehicle on the basis of a $50M predecessor that closed only two years ago and is mostly unrealised, plus prior SPVs whose returns are also redacted. The check size jumps from $1.25M to $10M, the decision template differs, and Opp II reserves (25%) are thinner than Susa IV's 50% — yet growth-stage down-rounds are precisely where reserves matter most.

Conflict of interest between the two funds — allocation logic, who prices the pro-rata, what happens when an Opp II Series B lead would be in a Susa IV company — is not addressed. Key-person succession is not addressed. The 1:2 stapled commitment compounds these risks rather than isolating them.

## To ask on the call

1. **gp_alignment**: What is each GP's dollar commitment to Susa IV and Opp II, as both an absolute amount and a percentage of fund size?
2. **skill_signal**: Walk us through realised DPI and net IRR for Susa I, II, III, and Opp I separately — not blended, not at secondary prices.
3. **conflict_of_interest**: How are allocation, pricing, and lead-investor decisions handled when both Susa IV and Opp II want exposure to the same company?
4. **response_to_failure**: What were the three biggest investment mistakes across Funds I-III, and what specifically changes in IV as a result?
5. **market_or_team_novelty**: Opp II is 4x Opp I. What deployment evidence shows the team can lead $10M Series B/C checks at scale, not only follow on?
6. **key_person_concentration**: If Byers, Berman, or Polovets leaves, what is the documented succession plan and how does the key-person clause trigger?
7. **portfolio_management**: At 25% reserves across 15 deals, how do you protect against a down-round in the second-best company in Opp II?
8. **metrics_interpretation**: The "Top 1%" Susa I claim depends on Robinhood/Flexport secondary prices — what is the comparable percentile using last-priced primary rounds only?
9. **end_to_end_process**: Walk us through a representative Susa III deal end-to-end — sourcing channel, IC dynamics, post-investment support, exit posture.
10. **founder_relationships**: Can you provide three founder references, including at least one whose company materially underperformed expectations?

(2 additional minor gaps not shown.)

---

## Structured output

```json
{
  "fund_name": "Susa Ventures IV & Susa Opportunities II",
  "as_of_date": "Q1 2021 (deck dated; data unaudited as of 2/28/2021)",
  "framework": {
    "team_trust": {
      "response_to_failure": {
        "value": "not present — deck shows failed Susa I investments visually faded but contains no narrative on mistakes or lessons",
        "source": "deck p.21 timeline (failures shown without commentary)",
        "confidence": "not_assessable",
        "what_would_change_the_call": "Ask for the three biggest investment mistakes across I-III, named, with what each GP would do differently."
      },
      "process_improvement": {
        "value": "not present — deck explicitly states Susa IV follows 'the same strategy as Susa I, II, & III'",
        "source": "deck p.15",
        "confidence": "low",
        "what_would_change_the_call": "Ask for one concrete process change between Fund II and Fund III, and one planned for IV."
      },
      "consistency": {
        "value": "not present",
        "source": "not present",
        "confidence": "not_assessable",
        "what_would_change_the_call": "On call, probe the same investment-decision question across two GPs separately and compare."
      },
      "founder_relationships": {
        "value": "Founder NPS reported as 96; bootcamps, family dinners, and Mountain Tech Summit cited; methodology and sample not disclosed",
        "source": "deck p.7",
        "confidence": "low",
        "what_would_change_the_call": "Ask for three founder references including one whose company materially underperformed."
      },
      "gp_alignment": {
        "value": "not present — no GP commitment percentage, dollar amount, fee structure, or carry mentioned",
        "source": "deck p.31 'Summary Terms' lists only target size and term",
        "confidence": "not_assessable",
        "what_would_change_the_call": "Ask each GP's dollar commitment to IV and Opp II, both absolute and as % of fund size."
      }
    },
    "strategy_mechanics": {
      "plausibility": {
        "value": "Barbell: Susa IV = 40 seeds at $1.25M avg with 1:1 reserves; Opp II = 15 Series B/C leads at $10M avg with 25% reserves; 1:2 stapled commitment between funds",
        "source": "deck p.11, p.15, p.24, p.31",
        "confidence": "high",
        "what_would_change_the_call": "Ask how the four-person investment team manages 40 new seed deals plus 15 growth-stage leads plus support for ~115 existing portfolio companies."
      },
      "end_to_end_process": {
        "value": "Sourcing partly via Venture Fellows program; portfolio support detailed (bootcamps, dinners, swag); IC process and exit strategy not described",
        "source": "deck p.6-7",
        "confidence": "low",
        "what_would_change_the_call": "Walk us through a representative Susa III deal end-to-end — sourcing channel, IC dynamics, support, exit posture."
      },
      "portfolio_management": {
        "value": "Susa IV: 40 companies, $1.25M avg check, 1:1 reserves. Opp II: 15 companies, $10M avg check, 25% reserves. Opp I 2019 deployed across 13+ named investments",
        "source": "deck p.15, p.24, p.29",
        "confidence": "high",
        "what_would_change_the_call": "Ask how 25% reserves on Opp II survive a down-round in the second-best company; ask deployment pace and recycling policy."
      },
      "skill_signal": {
        "value": "All track-record metrics (MOIC, TVPI, DPI, Gross/Net IRR) redacted as '#.##x' and '##%'; 'Top 1%' Susa I claim shown without numerator; back-tested Opp Fund analysis suffers selection bias (uses Series Bs led by top firms in hindsight)",
        "source": "deck p.10, p.12-14, p.25-26",
        "confidence": "low",
        "what_would_change_the_call": "Realised DPI and net IRR for each fund separately, not blended and not at secondary prices. The 'Top 1%' claim relies on Robinhood/Flexport secondary marks per slide 10 footnote — what is the percentile using last-priced primary rounds only?"
      },
      "metrics_interpretation": {
        "value": "Power-law analysis on slides 22-23 (20% drives 90%) is internally honest; but 70% Series A rate is presented from Susa I (2013) only, not Susa II/III, where the rate is plausibly lower; 2.5x follow-on rate cited against averaged peer benchmark",
        "source": "deck p.18, p.21-23",
        "confidence": "med",
        "what_would_change_the_call": "Ask for the same Series A graduation rate and follow-on rate computed for Susa II and Susa III separately, with cohort-age controls."
      }
    },
    "risk_recognition": {
      "key_person_concentration": {
        "value": "not present — three co-founder GPs plus one Partner; no succession plan or key-person clause discussed",
        "source": "deck p.4-5, p.31",
        "confidence": "not_assessable",
        "what_would_change_the_call": "If any of Byers/Berman/Polovets leaves, what is the documented succession plan and how does the key-person clause trigger?"
      },
      "market_or_team_novelty": {
        "value": "Susa IV strategy is well-rehearsed; Susa Opp II is a 4x scale-up from $50M Opp I (2019, mostly unrealised) into discretionary Series B/C leads where the team's track record is largely SPV-based",
        "source": "deck p.10, p.24, p.29",
        "confidence": "med",
        "what_would_change_the_call": "What deployment evidence shows the team can lead $10M Series B/C checks at scale, beyond pro-rata participation?"
      },
      "conflict_of_interest": {
        "value": "not present — no policy described for cross-fund allocation between Susa IV (seed + pro-rata) and Opp II (Series A pro-rata + B/C leads), where overlap is structurally guaranteed",
        "source": "not present",
        "confidence": "not_assessable",
        "what_would_change_the_call": "How are allocation, pricing, and lead decisions handled when both funds want exposure to the same company; who decides and is it disclosed to LPs?"
      },
      "risk_acceptance": {
        "value": "not present",
        "source": "not present",
        "confidence": "not_assessable",
        "what_would_change_the_call": "On call, probe which risks the GPs accept knowingly versus mitigate, especially around concentration in single positions."
      }
    }
  },
  "consistency_flags": [
    {
      "claim": "Portfolio company count",
      "sources": ["deck p.17 ('115+')", "deck p.21 timeline (visual count appears higher)"],
      "discrepancy": "Slide 17 states 115+ Susa-backed companies; the timeline on slide 21 visually lists ~130+ logos. Worth confirming whether the gap is fund-of-fund/SPV scope or undercounted headline."
    },
    {
      "claim": "Susa I performance basis",
      "sources": ["deck p.10 'Top 1%' claim", "deck p.10 footnote on secondary pricing"],
      "discrepancy": "Headline 'Top 1%' percentile is shown in the same panel where the footnote says the figure relies on Robinhood/Flexport secondary market prices. The percentile claim and the pricing basis should be reconciled — secondary marks are not standard benchmarking inputs."
    }
  ],
  "gap_list": [
    {"sub_criterion": "gp_alignment", "question": "What is each GP's dollar commitment to Susa IV and Opp II, in absolute terms and as a percentage of fund size?", "rank": 1},
    {"sub_criterion": "skill_signal", "question": "Walk us through realised DPI and net IRR for Susa I, II, III, and Opp I separately — not blended, not at secondary prices.", "rank": 2},
    {"sub_criterion": "conflict_of_interest", "question": "How are allocation, pricing, and lead-investor decisions handled when both Susa IV and Opp II want exposure to the same company?", "rank": 3},
    {"sub_criterion": "response_to_failure", "question": "What were the three biggest investment mistakes across Funds I-III, and what specifically changes in IV as a result?", "rank": 4},
    {"sub_criterion": "market_or_team_novelty", "question": "Opp II is 4x Opp I. What deployment evidence shows the team can lead $10M Series B/C checks at scale, not only follow on?", "rank": 5},
    {"sub_criterion": "key_person_concentration", "question": "If Byers, Berman, or Polovets leaves, what is the documented succession plan and how does the key-person clause trigger?", "rank": 6},
    {"sub_criterion": "portfolio_management", "question": "At 25% reserves across 15 deals, how do you protect against a down-round in the second-best company in Opp II?", "rank": 7},
    {"sub_criterion": "metrics_interpretation", "question": "The 'Top 1%' Susa I claim depends on Robinhood/Flexport secondary prices — what is the comparable percentile using last-priced primary rounds only?", "rank": 8},
    {"sub_criterion": "end_to_end_process", "question": "Walk us through a representative Susa III deal end-to-end — sourcing channel, IC dynamics, post-investment support, exit posture.", "rank": 9},
    {"sub_criterion": "founder_relationships", "question": "Can you provide three founder references, including at least one whose company materially underperformed expectations?", "rank": 10}
  ]
}
```
