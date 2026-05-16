# Reporting Framework - Meridian Ventures Fund I

## Reporting Cadence

| Report | Frequency | Delivery Deadline | Format |
|---|---|---|---|
| Quarterly LP Report | Quarterly | 45 days after quarter end | PDF with data appendix |
| Annual Audited Financials | Annual | 90 days after fiscal year end | Audited PDF |
| Capital Call Notice | As required | 10 business days before call date | PDF with wire instructions |
| Distribution Notice | As required | 5 business days before distribution | PDF with wire instructions |
| Material Event Notice | As required | Within 48 hours of event | Email with PDF attachment |

**Material events** requiring immediate notification:
Portfolio company entering a formal sale process.
Portfolio company CEO departure.
Write-off decision made by IC.
Regulatory adverse finding at any portfolio company.
Any single position exceeding 15% of fund NAV due
to mark-up from a new financing round.

---

## Quarterly Report Structure

### Section 1 - Executive Summary

One page. Three paragraphs. No tables.

The first paragraph states the fund's current
position: total capital called, total capital
deployed, number of active positions, current
reported NAV, and TVPI since inception.

The second paragraph identifies the most significant
development of the quarter across the portfolio:
the strongest performing company's milestone,
the most important strategic development, or the
most material risk change. One development only.
Forcing a single most important development is
a discipline that prevents the executive summary
from becoming a list of items with no hierarchy.

The third paragraph states the outlook for the
next quarter: anticipated capital calls, expected
exit processes, pipeline deals approaching IC,
and any macro developments with material portfolio
relevance. The Iran war macro stress calibration
case from Meridian-Monte-Carlo is referenced
here when macro conditions are creating portfolio-level
risk worth flagging.

### Section 2 - Portfolio Performance

One table per active portfolio company. Each table
contains: company name, corridor, sector, investment
date, cost basis, current reported valuation, gross
MOIC to date, ownership percentage, and a three-sentence
operational update.

The operational update answers three questions:
what did the company achieve this quarter, what
are the two most important metrics tracking against
plan, and what is the primary risk heading into
the next quarter. Three sentences. No more.

Portfolio companies are listed in order of current
reported valuation from highest to lowest. This
ordering is deliberate: LPs focus most attention
on the largest positions and the ordering should
reflect that priority rather than hiding the
strongest performers in the middle of a list
ordered by investment date.

### Section 3 - Fund-Level Performance Metrics

The six metrics every LP investment committee
tracks, calculated as of quarter end:

TVPI: total value to paid-in capital.
DPI: distributions to paid-in capital.
RVPI: residual value to paid-in capital.
Gross IRR since inception.
Net IRR since inception after fees and carry.
PME against MSCI AC Asia Pacific index.

Each metric is presented with its current value,
its value at the prior quarter end, and a one-sentence
interpretation of the change. Full definitions
in performance_metrics_glossary.md.

### Section 4 - Risk Dashboard

The Monte Carlo LP risk report output from
Meridian-Monte-Carlo/03_lp_reporting/ feeds
directly into this section. Three metrics are
presented with their current values and a
comparison to the prior quarter:

Portfolio VaR at 95% confidence (monthly).
Expected shortfall at 95% confidence (monthly).
Probability of meeting 8% annual hurdle rate
given current portfolio composition and market conditions.

The macro stress section presents the current
position of the portfolio on the Strait of Hormuz
disruption scenario distribution from
Meridian-Monte-Carlo/02_macro_stress/. If macro
conditions have moved materially since the last
report, the stress test is re-run and the updated
portfolio impact distribution is presented.

### Section 5 - Pipeline and Deployment Update

Two subsections.

**Active pipeline:** Deals currently in formal
diligence with expected IC submission date and
indicative position size. No company names are
disclosed at this stage. Deals are described by
sector and corridor only.

**Deployment status:** Total capital called to date,
total capital deployed, follow-on reserve status,
and expected remaining deployment timeline.

### Section 6 - Co-Investment Activity

Co-investment opportunities offered to eligible
private banking clients during the quarter.
For each opportunity: sector, corridor, Meridian
position size, co-investment tranche offered,
co-investment tranche subscribed, and average
ticket size. Company names are included for
opportunities that have already been disclosed
to co-investors. Pending opportunities are
described by sector only.

---

## Monte Carlo Integration

The risk dashboard in Section 4 is the primary
integration point between this repo and
Meridian-Monte-Carlo. The integration works
as follows:

The historical simulation model in
Meridian-Monte-Carlo/03_lp_reporting/ is run
at the end of each quarter using the current
portfolio composition as the weighting input.
The model generates updated VaR, CVaR, and
hurdle probability figures that are inserted
directly into the quarterly report template.

The scenario stress model in
Meridian-Monte-Carlo/02_macro_stress/ is run
when macro conditions change materially. The
calibration report from the Iran war Q1 2026
event is referenced in any quarter where
geopolitical risk is a primary portfolio concern.

---

## Valuation Policy

Portfolio company valuations are updated quarterly
using the following hierarchy:

**Level 1 - Observable transaction price:**
If a portfolio company has closed a new financing
round during the quarter at an arm's length price,
that price sets the new fair value. This is the
most reliable valuation input and requires no
further analysis.

**Level 2 - Comparable company multiples:**
If no new financing round has closed, valuation
is updated using the median revenue or EBITDA
multiple of comparable public companies in the
same sector and geography, applied to the portfolio
company's trailing twelve-month revenue or EBITDA.
The comparable company set is documented and
consistent across quarters.

**Level 3 - Cost basis:**
For companies less than 12 months from the last
financing round with no material positive or
negative operational developments, valuation
is held at cost basis.

**Write-down triggers:**
Valuation is written down below cost when: a new
financing round closes at a lower price than the
prior round (down round), or when Stage Gate 3
abandonment criteria are met and a controlled
wind-down is initiated.

All valuation decisions are documented in the
IC decision log for the relevant quarter and
reviewed by the LP Advisory Board annually.