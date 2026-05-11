# VC fund evaluation primer — Precursor Ventures Fund III

> **Note.** This is a verbatim run of the v3 Skill against the Precursor deck (Q3 2020). Source deck: [Google Drive link](https://drive.google.com/file/d/1Jhpbz95IfFE8iyVMS7oAvIYC0OtBtVlE/view).

## 1. Can we trust this team?

Charles Hudson is the sole GP, with a credible background: Stanford BA and MBA, operating stints at Google and IronPort Systems, two founded companies, and prior investing at Uncork Capital (SoftTech VC) and In-Q-Tel (deck p.4). The team includes Sydney Thomas (Duke/Berkeley-Haas, operator at Naya Health, Kimberly Clark) and Ayanna Kerrison (Baruch College, finance background at Credit Suisse/BMO/Merrill Lynch) (deck p.5), though their investment decision-making authority is unclear.

The fund progression from Fund I ($15.3M, 83 companies) to Fund II ($31M, 95 companies) to Fund III ($40M, 75 companies) shows iterative learning (deck p.35). Specific process changes are documented: Fund I prioritized access over ownership at 1–3% targets; Fund II increased to 4–6% and introduced proactive follow-on capital; Fund III adds a dedicated reserves fund replacing SPVs and shifts to 75% pre-seed weighting (deck p.35). These are concrete changes, though the deck does not name specific mistakes that prompted them — they're framed as improvements, not corrections.

GP commitment is not disclosed anywhere in the deck. The fund's deal sourcing is well-documented — 43% from other VCs, 17% from portfolio founders, 15% from friends (deck p.32) — which signals strong network positioning. However, nearly all quantitative performance data (MOIC, IRR, company counts per stage, exits) is redacted across slides 11–15, 18, 20, 22–23, and 33, making independent trust calibration impossible from documents alone.

## 2. How does their strategy work?

The thesis is straightforward: lead pre-seed rounds of ≤$1M where most institutional investors won't go — companies with low data on both business metrics and founder track record (deck p.3). Fund III targets 75 companies at 20–25 per year, with $250K initial checks for pre-seed and $400K for seed, aiming to deploy $500–750K total in the best companies before Series A (deck p.36). The math works: ~75 × $250K initial ≈ $18.75M, with the remainder for follow-ons and fees, plausible for a $40M fund.

The co-investor network is a genuine asset. At seed, the top co-investors include Y Combinator (13 companies), Bloomberg Beta (9), Homebrew, Founders Fund, and First Round Capital (5 each) (deck p.24). At Series A+, Y Combinator (9), Andreessen Horowitz (4), Founders Fund (3), plus Sequoia, Kleiner Perkins, and Benchmark each appearing (deck p.25). This suggests Precursor portfolio companies attract strong downstream capital. Standout Fund I names include The Athletic (Series D), Superhuman (Series B), Clearbanc (Series B), Juniper Square (Series C), and Carrot Fertility (Series B) (deck p.14).

However, the deck's redaction of all performance metrics is a significant limitation. The sector mix is consistent across funds: B2B Software (~30%), Consumer (23–34%), Digital Health (10%) (deck p.28). Geographic concentration remains high in the Bay Area (69% Fund I, 58% Fund II) (deck p.29), though Fund II shows diversification. The founder diversity data is notable — Fund II reached 45% female founders (deck p.30) — but the link between diversity focus and returns is not drawn.

## 3. What are the risks, and can we live with them?

Key-person risk is the dominant concern. Hudson is the sole named decision-maker; the other team members appear in operator/support roles with no stated carry structure or succession plan (deck pp.4–5). A $40M fund with 75 companies and one GP raises workload questions — that's roughly 25 active relationships per team member if all three are involved, but the investment authority distribution is unclear.

The pre-seed category itself is a structural risk the deck partially acknowledges by framing it as an opportunity (deck p.6). Pre-seed is where institutional seed was in 2007–2010, and the deck argues the cycle is repeating. But Fund III's 75% pre-seed weighting (up from 60–65% in earlier funds) increases exposure to the least data-rich, highest-failure-rate segment without disclosing loss rates.

Conflict-of-interest policies are absent. The transition from SPVs (Fund I/II) to a reserves fund (Fund III) is positive for alignment, but the deck does not discuss how follow-on decisions are made or whether LP co-investment rights exist. The deck is dated Q3 2020 — roughly 68 months stale — meaning all portfolio status claims (company stages, co-investor lists, team composition) require fresh verification.

## To ask on the call

1. **[metrics_interpretation]**: What are Fund I and Fund II gross/net MOIC and DPI as of today, and how concentrated are returns across the top 3–5 positions?
2. **[gp_alignment]**: What is the GP's dollar commitment to Fund III, and what is the carry structure across the team?
3. **[key_person_concentration]**: If Hudson were unable to continue, what is the operational and legal succession plan for the fund?
4. **[skill_signal]**: What is the loss ratio across Fund I and II, and how many of the standout companies (Athletic, Superhuman, Clearbanc) have produced realized DPI?
5. **[response_to_failure]**: Can you walk through a specific investment that didn't work and what you changed as a result?
6. **[conflict_of_interest]**: How are follow-on allocation decisions made between the main fund and the reserves fund, and do LPs have co-investment rights?
7. **[founder_relationships]**: Can you connect us with 2–3 founders whose companies struggled — not the winners — for reference calls?
8. **[portfolio_management]**: With 75 companies and one GP, what does the weekly time allocation look like per company, and how do you triage?
9. **[consistency]**: The deck is ~68 months old — what has changed in strategy, team composition, or portfolio status since Q3 2020?
10. **[risk_acceptance]**: What is the realistic downside scenario for Fund III, and what loss rate are you underwriting?

---

> **Reading guide.** Memo above = read top-to-bottom in 5–10 min for the call. JSON below = field-level audit trail (page citations, confidence per field, all 14 sub-criteria). Consult only to audit a specific claim or feed a downstream system.

## Audit JSON — page citations + per-field confidence

```json
{
  "fund_name": "Precursor Ventures Fund III",
  "as_of_date": "Q3 2020",
  "staleness_warning": "deck dated Q3 2020; ~68 months stale",
  "framework": {
    "team_trust": {
      "response_to_failure": {
        "value": "No explicit failures named. Fund progression shows iterative changes (access→ownership, SPV→reserves, increased pre-seed weighting) but framed as improvements, not corrections.",
        "source": "deck p.10, p.17, p.35",
        "confidence": "low",
        "what_would_change_the_call": "Ask Hudson to describe a specific investment that failed and what concrete process change resulted. Deck is 68 months old — verify against current public sources."
      },
      "process_improvement": {
        "value": "Fund I: $150K checks, 1-3% ownership, access-first, SPV follow-on. Fund II: $250K checks, 4-6% ownership, proactive follow-on. Fund III: $250K/$400K checks, reserves fund replacing SPVs, 75% pre-seed target.",
        "source": "deck p.35",
        "confidence": "med",
        "what_would_change_the_call": "What specifically went wrong with the SPV model that led to the reserves fund change? Did any SPV-based follow-ons underperform?"
      },
      "consistency": {
        "value": "not present",
        "source": "not present",
        "confidence": "not_assessable",
        "what_would_change_the_call": "Meet with Thomas and Kerrison separately to assess coherence of investment philosophy and decision-making process."
      },
      "founder_relationships": {
        "value": "Claims 300+ founder community, active Slack with ~233 messages in June 2020, hosted events including Female Founder Happy Hours and category dinners.",
        "source": "deck p.8, p.38, p.39",
        "confidence": "low",
        "what_would_change_the_call": "Request references from 2-3 founders whose companies struggled or shut down, not showcase portfolio companies."
      },
      "gp_alignment": {
        "value": "not present",
        "source": "not present",
        "confidence": "not_assessable",
        "what_would_change_the_call": "What is Hudson's personal dollar commitment to Fund III? What is the carry split across the team?"
      }
    },
    "strategy_mechanics": {
      "plausibility": {
        "value": "$40M fund, 75 companies, $250K pre-seed / $400K seed initial checks, $500-750K total per best companies pre-Series A. 20-25 companies/year over ~3 year deployment. Math is plausible.",
        "source": "deck p.35, p.36",
        "confidence": "med",
        "what_would_change_the_call": "With 75 companies and one GP decision-maker, how much diligence time per company? How many deals do you pass on per closed deal?"
      },
      "end_to_end_process": {
        "value": "Sourcing: 43% other VCs, 17% portfolio founders, 15% friends, 13% LPs, 3% accelerators. Support: hiring vetting, fundraising coaching, investor intros, on-demand advisory, founder Slack community. Exit strategy not discussed.",
        "source": "deck p.32, p.37, p.38",
        "confidence": "med",
        "what_would_change_the_call": "What is your exit strategy philosophy? Do you sell secondaries, hold through IPO, or distribute shares? What triggers a decision to write down vs. continue supporting?"
      },
      "portfolio_management": {
        "value": "Fund III introduces reserves fund (replacing SPVs). 75% pre-seed / 25% seed target. Proactive follow-on capital outside of rounds. Consistent 20-25 companies per year pacing.",
        "source": "deck p.35, p.36",
        "confidence": "med",
        "what_would_change_the_call": "What percentage of Fund III is allocated to reserves vs. initial deployments? What triggers a follow-on decision? Deck is 68 months old — verify deployment pace and reserves utilization against current data."
      },
      "skill_signal": {
        "value": "All quantitative performance metrics (MOIC, IRR, DPI) are redacted from the deck. Standout companies listed (The Athletic, Superhuman, Clearbanc, Juniper Square, Carrot, FINIX) with downstream investors named. Co-investor quality is strong (YC, a16z, Founders Fund, First Round).",
        "source": "deck pp.11-15, p.18, p.14, p.19, p.24-25",
        "confidence": "low",
        "what_would_change_the_call": "Provide unredacted Fund I and II performance data including gross/net MOIC, IRR, DPI, and return distribution across portfolio. High MOIC could be a single-deal artefact — what is the median MOIC across companies? Deck is 68 months old — verify against current public sources (Crunchbase, exit databases, fund filings)."
      },
      "metrics_interpretation": {
        "value": "Cannot assess — all quantitative metrics are redacted from the deck version provided.",
        "source": "deck pp.11-12, 18, 22-23",
        "confidence": "not_assessable",
        "what_would_change_the_call": "Request unredacted performance data. Ask how Hudson interprets loss rates, and whether high follow-on rate could mask aggressive doubling down on struggling companies rather than picking skill. Deck is 68 months old — verify against current public sources."
      }
    },
    "risk_recognition": {
      "key_person_concentration": {
        "value": "Hudson is sole GP/decision-maker. Thomas and Kerrison in supporting roles with unclear investment authority. No succession plan discussed.",
        "source": "deck pp.4-5",
        "confidence": "med",
        "what_would_change_the_call": "What happens to Fund III if Hudson is incapacitated? Is there a key-person clause? What investment authority do Thomas and Kerrison hold?"
      },
      "market_or_team_novelty": {
        "value": "Pre-seed as institutional category is relatively novel. Deck frames this as cyclical opportunity (seed was here in 2007-2010, now pre-seed). Fund III increases pre-seed weighting to 75% from 60-65% in prior funds.",
        "source": "deck p.6, p.35",
        "confidence": "med",
        "what_would_change_the_call": "Has the pre-seed institutional landscape changed since 2020? Are more firms competing in this space now, and has that affected pricing or access? Deck is 68 months old — verify against current market conditions."
      },
      "conflict_of_interest": {
        "value": "not present",
        "source": "not present",
        "confidence": "not_assessable",
        "what_would_change_the_call": "How are allocation decisions made between the main fund and the reserves fund? Are there LP co-investment rights? How do you handle situations where a Fund II company needs capital that Fund III could provide?"
      },
      "risk_acceptance": {
        "value": "not present",
        "source": "not present",
        "confidence": "not_assessable",
        "what_would_change_the_call": "What is the realistic downside scenario for Fund III? What loss rate is Hudson underwriting, and how does that compare to Fund I/II actuals?"
      }
    }
  },
  "consistency_flags": [
    {
      "claim": "Portfolio size trajectory",
      "sources": ["deck p.35"],
      "discrepancy": "Fund I had 83 companies on $15.3M; Fund II had 95 on $31M; Fund III targets 75 on $40M. The decreasing company count with increasing fund size implies higher concentration, but average check size only increases modestly ($250K→$250K for pre-seed). The math requires significant follow-on/reserves allocation not fully broken out."
    },
    {
      "claim": "Performance data entirely redacted",
      "sources": ["deck pp.11-15, 18, 20, 22-23, 33"],
      "discrepancy": "The deck version provided has all quantitative performance metrics (MOIC, IRR, exit outcomes, portfolio stage counts, SPV data) blacked out. This may be a version edited for public circulation, but it renders the performance narrative unverifiable."
    }
  ],
  "gap_list": [
    {"sub_criterion": "metrics_interpretation", "question": "What are Fund I and II gross/net MOIC, IRR, and DPI today, and how concentrated are returns?", "rank": 1},
    {"sub_criterion": "gp_alignment", "question": "What is Hudson's personal dollar commitment and the team carry structure?", "rank": 2},
    {"sub_criterion": "key_person_concentration", "question": "What is the succession plan if Hudson is unable to continue?", "rank": 3},
    {"sub_criterion": "skill_signal", "question": "What is the loss ratio and how many standout companies have produced realized DPI?", "rank": 4},
    {"sub_criterion": "response_to_failure", "question": "Describe a specific failed investment and resulting process change.", "rank": 5},
    {"sub_criterion": "conflict_of_interest", "question": "How are follow-on allocations decided between main fund and reserves?", "rank": 6},
    {"sub_criterion": "founder_relationships", "question": "Can we speak with founders whose companies struggled, not winners?", "rank": 7},
    {"sub_criterion": "portfolio_management", "question": "With 75 companies and one GP, what does weekly time allocation look like?", "rank": 8},
    {"sub_criterion": "consistency", "question": "What has changed in strategy, team, or portfolio since Q3 2020?", "rank": 9},
    {"sub_criterion": "risk_acceptance", "question": "What is the realistic downside scenario and target loss rate for Fund III?", "rank": 10}
  ]
}
```
