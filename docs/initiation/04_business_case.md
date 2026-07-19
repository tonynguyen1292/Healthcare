# Business Case

*Corresponds to item B. Fully net-new — no equivalent exists in the repo. Written using the Problem Statement/CR and Risk Register above as inputs, per the build sequence.*

## Executive summary
WA lacks a clear, region-comparable view of where the mental health treatment gap is worst. Existing national/modelled datasets can answer this, but sit unprocessed. This business case recommends completing the originally-scoped Phase 2/3 work (data ingestion → treatment-gap analysis → recommendation report) as the MVP, with an interactive dashboard treated as a deliberately deferred stretch option rather than bundled into the same delivery — directly to avoid the scope-creep risk (R-06) already identified.

## Problem / opportunity
See `03_problem_statement_change_request.md`. In short: strong discovery, zero delivery. The opportunity is low-cost relative to most health-data initiatives — the hardest part (framing the problem, mapping stakeholders and requirements to data sources) is already done to a high standard; what's missing is executing the already-planned analysis.

## Strategic alignment
[INFERRED] Aligns with WA and national mental health policy priorities around equitable access, particularly for rural/remote communities — a long-standing, publicly documented policy concern in WA (regional health access generally, and mental health specifically). [TO BE CONFIRMED against any specific current WA Health or Mental Health Commission strategic plan if this is ever run as a real engagement; no such document is currently referenced in the repo.]

## Current state summary
Discovery complete (`docs/01`–`06`). No data processed. No report exists. Repository has been dormant for ~3 weeks (last commit 2026-06-27). This is a portfolio-stage case study, not a funded or sponsored initiative — see R-07.

## Options considered

| Option | Description | Effort (indicative, solo/part-time) | Pros | Cons |
|---|---|---|---|---|
| **0 — Do nothing** | Leave the repo at current discovery-only state | None | Zero further cost; existing docs already demonstrate BA framing capability | Never answers the actual question the project set out to answer; `notebooks/`/`data_processed/`/`reports/` remain empty indefinitely; weakest portfolio signal (documents intent, not delivery) |
| **1 — Static report only (recommended)** | Execute the originally-planned Phase 2/3: ingest and clean the three NSMHW sources, compute treatment-gap metrics nationally/by state/by PHN, produce `07_gap_analysis.md`, `08_solution_requirements.md`, the three planned notebooks, `data_processed/wa_treatment_gap_summary.csv`, and the recommendation + executive-summary reports | Medium — bounded, uses only tools already in the repo's plan (Python/notebooks, no new infrastructure) | Directly closes the actual gap this project exists to close; demonstrates full BA→DA→output lifecycle; matches existing scope docs exactly, no re-scoping needed | Static output only — no live/updatable view |
| **2 — Static report + interactive dashboard** | Everything in Option 1, plus a dashboard (per README's "potential future extension" and `03_dashboard_spec.md` placeholder) | High — new tooling/hosting decision, materially larger scope | Strongest possible portfolio artifact if completed; matches PHN planners' likely preference for an explorable view over a static PDF | Directly triggers R-06 (discovery/scope creep instead of finishing); no dashboard tooling decision has been made yet; risks repeating the JobSearchCopilot/WA_Mining pattern of an unexecuted "stretch" layer |
| **3 — Ongoing monitoring capability** | Productionise this into a continuously updated regional mental health monitoring tool | Very high — real infrastructure, data refresh pipeline, likely real sponsorship required | Only option with genuine ongoing decision-support value | Entirely disproportionate to current project maturity and resourcing; not a credible next step from where the repo is today |

## Recommended option
**Option 1 — Static report only**, with Option 2 (dashboard) explicitly logged as a Phase 4 stretch goal, not committed. This mirrors the discipline already applied elsewhere in this portfolio: ship the smallest real, complete thing before adding a stretch layer. Rationale: the project's own README already scoped Phase 2/3 this way before any dashboard idea appeared; re-scoping upward now, with zero data work done, is the single biggest risk to this project ever reaching a finished state (R-06).

## Expected benefits
- A genuinely evidence-based, WA-specific view of the mental health treatment gap by region — the thing every stakeholder in the register actually asked for.
- Converts five strong but static discovery documents into a demonstrable, reproducible analytical output — closing the credibility gap between "well-documented" and "delivered."
- Directly usable portfolio evidence of BA→PO→delivery lifecycle ownership, not just requirements-writing.

## Expected costs
No dollar budget applies — this is unsponsored, solo, part-time delivery (consistent with `../02_scope_and_assumptions.md`'s exclusion of "detailed economic modelling"). Indicative effort: data ingestion/cleaning (3 datasets, moderate complexity given `.xlsx` multi-table format) → metric computation → report drafting. [TO BE CONFIRMED: actual hours once Phase 2 begins; no estimate currently exists in the repo.]

## Risks
See `02_risk_register.md` in full. Most relevant to this recommendation: R-01 (modelled-estimate uncertainty), R-02 (small-cell suppression may limit planned granularity), R-06 (scope creep risk if Option 2 is pursued prematurely).

## Dependencies
- Successful extraction/parsing of the `.xlsx` tables inside `data_raw/*.zip` (not yet attempted).
- Resolution of R-02 (confirm what granularity the source data actually supports) before BR-03's priority-population analysis can be finalised.
- No external dependency — no other team, system, or approval currently blocks starting Phase 2.

## Success measures / KPIs
- `data_processed/wa_treatment_gap_summary.csv` exists and is populated (binary — currently not met).
- All three planned notebooks (`01_data_ingestion_wa`, `02_treatment_gap_analysis`, `03_barrier_analysis`) exist and run end-to-end.
- Recommendation report identifies at least 2 priority regions/populations with linked evidence (per BR-03/BR-04 acceptance criteria, already defined in `../04_business_requirements.md`).
- [Portfolio KPI] A reviewer (recruiter/hiring manager) can trace a single finding from raw data → notebook → processed table → report claim without gaps.

## Recommendation
Approve Option 1 as the immediate delivery target. Do not commit to Option 2 (dashboard) until Option 1 is fully delivered and its findings validated.

## Approval considerations
[TO BE CONFIRMED — no real sponsor currently exists, see R-07] In a real engagement, this would need sign-off from WA Dept of Health/Mental Health Commission and WAPHA (both scored High/High in the Stakeholder Register) before public-facing publication, given the sensitivity flagged in R-03 and R-08.
