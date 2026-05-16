# Meridian Ventures

**Capital Deployment Layer | Meridian Private Bank | Singapore MAS**

---

## What This Is

This repository is the capital deployment infrastructure of
Meridian Private Bank. It documents the venture arm of a
Singapore-domiciled boutique private banking institution
serving HNW and UHNW clients across five Asia-Pacific
corridors: China, Singapore, Indonesia, Macau, and Brunei.

Meridian Ventures is not a standalone PE fund. It is a
hybrid: PE fund architecture nested inside private bank
integration logic. This structure creates three competitive
advantages that neither a pure PE fund nor a pure private
bank can replicate independently.

First, proprietary deal access through the private bank's
UHNW client network across five jurisdictions. Second,
co-investment rights that convert venture exits into AUM
growth events for the wealth management side. Third,
BI-driven due diligence applying the same intelligence
infrastructure used for client portfolio analysis to
venture target evaluation.

---

## The Hybrid Architecture Decision

Two alternatives were rejected before this structure was chosen.

A pure PE fund repo would demonstrate capital allocation
discipline but miss the private banking integration that
makes Meridian's deal access and co-investment architecture
defensible. Any generalist fund can document a GP/LP
structure. Not every fund can source deals through a
UHNW client network spanning five Asia-Pacific corridors.

A pure private banking venture arm would miss the
institutional rigor that makes the blind pool credible
to LP investors. Thesis-driven commitment requires the
full PE structural documentation to be taken seriously
by institutional capital.

The hybrid closes both gaps simultaneously.

---

## Repo Architecture

Meridian-Ventures/
|
|-- 00_institutional_context/      <- Why Ventures exists inside a private bank
|   |-- ventures_identity.md       <- Hybrid architecture rationale and three integration mechanisms
|   +-- competitive_positioning.md <- Sequential game vs incumbents and commitment trigger
|
|-- 01_fund_structure/             <- GP/LP mechanics, blind pool, fund economics
|   |-- gp_lp_structure.md         <- GP identity, LP profile, blind pool rationale
|   |-- fund_economics.md          <- 2/20 structure, hurdle, clawback, fund lifecycle
|   |-- waterfall.md               <- Distribution waterfall with worked numerical example
|   +-- blind_pool_thesis.md       <- Full investment mandate LPs commit to
|
|-- 02_investment_thesis/          <- What Meridian Ventures invests in and why
|   |-- thesis_statement.md        <- Uncertainty-reduction principle, Series A-B window
|   |-- real_options_framework.md  <- Four real options mapped to investment process
|   |-- target_profile.md          <- Ideal Series A target characteristics
|   +-- sector_focus.md            <- Five target sectors with private bank rationale
|
|-- 03_investment_committee/       <- How investment decisions are made
|   |-- ic_framework.md            <- IC structure, quorum, vote rules
|   |-- stage_gate_criteria.md     <- Series A entry, Series B follow-on, abandon triggers
|   +-- decision_log_template.md   <- Template for each IC decision with LHS valuation link
|
|-- 04_due_diligence/              <- BI-driven due diligence framework
|   |-- dd_framework.md            <- Five-dimension DD methodology
|   |-- dd_checklist.md            <- Operational checklist with pass/flag/fail status
|   +-- dd_template/
|       +-- synthetic_deal_memo.md <- Completed DD memo for synthetic Series A target
|
|-- 05_valuation/                  <- Expanded NPV valuation framework
|   |-- valuation_framework.md     <- Static NPV plus option value, LHS integration
|   +-- synthetic_valuation_case.md <- Worked case linking to Monte Carlo LHS outputs
|
|-- 06_portfolio_construction/     <- Fund-level portfolio architecture
|   |-- construction_principles.md <- Concentration limits, diversification rules
|   +-- portfolio_model.md         <- Fund I synthetic portfolio with J-curve projection
|
|-- 07_pb_integration/             <- Private bank integration layer
|   |-- deal_sourcing_network.md   <- How UHNW client network generates proprietary deal flow
|   |-- co_investment_mechanics.md <- Eligibility, allocation, AUM conversion logic
|   +-- aum_conversion_model.md    <- Financial logic of co-investment as AUM growth
|
|-- 08_lp_reporting/               <- Quarterly LP communication framework
|   |-- reporting_framework.md     <- What LPs receive, how often, in what format
|   |-- lp_report_template.md      <- Full quarterly LP report template
|   +-- performance_metrics_glossary.md <- IRR, MOIC, DPI, RVPI, TVPI, PME defined
|
+-- docs/
|-- methodology.md             <- Why hybrid, how real options governs deployment
|-- glossary.md                <- Ventures-specific terms scoped to Meridian usage
+-- CHANGELOG.md               <- Version history

---

## Connection to the Other Two Repos

| Input From | What It Feeds |
|---|---|
| Meridian-Business-Intelligence clients.csv | Co-investment eligibility flags, corridor AUM for deal sourcing prioritization |
| Meridian-Monte-Carlo/01_lhs_valuation/outputs | P10/P50/P90 valuation range in IC decision logs and deal memos |
| Meridian-Monte-Carlo/02_macro_stress/outputs | Macro risk section of quarterly LP report |
| Meridian-Monte-Carlo/03_lp_reporting/outputs | Risk dashboard in LP report template |

---

## Fund Parameters

| Parameter | Specification |
|---|---|
| Fund Name | Meridian Ventures Fund I |
| GP Entity | Meridian Capital Management Pte. Ltd. |
| Jurisdiction | Singapore MAS |
| Target Size | USD 150M to 250M |
| Management Fee | 2.0% per annum |
| Hurdle Rate | 8.0% per annum |
| Carried Interest | 20% above hurdle |
| Fund Life | 10 years |
| Deployment Period | Years 1 to 5 |
| Realization Period | Years 6 to 10 |
| Target Stage | Series A and B |
| Geographic Focus | Asia-Pacific - China, Singapore, Indonesia, Macau, Brunei |
| Exit Mechanism | Recapitalization and continuation vehicles - no third-party sale |

---

## Part of Meridian Private Bank

This repo is a portfolio artifact demonstrating founder-level
strategic thinking in private banking and venture capital.

**Singapore MAS Jurisdiction | Asia-Pacific Focus | Version 1.0**
All data synthetic. Not a licensed institution.

