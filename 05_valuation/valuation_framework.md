# Valuation Framework - Meridian Ventures

## The Expanded NPV Framework

Every investment decision uses Expanded NPV as the
operative valuation metric. The framework has three
components that are calculated independently and
combined to produce the final decision metric.

---

## Component 1 - Static NPV

Static NPV is the present value of projected cash
flows discounted at the risk-adjusted WACC, minus
the initial Series A investment. It is the baseline
financial case for the investment assuming no
managerial flexibility beyond the initial commitment.

The LHS Monte Carlo model generates a distribution
of static NPV outcomes rather than a point estimate.
The distribution reflects the uncertainty in five
input variables: Year 1 revenue growth, Years 2-5
revenue growth, terminal EBITDA margin, exit multiple,
and WACC. Each variable is sampled 10,000 times
using Latin Hypercube Sampling to ensure full
coverage of the input distribution including tails.

The output is a percentile table of equity values
from P5 through P95. The IC uses P10 as the downside
case, P50 as the base case, and P90 as the upside case.

**IC thresholds for static NPV:**
P10 equity value must exceed the initial Series A
investment at minimum. An investment where the
downside case returns less than the capital invested
requires explicit IC justification based on option
value before approval.

P50 equity value must produce a gross MOIC above
2.5x on the initial Series A investment to generate
a fund-level return consistent with the 8% hurdle
after fees and carry.

---

## Component 2 - Compound Option Value

The compound option value captures the economic
benefit of the right - but not the obligation -
to participate in Series B. It has two parameters:
the probability of Series B participation and the
economic value of that participation.

**Probability of Series B participation:**
Calibrated per deal based on the strength of the
Stage Gate 1 assessment. A deal where all five DD
dimensions pass with no flags has a higher probability
of reaching a fundable Series B than a deal where
multiple dimensions are flagged. The base case
assumption in venture_assumptions.json is 65%.
This parameter is adjusted up to 80% for the
strongest DD outcomes and down to 45% for deals
with multiple flag assessments.

**Economic value of Series B participation:**
The value of participating at Series B before the
growth equity market has fully priced the execution
evidence that Meridian has observed as a Series A
investor. This is estimated as the discount to
fair value at which Meridian can participate at
Series B by exercising its pro-rata rights before
the round is fully priced in competitive tension.
The base case assumption is USD 3.5M per deal.
This parameter is adjusted based on the competitive
dynamics of the Series B market in the relevant
sector at the time of Series A investment.

**Compound option value formula:**
Option Value = P(Series B) x Series B economic value
Base case: 0.65 x USD 3,500,000 = USD 2,275,000

---

## Component 3 - Abandonment Option Value

The abandonment option value captures the economic
benefit of being able to stop deploying capital
if execution evidence does not support continuation.
A fund with no follow-on reserve and no ability
to abandon positions has negative option value
from the abandonment dimension - it must hold
through bad outcomes with no ability to accelerate
capital recovery.

Meridian's stage gate criteria and follow-on reserve
structure create positive abandonment option value
by preserving the ability to redirect follow-on
capital from underperformers to the strongest
performers. This value is estimated qualitatively
per deal and documented in the IC decision log
rather than calculated precisely, because the
range of abandonment scenarios is too wide to
parameterize reliably at Series A stage.

---

## Expanded NPV Calculation
Expanded NPV = Static NPV (P50) + Compound Option Value + Abandonment Option Value
Minimum threshold: Expanded NPV must be positive at P50
Strong case: Expanded NPV positive at P25
Exceptional case: Expanded NPV positive at P10

The IC does not approve investments where Expanded
NPV is negative at P50. A negative Expanded NPV
at P50 means that even accounting for the option
value of staged participation, the investment
is expected to destroy value relative to the
opportunity cost of deploying the capital elsewhere
in the fund.

---

## LHS Integration

The LHS valuation model in Meridian-Monte-Carlo
generates the static NPV distribution that feeds
this framework. The integration works as follows:

The venture_assumptions.json file in
01_lhs_valuation/inputs/ is populated with
deal-specific assumptions derived from the DD
process. The model is run and the output files
in 01_lhs_valuation/outputs/ are reviewed by
the Risk and Valuations Officer before the IC
package is distributed.

The valuation_summary.csv output is embedded
directly in the IC decision log. The P10, P50,
and P90 equity values, the static NPV, and the
Expanded NPV are all drawn from this file. There
is no manual transcription. The model output
is the IC input.

This integration eliminates the risk of valuation
being adjusted to make a deal appear more attractive
than the model indicates. The model runs, the
output is filed, and the IC receives the unmodified
output. The only parameter that can be adjusted
between model runs is the venture_assumptions.json
file, and any change to that file must be documented
in the IC decision log with the rationale for
the parameter revision.

---

## Valuation Discipline Rules

Four rules govern how the valuation framework is
applied. They exist to prevent the cognitive biases
that degrade valuation discipline in competitive
deal environments.

**Rule 1 - Model before negotiation.**
The LHS model is run before Meridian enters term
sheet negotiation. The output establishes the
maximum valuation at which the Expanded NPV remains
positive at P50. This maximum is the GP's walk-away
price in negotiation. Winning a deal at a valuation
that produces negative Expanded NPV is a loss,
not a success.

**Rule 2 - No post-negotiation model revision.**
Once term sheet negotiation begins, the model
assumptions are frozen. Revising assumptions to
make a deal work at an agreed valuation that the
original model rejected is a form of motivated
reasoning that the framework is designed to prevent.
If the negotiated valuation exceeds the model's
maximum, the deal is passed.

**Rule 3 - Follow-on uses updated model.**
Series B follow-on decisions require a fresh model
run with updated assumptions reflecting 18 to 24
months of observed operating performance. The Series A
model assumptions are not carried forward to the
follow-on decision. The follow-on model reflects
what is now known, not what was projected.

**Rule 4 - Abandonment uses replacement cost logic.**
When evaluating abandonment, the relevant comparison
is not the original Series A investment cost but
the current opportunity cost of the capital locked
in the position. A position worth USD 3M in the
secondary market costs Meridian USD 3M to hold,
regardless of the original USD 8M invested. The
abandonment decision compares USD 3M deployed in
the next best alternative against USD 3M continuing
in the current position.