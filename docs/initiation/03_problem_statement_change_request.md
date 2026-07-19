# Problem Statement / Change Request

*Corresponds to item A. This does not replace `../01_problem_statement.md` (which remains the canonical background/objectives reference and is [CONFIRMED] strong as-is) — it adds the Change-Request framing your template asks for that the original document didn't need for its original (case-study) purpose.*

## Title
Establishing an evidence base for the WA Mental Health Treatment Gap to inform service planning and commissioning decisions.

## Background
[CONFIRMED, from `../01_problem_statement.md`] Around one in five Australians experiences a mental disorder in a 12-month period; fewer than half of those access professional help. People in rural/remote WA face similar need but more limited access. National and modelled datasets (NSMHW 2020–2022) exist to quantify this at national, state, and PHN level, but aren't currently packaged in a way that clearly shows planners where the gap is worst.

## Business problem
There is a significant, currently unquantified-for-WA-planning-purposes gap between mental health need and mental health service use, driven by financial, geographic, and system-level barriers. Decision makers lack a clear, WA-specific, region-comparable evidence base to prioritise funding, workforce, and service models.

## Current pain points
- No single, decision-ready view of WA's treatment gap benchmarked against national/other-state figures. [CONFIRMED — this is the explicit gap BR-01 was written to close]
- No regional (PHN) breakdown showing where need and service use diverge most. [CONFIRMED — BR-02]
- No evidence-based shortlist of priority populations/regions for targeted intervention. [CONFIRMED — BR-03]
- Existing raw datasets (`data_raw/`) have not yet been processed into anything usable — `data_processed/`, `notebooks/`, and `reports/` are empty. [CONFIRMED, direct repo inspection]

## Who is impacted
State health policymakers, WAPHA/PHN regional planners, community mental health NGOs, GPs/primary care, and — per this project's dual purpose — the researchers/students and portfolio-evaluator audiences named in the README. Full detail: `01_stakeholder_register.md`.

## Why now
[INFERRED] No externally-imposed deadline exists — this is a self-directed initiative. The practical "why now" is that discovery work is complete and sitting idle (last repo commit 2026-06-27); further delay risks the existing high-quality problem framing going stale without ever producing an output. [TO BE CONFIRMED if a real sponsor/deadline is ever attached.]

## Desired outcome
A decision-ready recommendation report (and possibly a lightweight dashboard — see Business Case §Options) that: quantifies the WA treatment gap overall and by PHN, identifies priority regions/populations, and gives evidence-linked recommendations mapped to responsible stakeholder groups. [CONFIRMED — matches `../01_problem_statement.md` success criteria]

## Initial scope
As defined in `../02_scope_and_assumptions.md` [CONFIRMED]: national/state/PHN-level aggregate analysis using NSMHW and modelled estimates; descriptive breakdown by geography and basic demographics (age, sex); summary tables, charts, and a recommendation report.

## Out of scope
[CONFIRMED, from `../02_scope_and_assumptions.md`]: clinical evaluation of specific treatments; individual/patient-level analysis; detailed cost-effectiveness modelling; implementation planning for specific programs; analysis below the granularity the source data can support.

## Assumptions
[CONFIRMED, from `../02_scope_and_assumptions.md`]: modelled estimates are reliable enough for cross-region comparison; the need-minus-service-use gap is a reasonable (if imperfect) proxy for unmet need; PHN/remoteness classifications adequately capture metro/rural access differences; the 2020–2022 data vintage is a suitable basis for current planning despite lag.

## Open questions
- Is this initiative ever going to be run "as-if commissioned" with a real (simulated) sponsor and approval cadence, or does it stay a self-directed case study? This materially changes how the rest of this pack should be used. [TO BE CONFIRMED]
- Is a dashboard actually wanted, or is a static recommendation report sufficient for the stated audiences? [TO BE CONFIRMED — see Business Case §Options]
- What triggers moving from this initiation pack into actually starting Phase 2 (data ingestion)? [GAP — no current answer; addressed as a hard gate in the Risk Register, R-06]
