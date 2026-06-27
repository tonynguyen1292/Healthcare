# Data Sources and Analytical Questions

## 1. Purpose

This document links business requirements to specific analytical questions and data sources used in the Mental Health Treatment Gap in Western Australia project.

It ensures that each dataset and analysis step serves a clear stakeholder need and contributes to the project’s objectives and success criteria.

---

## 2. Core Data Sources

The following datasets are stored in `data_raw/` as read‑only inputs.

1. **Mental-health-tables-National.zip**  
   - National‑level tables from the National Study of Mental Health and Wellbeing (NSMHW).  
   - Provides prevalence estimates and service use indicators for Australia overall.

2. **Mental-health-tables-State-and-territory.zip**  
   - State/territory breakdowns of mental health prevalence and service use.  
   - Used to compare Western Australia with other jurisdictions.

3. **Modelled-estimates-from-NSMHW-by-PHN.zip**  
   - Modelled estimates of mental health need and service use by Primary Health Network (PHN).  
   - Enables regional analysis within Western Australia, aligned with PHN planning boundaries.

Additional contextual sources (e.g. reports on rural access barriers and community mental health supports) are used to interpret quantitative findings and strengthen recommendations.

---

## 3. Analytical Questions by Business Requirement

### BR‑01: WA treatment gap overview

**Key analytical questions**

- Q1.1: What proportion of people in Western Australia are estimated to have a 12‑month mental disorder, and how does this compare to Australia overall and other states/territories?  
- Q1.2: What proportion of people with a 12‑month mental disorder in WA report consulting a health professional for their mental health, and how does this compare nationally?  
- Q1.3: What is the estimated treatment gap (need minus service use) for WA, expressed as a count and/or proportion?

**Primary data sources**

- State and territory tables from NSMHW (`Mental-health-tables-State-and-territory.zip`).
- National summary tables (`Mental-health-tables-National.zip`).

---

### BR‑02: Regional treatment gap insights

**Key analytical questions**

- Q2.1: What are the estimated prevalence of mental disorders and service use by PHN, with focus on PHNs covering WA?  
- Q2.2: How do treatment gap indicators vary across WA PHNs (e.g. metropolitan vs more rural/remote regions)?  
- Q2.3: Which PHNs within WA show relatively high need combined with relatively low service use?

**Primary data sources**

- PHN‑level modelled estimates (`Modelled-estimates-from-NSMHW-by-PHN.zip`).
- Where available, remoteness or metro/rural classifications linked to PHN boundaries.

---

### BR‑03: Priority populations and barrier profiling

**Key analytical questions**

- Q3.1: How do mental health need and service utilisation differ by age group and sex within WA and its PHNs, based on available tables?  
- Q3.2: Are there demographic or regional combinations (e.g. younger adults in certain PHNs) where treatment gaps appear particularly large?  
- Q3.3: What contextual evidence suggests that financial, geographic, or system‑level barriers are driving observed gaps in these groups or regions?

**Primary data sources**

- Any demographic breakdowns (age, sex) included in state/territory and PHN tables.
- External reports and studies on rural/remote access, cost barriers, and service availability.

---

### BR‑04: Decision‑ready recommendations

**Key analytical questions**

- Q4.1: Based on the quantitative findings, which regions and population groups should be considered priority targets for investment or new service models?  
- Q4.2: What types of interventions (e.g. increased outreach, telehealth expansion, community‑based supports) align with the barrier patterns observed?  
- Q4.3: How can the project’s findings be summarised in a concise, decision‑friendly way for different stakeholder groups?

**Primary data sources**

- Synthesised outputs from analyses addressing Q1.x–Q3.x (tables, charts, summary metrics).
- Contextual evidence and existing planning frameworks used by WA health agencies and PHNs.

---

### BR‑05: Transparent, reusable analytical workflow

**Key analytical questions**

- Q5.1: How can the data ingestion, cleaning, and transformation steps be documented so that other analysts can reproduce WA treatment gap metrics?  
- Q5.2: How should notebooks and processed datasets be structured to clearly reflect the hybrid BA/data workflow?  
- Q5.3: How can analysis steps be linked back to business requirements and stakeholder questions?

**Primary data sources**

- All raw and processed datasets, plus notebooks in `/notebooks` and documentation in `/docs`.

---

## 4. Data Processing and Outputs

Data from the sources above will be transformed into:

- Cleaned, analysis‑ready tables stored in `data_processed/` (e.g. `wa_treatment_gap_summary.csv`).
- Exploratory and analytical notebooks in `notebooks/` documenting ingestion and analysis steps.
- Summary tables and visualisations embedded in `reports/` to support recommendations.

Processing steps will be described in `06_solution_approach.md` and referenced within notebooks.

---

## 5. Limitations

- Some PHN or demographic breakdowns may be unavailable or too aggregated for fine‑grained local analysis.
- Privacy protections and modelling assumptions may restrict small‑area insights, particularly in remote communities.
- Data vintages may not fully reflect post‑pandemic changes in need or service patterns, but are considered sufficient for illustrative planning purposes.