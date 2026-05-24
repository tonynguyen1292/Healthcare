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
├─ data_raw/               # Source datasets and zipped files (read-only)
│  ├─ Mental-health-tables-National.zip
│  ├─ Mental-health-tables-State-and-territory.zip
│  └─ Modelled-estimates-from-NSMHW-by-PHN.zip
├─ data_processed/         # Cleaned / transformed data for analysis
├─ notebooks/              # Exploratory and analytical notebooks / scripts
├─ docs/                   # BA documentation (problem, scope, requirements, etc.)
├─ reports/                # Final analyses and recommendation reports
├─ .gitignore
└─ README.md
```

## Key documentation

- `docs/01_problem_statement.md` – defines the core problem, objectives, and success criteria.
- `docs/02_scope_and_assumptions.md` – clarifies boundaries, in‑scope/out‑of‑scope items, and key assumptions.
- `docs/03_stakeholder_analysis.md` – outlines stakeholder groups and their information needs.
- `docs/04_business_requirements.md` – captures business needs and high‑level requirements. (will be commited once reviewed)
- `docs/05_data_sources_and_questions.md` – links data sources to analytical questions. (will be commited once reviewed)
- `docs/06_solution_approach.md` – describes the analytical and technical approach. (will be commited once reviewed)
- `reports/` – will contain the final findings and recommendations. (will be commited once reviewed)

## Current status

- Phase 1: Problem definition and initial documentation drafted.
- Phase 2 (planned): Data ingestion, cleaning, and exploratory analysis for WA and comparison regions.
- Phase 3 (planned): Visualisation, synthesis, and generation of recommendations.

## Intended audience

- Health system decision makers (government, PHNs, NGOs).
- Data and business leaders interested in health equity and service planning.
- Recruiters and hiring managers evaluating hybrid BA / data roles.

## Future extensions

Potential extensions include:

- Interactive dashboards for WA mental health treatment gaps (by region and demographic).
- Scenario analysis for funding or workforce distribution.
- Deeper focus on specific populations (e.g. young people, Aboriginal communities) where data allows. 