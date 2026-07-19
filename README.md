# The Mental Health Treatment Gap in Western Australia

This project analyses the mental health treatment gap in Western Australia, with a focus on how financial barriers, rural and remote access issues, and systemic service limitations contribute to unmet mental health needs. It is designed as a hybrid Business Analysis (BA) and Data Analysis project to demonstrate end-to-end problem framing, data-driven insight generation, and practical recommendations for decision makers.

## Project context

National surveys show that around one in five Australians experiences a mental disorder in a given year, yet less than half of those with a 12‑month mental disorder access professional help for their mental health. Evidence also shows that people living outside major cities have more limited access to mental health services despite similar levels of need. In Western Australia, regional and remote communities experience high distress, lower wellbeing, and ongoing unmet mental health needs. 

This project uses modelled estimates from the National Study of Mental Health and Wellbeing (NSMHW) and related sources to quantify the treatment gap in Western Australia and identify where access barriers are likely to be most acute. 

**Start here:** `docs/initiation/00_initiative_one_pager.md` for a one-screen summary, or `docs/initiation/09_delivery_plan_sprints.md` for the full sprint-by-sprint delivery plan and timeline.

## Objectives

- Quantify mental health need and service use for Western Australia overall and by region.
- Estimate the mental health treatment gap (need vs service utilisation).
- Explore how financial, geographic (rural/remote) and systemic factors contribute to unequal access.
- Provide evidence-based recommendations for policy, funding, and service planning.

## Role and approach (Hybrid BA)

This repository is structured to reflect the work of a hybrid Business Analyst who combines problem framing, stakeholder and requirements analysis, and data exploration:

- Define the problem, business context, and stakeholder needs.
- Translate those needs into analytical questions and data requirements.
- Perform exploratory and targeted analysis using official health data.
- Communicate insights and recommendations in a concise, decision‑friendly way.

## Repository structure

Planned structure:

```text
Healthcare/
├─ data_raw/
│  ├─ Mental-health-tables-National.zip
│  ├─ Mental-health-tables-State-and-territory.zip
│  └─ Modelled-estimates-from-NSMHW-by-PHN.zip
├─ data_processed/
│  └─ wa_treatment_gap_summary.csv
├─ docs/
│  ├─ 01_problem_statement.md          ✅ committed
│  ├─ 02_scope_and_assumptions.md      ✅ committed
│  ├─ 03_stakeholder_analysis.md       ✅ committed
│  ├─ 04_business_requirements.md      ✅ committed
│  ├─ 05_data_sources_and_questions.md ✅ committed
│  ├─ 06_as_is_process.md              ✅ committed
│  ├─ 07_gap_analysis.md               🟡 stub — content scheduled Sprint 4
│  ├─ 08_solution_requirements.md      🟡 stub — content scheduled Sprint 4
│  ├─ 09_use_cases.md                  🟡 stub — content scheduled Sprint 5
│  └─ initiation/                      ✅ committed — PO/BA delivery-governance pack, see below
├─ notebooks/
│  ├─ 01_data_ingestion_wa.ipynb       ✅ Sprint 1 complete — Epic H1, verified against real data
│  ├─ 02_treatment_gap_analysis.ipynb  🟡 stub — Epics H2-H3, Sprints 2-3
│  └─ 03_barrier_analysis.ipynb        🟡 stub — Epic H4, Sprints 3-4
├─ reports/
│  ├─ 01_findings_and_recommendations.md 🟡 stub — Sprint 4
│  ├─ 02_executive_summary.md            🟡 stub — Sprint 4-5
│  └─ 03_dashboard_spec.md             🔲 not started — stretch scope only, not authorised by current charter
├─ .gitignore
└─ README.md
```

🟡 stub = file exists with planned structure and sprint reference, content not yet written — see `docs/initiation/09_delivery_plan_sprints.md` for the sprint-by-sprint plan.

## Key documentation

`docs/01_problem_statement.md` – defines the core healthcare access problem, project purpose, objectives, and success criteria.

`docs/02_scope_and_assumptions.md` – defines boundaries, assumptions, constraints, and what is included or excluded from the analysis.

`docs/03_stakeholder_analysis.md` – identifies key stakeholder groups and their planning, service, and information needs.

`docs/04_business_requirements.md` – captures high-level business requirements that guide the analysis and reporting.

`docs/05_data_sources_and_questions.md` – maps business requirements to analytical questions and supporting data sources.

`docs/06_as_is_process.md` – describes the current-state process through which people in WA seek and access mental health care.

Planned BA extension documents
`docs/07_gap_analysis.md` – will compare the current state to the desired future state and identify major business and service gaps.

`docs/08_solution_requirements.md` – will translate identified gaps into solution-oriented business and information requirements.

`docs/09_use_cases.md` – will describe how specific stakeholders would use the project outputs for planning and decision-making.

## Analytical and reporting outputs
`notebooks/` – exploratory and targeted analytical workflow supporting the case study. `01_data_ingestion_wa.ipynb` is complete and verified (Sprint 1); the rest land sprint by sprint per the roadmap above.

`data_processed/` – cleaned outputs used to quantify treatment gap indicators. `national_state_indicators.csv` (24,865 rows) and `phn_modelled_indicators.csv` (48,267 rows) exist as of Sprint 1 — see data dictionary below.

`reports/` – final findings, recommendations, and executive summary. Structure exists now (stubs); content lands in Sprint 4-5.

### Data dictionary — Sprint 1 output

**`national_state_indicators.csv`** (National + State/Territory sources): `table_id`, `geography`, `category`, `item`, `sex`, `age_group`, `metric_type` (estimate/rse/proportion/moe), `value`, `source_file`.

**`phn_modelled_indicators.csv`** (PHN-modelled sources): `indicator`, `sub_indicator` (severity/self-harm/suicidal-thoughts/service-use files only), `sex`, `phn_code`, `phn_name`, `age_band`, `metric_name`, `unit`, `value`. Covers all 31 official Australian PHNs.

Full derivation, verified row counts, and known limitations: `notebooks/01_data_ingestion_wa.ipynb` (§H1.5).

## Current status

- **Phase 1 — Discovery: complete.** Problem statement, scope, stakeholder analysis, business requirements, and data-source mapping (`docs/01`–`06`) are drafted and stable.
- **Phase 1.5 — Initiation: complete.** `docs/initiation/` adds the formal delivery-governance pack (business case, project charter, stakeholder and risk registers, requirements/epics, current/future state, and governance & communications plan) that authorises and scopes Phase 2/3.
- **Phase 2/3 — Delivery: in progress.** Sprint 1 (Epic H1, data ingestion) is complete and verified. `reports/` and the remaining `docs/07`–`09` files are still labelled stubs matching the plan below.

### Roadmap

Dates use Australian day/month/year format.

| Sprint | Dates | Focus | Status |
|---|---|---|---|
| 1 | 13/07/2026 – 26/07/2026 | Data ingestion parsers (National/State + PHN-modelled schemas) | ✅ Complete (all of H1.1–H1.5, delivered within week 1 of the sprint) |
| 2 | 27/07/2026 – 09/08/2026 | Treatment-gap computation (H1.4/H1.5 already done — see Sprint 1) | Not started |
| 3 | 10/08/2026 – 23/08/2026 | Regional/demographic comparative reporting, priority-population thresholds | Not started |
| 4 | 24/08/2026 – 06/09/2026 | Barrier analysis, gap analysis & solution-requirements docs, report drafting | Not started |
| 5 | 07/09/2026 – 20/09/2026 | Final report, executive summary, documentation pass | Not started |

Full work-item breakdown, hour estimates, and planning assumptions: `docs/initiation/09_delivery_plan_sprints.md`.

## Project initiation pack

`docs/initiation/` holds the formal delivery-governance pack described above. This pack builds on — and does not replace — the discovery documents in `docs/01`–`06`; each initiation document cites which parts are confirmed from the existing analysis versus newly drafted.

## Intended audience

- Health system decision makers involved in policy, commissioning, and service planning.
- Recruiters and hiring managers evaluating ICT Business Analyst capability in healthcare and analytics contexts.
- Analysts, students, and practitioners interested in hybrid BA/data workflows for public sector problem-solving.

## Future extensions

Authorised for this delivery (Business Case Option 1, see `docs/initiation/04_business_case.md`): gap analysis, solution requirements, use cases, and a recommendation report — the roadmap above. These extend the repository from a problem-definition case study into a fuller end-to-end BA artefact showing how evidence can support service planning and equity-focused decisions in healthcare.

Deliberately **not** authorised yet: an interactive dashboard (Business Case Option 2). Logged as a stretch goal, not committed — the current plan finishes the static report first and revisits the dashboard decision only once that's delivered and validated.