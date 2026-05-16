# Real Options Framework - Meridian Ventures

## Options Theory Applied to Venture Capital

Real options theory prices the value of managerial
flexibility under uncertainty. In venture capital,
every funding stage creates a set of options: the
right but not the obligation to continue, follow-on,
or exit based on observed performance. This flexibility
has quantifiable value that static DCF analysis ignores.

Meridian's investment process operationalizes four
real options precisely. Each maps to a specific
decision point in the investment lifecycle.

---

## Option 1 - The Option to Defer

**Financial analog:** Call option on the underlying asset.
**Value driver:** Uncertainty. Higher uncertainty increases
option value by widening the upside distribution while
capping the downside at the option premium paid.

**Meridian application:** Meridian does not invest at
pre-seed or seed stage. The decision to wait until
Series A is not conservatism. It is the exercise of
the option to defer until the information value of
early operating history exceeds the cost of waiting,
which includes the opportunity cost of not participating
in earlier upside and the risk of being priced out
of the round at Series A by competitive dynamics.

The trigger for exercising the defer option is the
availability of sufficient execution evidence to
distinguish operational capability from early-stage
noise. That evidence threshold is defined in the
stage gate criteria in 03_investment_committee.

**Quantification:** The option to defer is implicitly
valued in the LHS Monte Carlo model through the
input distribution for revenue growth year 1. The
wide triangular distribution (40% to 150%, mode 75%)
reflects the range of outcomes observable at Series A
stage after the deferral period has allowed early
evidence to accumulate.

---

## Option 2 - The Compound Option

**Financial analog:** Option on an option. Each stage
is an option on the next.
**Value driver:** Sequential information revelation.
Each stage produces information that improves the
precision of the next stage decision.

**Meridian application:** Series A capital buys two
things simultaneously. First, the economic exposure
to the portfolio company's value creation between
Series A and exit. Second, the right - but not the
obligation - to participate in Series B at a price
determined by Series A to B performance.

The second thing is the compound option. Its value
is the product of the probability of Series B
participation (65% in the base case assumption in
venture_assumptions.json) and the economic benefit
of participating at Series B before the growth
equity market has fully priced the execution evidence
that Meridian has observed as a Series A investor.

**Why this matters for Expanded NPV:** A venture with
negative static NPV at Series A may have positive
Expanded NPV when the compound option value of Series
B participation is included. The LHS model calculates
both. The IC decision uses Expanded NPV, not static NPV.

**Quantification:** option_value_parameters in
venture_assumptions.json: Series B probability 65%,
Series B option value USD 3.5M. These parameters
are calibrated per deal based on the quality of
execution evidence and the competitive dynamics
of the Series B market in the relevant sector.

---

## Option 3 - The Option to Abandon

**Financial analog:** Put option on the underlying asset.
**Value driver:** Salvage value. The higher the
recoverable value at abandonment, the more valuable
the option.

**Meridian application:** Every Meridian Ventures
investment has a defined recapitalization or
abandonment threshold documented in the IC decision
log at the time of initial investment. If a portfolio
company fails to achieve the stage gate milestones
defined at Series A, the investment committee evaluates
three paths: follow-on at a restructured valuation,
bridge financing to extend the runway toward a specific
milestone, or controlled wind-down to recover residual
asset value.

The option to abandon is not exercised lightly. In
venture capital, the J-curve dynamics and the compound
option structure mean that early underperformance
does not necessarily predict final outcome. The
abandonment decision requires evidence that the
execution quality hypothesis underlying the original
investment has been falsified, not merely that
short-term results are below plan.

**Quantification:** The abandonment threshold maps to
the P10 case in the LHS valuation output. If observed
company performance is tracking below the P10 equity
value at the next financing milestone, the IC evaluates
abandonment against the cost of continuing.

---

## Option 4 - The Option to Expand

**Financial analog:** Call option on additional units.
**Value driver:** Operational scalability. The value
of the expansion option increases with the quality
of the platform being scaled.

**Meridian application:** For the strongest performers
in the portfolio, Meridian exercises the option to
expand through Series B follow-on participation.
The criteria for Series B follow-on are documented
in stage_gate_criteria.md. The economic logic is
that a portfolio company tracking at or above the
P50 valuation case at the Series A to B transition
has validated the execution quality hypothesis.
Additional capital deployed at Series B participates
in a de-risked growth trajectory at a valuation
that still reflects incomplete execution evidence
from the growth equity market's perspective.

The expansion option also applies to the co-investment
dimension. For the strongest performers, co-investment
rights are offered to eligible private banking clients
at Series B, creating a larger co-investment ticket
than was offered at Series A and deepening the client
relationship at the moment of maximum conviction
about the portfolio company's trajectory.

---

## Expanded NPV Formula

Every IC investment decision uses Expanded NPV:
Expanded NPV = Static NPV + Option Value
Where:
Static NPV = PV of projected cash flows discounted at WACC
minus initial Series A investment
Option Value = (P(Series B) x Series B option value)
+ (P(abandonment avoided) x abandonment cost saved)
+ (P(expansion) x expansion value premium)

The LHS Monte Carlo model in Meridian-Monte-Carlo
calculates Static NPV and the compound option value
across 10,000 simulated paths. The abandonment and
expansion option values are estimated qualitatively
by the IC at the time of each investment decision
and documented in the decision log.