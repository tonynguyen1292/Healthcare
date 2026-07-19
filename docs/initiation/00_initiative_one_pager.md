# Initiative One-Pager — WA Mental Health Treatment Gap

*Confirmed from repo unless marked [ASSUMPTION] or [TO BE CONFIRMED]. Sources: `01_problem_statement.md`, `02_scope_and_assumptions.md`, `03_stakeholder_analysis.md`.*

| | |
|---|---|
| **Initiative** | The Mental Health Treatment Gap in Western Australia |
| **Sponsor** | [TO BE CONFIRMED] — no named sponsor exists; this project is currently framed as an independent case study, not a commissioned engagement |
| **Product Owner / BA** | Vy Nguyen |
| **Stage** | Discovery/definition largely complete; delivery (data ingestion, analysis, reporting) not yet started |

## The problem
There is a significant gap between the mental health needs of people in WA and the services they receive, driven by financial, geographic, and system-level barriers. National and modelled datasets exist to quantify this, but the information isn't presented in a way that clearly shows *where* the gap is worst or *who* it affects most — making it harder for planners to prioritise funding and service models.

## What we're building
An evidence base and recommendation report that quantifies the WA treatment gap (need minus service use) nationally, by state, and by Primary Health Network (PHN), identifies priority regions/populations, and translates findings into decision-ready recommendations. [ASSUMPTION] A future extension may add an interactive dashboard — not yet decided (see Business Case, §Options).

## Who it's for
WA Dept of Health / Mental Health Commission, WA Primary Health Alliance (WAPHA) and PHN planners, community mental health NGOs (e.g. WAAMH), GPs/primary care providers. [CONFIRMED — full detail in `01_stakeholder_register.md`]

## Data foundation
ABS/AIHW National Study of Mental Health and Wellbeing (NSMHW) 2020–2022 release — national tables, state/territory tables (WA-specific file confirmed present), and PHN-modelled estimates covering disorder prevalence, severity, service use, medication (PBS), and self-harm/suicidality indicators. [CONFIRMED by direct inspection of `data_raw/*.zip` contents]

## Current status
Phase 1 (problem definition, scope, stakeholders, requirements, data mapping, AS-IS process) is done and strong. Phase 2 (data ingestion/analysis) and Phase 3 (visualisation/recommendations) have not started — `notebooks/`, `data_processed/`, and `reports/` are empty. [CONFIRMED]

## Top 3 risks
1. Modelled/small-area PHN estimates carry statistical uncertainty — risk of over-reading regional "differences" as real signal.
2. Sensitive content (suicidality/self-harm tables) requires careful, non-sensational, aggregate-only handling.
3. Discovery has significantly outpaced delivery — risk of continuing to document instead of starting Phase 2. *(Full register: `02_risk_register.md`.)*

## Decision needed now
Confirm whether this proceeds as a documentation-only case study or a "as-if commissioned" delivery initiative with the fuller pack in this folder — that choice shapes tone and governance weight for everything downstream. [TO BE CONFIRMED — see Business Case §Recommended option]
