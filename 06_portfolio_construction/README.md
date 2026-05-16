# 06 - Portfolio Construction

Fund-level architecture governing how individual
investment decisions aggregate into a coherent
portfolio. The difference between a collection
of deals and an institutional portfolio is the
discipline applied at the fund level, not the
quality of individual positions.

---

## Files

| File | Purpose |
|---|---|
| construction_principles.md | Concentration limits, diversification rules, follow-on reserve logic |
| portfolio_model.md | Fund I synthetic portfolio with return modeling and J-curve projection |

---

## The Portfolio as a System

Every individual investment decision in Meridian
Ventures is evaluated against both the position-level
Expanded NPV and the fund-level portfolio impact.
A position that clears all IC thresholds on its
own merits may still be declined if it pushes
corridor or sector concentration beyond the limits
defined in the blind pool thesis.

Portfolio construction discipline is the mechanism
through which the blind pool commitment is honored.
LPs committed capital to a mandate with defined
diversification boundaries. Respecting those
boundaries is not a constraint on returns - it
is the fulfillment of a governance obligation.