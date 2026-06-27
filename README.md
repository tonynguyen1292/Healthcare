# The Mental Health Treatment Gap in Western Australia

This project analyses the mental health treatment gap in Western Australia, with a focus on how financial barriers, rural and remote access issues, and systemic service limitations contribute to unmet mental health needs. It is designed as a hybrid Business Analysis (BA) and Data Analysis project to demonstrate end-to-end problem framing, data-driven insight generation, and practical recommendations for decision makers.

## Project context

National surveys show that around one in five Australians experiences a mental disorder in a given year, yet less than half of those with a 12‑month mental disorder access professional help for their mental health. Evidence also shows that people living outside major cities have more limited access to mental health services despite similar levels of need. In Western Australia, regional and remote communities experience high distress, lower wellbeing, and ongoing unmet mental health needs. 

This project uses modelled estimates from the National Study of Mental Health and Wellbeing (NSMHW) and related sources to quantify the treatment gap in Western Australia and identify where access barriers are likely to be most acute. 

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
│  ├─ 07_gap_analysis.md               🔲 to commit
│  ├─ 08_solution_requirements.md      🔲 to commit
│  └─ 09_use_cases.md                  🔲 to commit
├─ notebooks/
│  ├─ 01_data_ingestion_wa.ipynb
│  ├─ 02_treatment_gap_analysis.ipynb
│  └─ 03_barrier_analysis.ipynb
├─ reports/
│  ├─ 01_findings_and_recommendations.md
│  ├─ 02_executive_summary.md
│  └─ 03_dashboard_spec.md             
├─ .gitignore
└─ README.md
```

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
`notebooks/` – will contain the exploratory and targeted analytical workflow supporting the case study.

`data_processed/` – will contain cleaned outputs used to quantify treatment gap indicators.

`reports/` – will contain the final findings, recommendations, executive summary, and any dashboard specification.

## Current status

- Phase 1: Problem definition and initial documentation drafted.
- Phase 2 (planned): Data ingestion, cleaning, and exploratory analysis for WA and comparison regions.
- Phase 3 (planned): Visualisation, synthesis, and generation of recommendations.

## Intended audience

- Health system decision makers involved in policy, commissioning, and service planning.
- Recruiters and hiring managers evaluating ICT Business Analyst capability in healthcare and analytics contexts.
- Analysts, students, and practitioners interested in hybrid BA/data workflows for public sector problem-solving.

## Future extensions

Potential extensions include:

- Planned future enhancements include gap analysis, solution requirements, use cases, recommendation reports, and potentially a dashboard specification or interactive visual layer to support decision-making. These additions will extend the repository from a problem-definition case study into a fuller end-to-end BA artefact showing how evidence can support service planning and equity-focused decisions in healthcare.