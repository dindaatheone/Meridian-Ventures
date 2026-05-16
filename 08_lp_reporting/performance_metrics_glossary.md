# Performance Metrics Glossary - Meridian Ventures

Every metric used in LP reporting defined precisely
with its calculation methodology, its limitations,
and what a sophisticated LP should look for when
evaluating it. Definitions are scoped to Meridian's
specific fund structure and reporting context.

---

## Primary Return Metrics

### TVPI - Total Value to Paid-In Capital

**Definition:** The ratio of the fund's total value
to the total capital paid in by LPs to date.

**Formula:**
TVPI = (Distributions to Date + Residual NAV) / Total Capital Called

**Interpretation:** A TVPI of 1.5x means that for
every dollar of capital called, the fund has returned
or holds assets worth USD 1.50. TVPI above 1.0x
means the fund is in positive territory before
fees and carry. TVPI of 2.0x or above at fund
maturity is the threshold for a credible institutional
private equity outcome.

**Limitation:** TVPI ignores the time value of money.
A fund that returns 2.0x in year 2 is dramatically
more valuable than a fund that returns 2.0x in year 9,
but TVPI treats both identically. TVPI is most
meaningful when read alongside IRR.

**What to look for:** TVPI trajectory matters as
much as level. A fund at 1.2x TVPI in year 3 with
an accelerating trajectory is in a better position
than a fund at 1.4x TVPI in year 7 with a decelerating
trajectory.

---

### DPI - Distributions to Paid-In Capital

**Definition:** The ratio of cash distributions
returned to LPs to total capital paid in.

**Formula:**
DPI = Total Cash Distributions to LPs / Total Capital Called

**Interpretation:** DPI is the realized return metric.
A DPI of 0.8x means the fund has returned USD 0.80
for every dollar called. DPI below 1.0x means LPs
have not yet received their capital back in cash.
DPI of 1.0x plus the 8% hurdle is the threshold
at which carry begins accruing to the GP.

**Limitation:** DPI is zero for most of the fund
lifecycle until exits begin. Early DPI of zero
does not indicate poor fund performance. It indicates
that the fund is in the deployment and value creation
phase before exits.

**What to look for:** DPI should begin accelerating
in years 6 to 8 as exits close. A fund at year 7
with DPI still at or near zero has either delayed
exits or has not generated exit-quality portfolio
companies. Both are concerns.

---

### RVPI - Residual Value to Paid-In Capital

**Definition:** The ratio of the fund's unrealized
portfolio NAV to total capital paid in.

**Formula:**
RVPI = Reported Residual NAV / Total Capital Called

**Relationship to TVPI:**
TVPI = DPI + RVPI

**Interpretation:** RVPI represents the unrealized
portion of TVPI. Early in the fund lifecycle,
TVPI is almost entirely RVPI. Late in the fund
lifecycle, TVPI should be transitioning toward
DPI as exits close and RVPI declines.

**Limitation:** RVPI is only as reliable as the
valuation methodology applied to unrealized positions.
Level 3 cost basis valuations inflate RVPI stability
but do not reflect genuine mark-to-market movements.

**What to look for:** The ratio of DPI to RVPI
should be increasing through the realization period.
A fund in year 8 with RVPI significantly exceeding
DPI has not converted unrealized value to cash
at the expected pace.

---

### Gross IRR

**Definition:** The internal rate of return on
all fund cash flows including management fees
but before carried interest to the GP.

**Formula:** The discount rate that makes the
net present value of all cash flows equal to zero:

0 = Sum of (Cash Flow at Time T / (1 + IRR)^T)

Where cash flows include capital calls (negative)
and distributions (positive) at their actual dates.

**Interpretation:** Gross IRR is the fund's investment
performance before the cost of GP compensation.
It measures the quality of investment decisions
independent of the fee structure.

**Limitation:** IRR is sensitive to the timing
of cash flows. A fund that returns capital quickly
through early exits can show a high IRR even with
modest absolute returns. Conversely, a fund with
a few very large late exits may show a lower IRR
than its absolute return quality warrants.

**Warning on leverage:** For funds that use leverage
at the fund or portfolio company level, IRR can
be mechanically inflated by leverage without
creating additional fundamental value. Gross IRR
should always be read alongside gross MOIC to
distinguish leverage-amplified IRR from genuine
investment performance.

---

### Net IRR

**Definition:** The internal rate of return from
the LP's perspective after all fees, carried
interest, and fund expenses.

**Formula:** Same as Gross IRR but using LP-level
cash flows: capital called minus management fees
and expenses (negative) and distributions after
carry (positive).

**Interpretation:** Net IRR is the return LPs
actually receive. This is the metric that should
be compared to the hurdle rate, to public market
equivalents, and to other private market fund
alternatives.

**Target:** Net IRR above the 8% hurdle rate
means the LP has cleared the preferred return
threshold. Net IRR above 15% represents institutional-
quality private equity performance for an Asia-Pacific
Series A to B focused fund.

---

### PME - Public Market Equivalent

**Definition:** A metric that compares the fund's
net cash flows to the hypothetical return from
investing the same cash flows at the same times
in a public market index.

**Calculation method used:** Kaplan-Schoar PME.

KS-PME = Sum of (Distributions x Index Multiple at Distribution Date) /
          Sum of (Capital Calls x Index Multiple at Call Date)

Where Index Multiple = Index Level at Evaluation Date /
                       Index Level at Transaction Date

**Benchmark:** MSCI AC Asia Pacific Total Return Index.

**Interpretation:** A PME above 1.0x means the
fund has outperformed the public market benchmark
on a like-for-like cash flow basis. A PME below
1.0x means an LP would have done better investing
in the public index.

**Why PME is the most important metric:**
PME strips out the market beta that all private
equity funds earn simply by being exposed to
equity market appreciation. It isolates the
alpha - the genuine skill-based outperformance -
that justifies the illiquidity premium and the
management fee and carry structure of a private
fund. A fund with strong TVPI and IRR but PME
below 1.0x has not outperformed what a liquid
public index investment would have delivered.
The illiquidity and fees were not justified by
the return.

**Limitation:** PME assumes the public index
is a realistic alternative for the capital deployed.
For LPs with a specific Asia-Pacific private markets
mandate, this assumption is reasonable. For LPs
with a global multi-asset portfolio, the appropriate
benchmark may differ.

---

### MOIC - Multiple on Invested Capital

**Definition:** The ratio of exit proceeds or
current value to the capital invested in a
specific position.

**Formula:**
MOIC = (Exit Proceeds or Current Value) / Capital Invested

**Gross vs Net:**
Gross MOIC is calculated at the position level
before fund-level fees and carry. Net MOIC at
the fund level is the LP-level equivalent after
all costs.

**Interpretation:** A 3x gross MOIC means the
capital invested in that position has returned
three times the investment. MOIC does not account
for time. A 3x MOIC in 2 years is a dramatically
better outcome than a 3x MOIC in 9 years.

**Use in Meridian IC decisions:** MOIC at P50
from the LHS valuation model must exceed 2.5x
for a new Series A investment to clear the IC
threshold. This threshold ensures that the base
case generates fund-level returns consistent
with the net IRR target after fees and carry.

---

## Risk Metrics

### VaR - Value at Risk

**Definition:** The maximum portfolio loss that
is not expected to be exceeded with a given
confidence level over a given time period.

**Meridian calculation:** Monthly VaR at 95% and
99% confidence using Historical Simulation Monte Carlo.
Generated by Meridian-Monte-Carlo/03_lp_reporting/.

**Interpretation:** A monthly VaR of -8% at 95%
confidence means there is a 5% probability that
the portfolio will lose more than 8% of its
value in any given month. Equivalently, 19 months
out of 20, the portfolio loss will not exceed 8%.

**Limitation:** VaR is not a coherent risk measure.
It says nothing about the magnitude of losses
beyond the threshold. Two portfolios can have
identical VaR but very different expected losses
in the tail. CVaR addresses this limitation.

---

### CVaR - Conditional Value at Risk

**Also known as:** Expected Shortfall (ES).

**Definition:** The expected portfolio loss given
that the loss exceeds the VaR threshold.

**Meridian calculation:** CVaR at 95% confidence
generated by Meridian-Monte-Carlo/03_lp_reporting/.

**Interpretation:** If the 95% VaR is -8%, the CVaR
at 95% answers: given that we are in the worst 5%
of outcomes, what is the average loss? A CVaR of
-14% means that in the worst 5% of months, the
average loss is 14%.

**Why CVaR is superior to VaR:** CVaR is a coherent
risk measure. It provides information about the
full tail of the loss distribution rather than
just the threshold. For a portfolio with
alternatives and private credit, tail losses can
be significantly larger than VaR implies, and
CVaR captures this accurately.

---

### Hurdle Rate Probability

**Definition:** The probability that the portfolio
generates an annual return at or above the 8%
LP hurdle rate under current market conditions.

**Meridian calculation:** Generated by Historical
Simulation Monte Carlo in Meridian-Monte-Carlo/03_lp_reporting/.
The simulation draws from 10 years of synthetic
Asia-Pacific asset class return history to generate
10,000 simulated annual portfolio returns. The
hurdle probability is the fraction of simulated
returns at or above 8%.

**Interpretation:** A hurdle probability of 72%
means that under current portfolio composition
and market conditions, 72 out of 100 simulated
annual return paths meet or exceed the 8% LP
hurdle. This is not a guarantee of meeting the
hurdle. It is a probabilistic assessment of
the likelihood given current information.

**Target:** Hurdle probability above 60% at all
points in the fund lifecycle after the first
three years of deployment. Below 60% triggers
a portfolio composition review by the IC.