# Synthetic Valuation Case - ArcWealth Pte. Ltd.

This document presents the complete Expanded NPV
valuation for the ArcWealth Series A investment
documented in 04_due_diligence/dd_template/synthetic_deal_memo.md.
All quantitative outputs reference the LHS model
in Meridian-Monte-Carlo/01_lhs_valuation/.

---

## Deal Parameters

**Company:** ArcWealth Pte. Ltd.
**Stage:** Series A
**Proposed investment:** USD 8M
**Post-money valuation:** USD 40M
**Implied ownership:** 20% fully diluted

---

## LHS Model Assumptions

Input file: Meridian-Monte-Carlo/01_lhs_valuation/inputs/venture_assumptions.json

| Input Variable | Distribution | Parameters | Rationale |
|---|---|---|---|
| Revenue growth Year 1 | Triangular | Min 40%, Mode 75%, Max 150% | ArcWealth's existing pipeline of 7 qualified opportunities supports mode of 75%. Upper tail reflects potential enterprise contract upside. |
| Revenue growth Years 2-5 | Normal | Mean 55%, Std 20% | Growth normalization as institutional sales cycles lengthen at larger contract sizes. Clipped at 10% floor. |
| Terminal EBITDA margin | Normal | Mean 22%, Std 8% | Asia-Pacific B2B SaaS at scale. Lower than US benchmarks reflecting higher client servicing costs. |
| Exit multiple EV/EBITDA | Triangular | Min 8x, Mode 14x, Max 25x | Comparable Asia-Pacific wealthtech M&A 2022-2025. Mode reflects median transaction. |
| WACC | Normal | Mean 18%, Std 3% | Series A illiquidity premium plus Asia-Pacific risk premium over 4.5% USD risk-free rate. |

---

## LHS Model Outputs

Reference: Meridian-Monte-Carlo/01_lhs_valuation/outputs/valuation_summary.csv

| Percentile | Equity Value | Gross MOIC on USD 8M |
|---|---|---|
| P5 | USD 4.2M | 0.5x |
| P10 | USD 12.4M | 1.6x |
| P25 | USD 19.8M | 2.5x |
| P50 | USD 31.8M | 4.0x |
| P75 | USD 48.3M | 6.0x |
| P90 | USD 68.5M | 8.6x |
| P95 | USD 84.1M | 10.5x |

**Mean equity value:** USD 33.4M
**Standard deviation:** USD 19.7M

---

## IC Threshold Assessment

| Threshold | Required | Result | Assessment |
|---|---|---|---|
| P10 above initial investment | Above USD 8M | USD 12.4M | Pass |
| P50 gross MOIC above 2.5x | Above 2.5x | 4.0x | Pass |
| Static NPV positive at P50 | Positive | USD 23.8M | Pass |
| Expanded NPV positive at P50 | Positive | USD 26.1M | Pass |

---

## Expanded NPV Calculation

**Static NPV at P50:**
P50 equity value: USD 31.8M
Series A investment: USD 8M
Static NPV: USD 23.8M

**Compound Option Value:**
P(Series B participation): 0.75
Adjusted above base case of 0.65 reflecting:
all five DD dimensions pass with no fails,
existing client pipeline reduces Series B
uncertainty, NRR of 118% validates product stickiness.
Series B economic value: USD 3,500,000
Option Value: 0.75 x USD 3,500,000 = USD 2,625,000

**Abandonment Option Value:**
Qualitative assessment: moderate positive value.
ArcWealth's clean cap table and strong unit economics
create secondary market liquidity at a discount
to fair value if abandonment becomes necessary.
Estimated at USD 500,000 based on comparable
secondary transaction discounts for Asia-Pacific
B2B SaaS at Series A stage.

**Expanded NPV:**
USD 23,800,000 + USD 2,625,000 + USD 500,000
= USD 26,925,000

Rounded to USD 26.9M for IC reporting.

---

## Sensitivity Analysis

The three highest-sensitivity inputs and the
impact of a one standard deviation adverse move
in each on the P50 equity value:

| Input | Base Case | Adverse Move | P50 Impact |
|---|---|---|---|
| Exit multiple | 14x mode | 11x mode | -22% to P50 equity value |
| Terminal EBITDA margin | 22% mean | 14% mean | -18% to P50 equity value |
| Revenue growth Years 2-5 | 55% mean | 35% mean | -11% to P50 equity value |

Combined adverse move in all three simultaneously
reduces P50 equity value to approximately USD 16M,
producing a gross MOIC of 2.0x on the USD 8M
investment. This combined adverse scenario produces
a static NPV of approximately USD 8M and an Expanded
NPV of approximately USD 11M. The investment
remains positive Expanded NPV even in this combined
adverse scenario.

---

## Valuation Distribution Chart

Reference: Meridian-Monte-Carlo/01_lhs_valuation/outputs/valuation_distribution.png

The distribution is right-skewed as expected for
a venture investment with bounded downside and
uncapped upside. The P10 to P90 range spans USD 56M,
reflecting the genuine uncertainty in exit timing
and market conditions rather than artificially
narrow assumptions. The IC is making a decision
under meaningful uncertainty. The distribution
makes that uncertainty explicit rather than
concealing it behind a single point estimate.

---

## IC Conclusion

ArcWealth clears all four IC valuation thresholds.
The Expanded NPV of USD 26.9M against a USD 8M
investment reflects a risk-adjusted value creation
estimate that accounts for the full distribution
of outcomes, not the optimistic case.

The sensitivity analysis confirms that even a
combined adverse move in the three highest-sensitivity
inputs does not produce a negative Expanded NPV.
The investment has a margin of safety in the
valuation that justifies the USD 8M commitment
within the fund's portfolio construction constraints.