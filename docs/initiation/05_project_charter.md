# Project Charter / PID — WA Mental Health Treatment Gap

*Corresponds to item C. Net-new. Formalises what the Business Case recommended (Option 1) into a scoped, governed initiative.*

| Field | Value |
|---|---|
| **Project title** | The Mental Health Treatment Gap in Western Australia |
| **Sponsor** | [TO BE CONFIRMED — no real sponsor exists; project is self-directed] |
| **Product Owner / BA** | Vy Nguyen |
| **Delivery approach** | Solo/part-time, iterative — one analyst executing BA and DA roles across a single sequential phase plan (not a multi-person Agile team). **Secondary priority as of 21/07/2026** — WA_Mining is the primary commitment; this project proceeds at reduced (~4 hrs/week) capacity. Sprint 2's start date remains a firm commitment regardless — see Milestones and `08_governance_communication_plan.md`. |

## Background
See `03_problem_statement_change_request.md` and `04_business_case.md`. Discovery phase complete; this charter authorises Phase 2/3 delivery (Business Case Option 1).

## Objectives
1. Quantify the WA mental health treatment gap nationally, by state, and by PHN. *(= `../01_problem_statement.md` objective 1–2)*
2. Identify priority regions/populations with the largest unmet need. *(= objective 3)*
3. Produce decision-ready recommendations linked to evidence. *(= objective 4)*
4. Deliver a reproducible, documented analytical workflow. *(= BR-05)*

## Scope
As per `03_problem_statement_change_request.md` §Initial scope — national/state/PHN aggregate analysis, descriptive breakdowns by geography and basic demographics, summary outputs (tables, charts, recommendation report). This charter authorises **Business Case Option 1 only.**

## Out of scope
As per `03_problem_statement_change_request.md` §Out of scope, plus: any dashboard/interactive tooling (Business Case Option 2) is explicitly **not** authorised by this charter and requires a separate charter amendment if pursued later.

## Deliverables
- `docs/07_gap_analysis.md`, `docs/08_solution_requirements.md`, `docs/09_use_cases.md` (already named in README roadmap)
- `notebooks/01_data_ingestion_wa.ipynb` ✅ done, `02_treatment_gap_analysis.ipynb`, `03_barrier_analysis.ipynb`
- `data_processed/national_state_indicators.csv` + `phn_modelled_indicators.csv` ✅ done (Sprint 1); a combined `wa_treatment_gap_summary.csv` is a Sprint 2 (Epic H2) output computed from these
- `reports/01_findings_and_recommendations.md`, `02_executive_summary.md`

## Milestones

Dates use Australian day/month/year format. Sprint 1 runs 13/07/2026–26/07/2026 — anchored to the Monday of the week delivery actually started, not the following Monday, so milestone claims stay chronologically consistent with the calendar rather than claiming work finished before its own sprint window began.

| Milestone | Deliverable | Target | Status |
|---|---|---|---|
| M0 | This initiation pack (`docs/initiation/`) | — | **Complete** |
| M1 | Data ingestion notebook + `data_processed/` populated | End of Sprint 2 (week 4, by 09/08/2026) | **Complete — delivered 19/07/2026**, within week 1 of Sprint 1, well ahead of target (H1.4/H1.5 completed alongside H1.1-H1.3 rather than split across two sprints) |
| M2 | Treatment-gap and barrier-analysis notebooks complete | End of Sprint 2, by 09/08/2026 | **Committed start date 27/07/2026 for Sprint 2** — target completion unchanged, not started |
| M3 | `07_gap_analysis.md` + `08_solution_requirements.md` drafted | End of Sprint 6, by 04/10/2026 (revised — see below) | Not started |
| M4 | Recommendation report + executive summary published | End of Sprint 8, by 01/11/2026 (revised — see below) | Not started |

**Revised 21/07/2026**: M3 and M4 target dates extended from the original plan (previously 06/09/2026 and 20/09/2026) to reflect this project's new secondary-priority status behind WA_Mining — capacity dropped from ~7 hrs/week to ~4 hrs/week, so the same 74-hour scope now spans 8 sprints instead of 5. M1 and M2's targets are unaffected: M1 is already done, and Sprint 2's 27/07/2026 start is a firm commitment regardless of the reduced pace. See `09_delivery_plan_sprints.md` for the full revised sprint-by-sprint breakdown and `08_governance_communication_plan.md` for the stakeholder communication formalising this change.

## Assumptions
See `03_problem_statement_change_request.md` §Assumptions (carried forward unchanged).

## Constraints
- Solo, part-time delivery; no dedicated data engineering, design, or governance support.
- **Secondary priority behind WA_Mining as of 21/07/2026** — ~4 hrs/week available, down from the original ~7 hr/week assumption (R-09).
- No budget; free/open tooling only (Python notebooks, markdown docs — consistent with what's already in the repo).
- Source data granularity may not support every breakdown BR-03 wants (R-02).

## Dependencies
As per `04_business_case.md` §Dependencies.

## Governance
See `08_governance_communication_plan.md` for cadence and escalation detail. Summary: Product Owner/BA holds sole delivery authority given no sponsor currently exists; any future real sponsor engagement would sit above this role per the Stakeholder Register's High/High entries.

## RAID Summary

| Type | ID | Description | Owner | Status |
|---|---|---|---|---|
| Risk | R-01 to R-09 | See `02_risk_register.md` in full | PO/BA | Open (8), Accepted (1) — 9 risks total |
| Assumption | A-1 | Modelled NSMHW estimates are reliable enough for cross-region comparison | PO/BA | Accepted, per `../02_scope_and_assumptions.md` |
| Assumption | A-2 | Treatment gap (need − service use) is a reasonable, if imperfect, proxy for unmet need | PO/BA | Accepted with caveat (R-05) |
| Assumption | A-3 | PHN/remoteness classifications adequately capture metro/rural access differences | PO/BA | Accepted, pending Phase 2 validation |
| Issue | I-1 | No named sponsor exists, weakening formal governance authority of this charter | PO/BA | Open — accepted as a structural feature of a self-directed case study (R-07) |
| Issue | I-2 | Discovery documentation risked outpacing actual delivery | PO/BA | Resolved for Sprint 1 (real data processing shipped, R-06 partially mitigated); same discipline still required every remaining sprint |
| Dependency | D-1 | Successful parsing of multi-table `.xlsx` source files | PO/BA | Open, blocks M1 |
| Dependency | D-2 | Resolution of small-cell suppression limits before finalising BR-03 granularity | PO/BA | Open, blocks M2–M3 |

## Approval required
[TO BE CONFIRMED] In a real engagement: Dept of Health / Mental Health Commission and WAPHA sign-off before any public-facing publication (per Stakeholder Register). For the current self-directed case study, approval is self-authorised by the PO/BA — logged here explicitly rather than left implicit, per R-07.
