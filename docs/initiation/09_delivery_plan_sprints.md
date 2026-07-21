# Delivery Plan — Timeline, Sprints, Work Items

*Extends the initiation pack beyond the original A–H document set, per direct request. Fills the `[TO BE CONFIRMED: target dates]` placeholder left in `05_project_charter.md`'s milestone table. Scope = Business Case Option 1 (static report) only, per Charter authorisation — Epic H7 (dashboard) is not included.*

## Planning assumptions [state these explicitly — adjust and re-run the math if wrong]

- **This project is now secondary to WA_Mining (confirmed 21/07/2026).** Vy's primary time commitment sits elsewhere; Healthcare gets whatever's left. Capacity assumption revised down accordingly — see below. This is Risk R-09 (`02_risk_register.md`) moving from a hypothetical to an active, confirmed constraint.
- **Solo delivery, ~4 hours/week** (revised down from the original ~7hr midpoint, using the lower end of the sensitivity range already published below) given secondary-project status. Still a working assumption, not confirmed capacity.
- **2-week sprints** — unchanged. Keeping the cadence stable rather than stretching sprint length keeps the review rhythm predictable even though less gets done per sprint.
- Estimates below are grounded in the actual data structure inspected directly — two distinct parser schemas, uncertainty data (RSE/MoE/RRMSE/CI) present and to be carried through, messy multi-row publication headers.
- No workshops/stakeholder validation time is budgeted — this is solo, self-directed delivery per the Governance Plan; the "workshop" items from the initiation pack are logged as open gaps, not scheduled work.
- **Sprint 2's start date (27/07/2026) is a firm commitment, not just a plan** — see `08_governance_communication_plan.md` for the stakeholder communication formalising this. Starting on time is achievable regardless of reduced capacity; what changes is how much fits in each sprint thereafter, not whether Sprint 2 begins on schedule.

## Work items by epic (hours are point estimates, not padded)

### Epic H1 — Data Ingestion & Processing Pipeline
| Item | Description | Est. (hrs) |
|---|---|---|
| H1.1 | Parser for National/State-style tables (`.1 Estimates`/`.2 RSE`/`.3 Proportions`/`.4 MoE`, multi-row merged headers) | 5 |
| H1.2 | Parser for PHN-modelled-style tables (Males/Females/Persons + methodology sheets — different schema) | 4 |
| H1.3 | Verify and standardise geographic keys (PHN/state naming) across all 3 sources — resolves the open question in `06_requirements_epics_capabilities.md` (ID-02) | 2 |
| H1.4 | Output standardised long/tidy format to `data_processed/` | 2 |
| H1.5 | Data-quality checks: row counts, null/suppressed-cell handling (R-02) | 2 |
| **Subtotal** | | **15** |

### Epic H2 — Treatment-Gap Metric Computation
| Item | Description | Est. (hrs) |
|---|---|---|
| H2.1 | National/state-level gap (need % − service-use %) | 3 |
| H2.2 | PHN-level gap from modelled tables | 3 |
| H2.3 | Attach uncertainty bounds (RSE/MoE, RRMSE/CI) to every computed gap figure — R-01 mitigation, not a stretch goal | 3 |
| **Subtotal** | | **9** |

### Epic H3 — Regional & Demographic Comparative Reporting
| Item | Description | Est. (hrs) |
|---|---|---|
| H3.1 | WA vs. national/other-state benchmark table + chart (RA-01) | 3 |
| H3.2 | PHN comparison view, uncertainty-aware (don't rank PHNs as confidently different when CIs overlap) (RA-02) | 4 |
| H3.3 | Age/sex demographic breakdown where source allows (RA-03) | 3 |
| **Subtotal** | | **10** |

### Epic H4 — Priority Population & Barrier Analysis
| Item | Description | Est. (hrs) |
|---|---|---|
| H4.1 | Define and apply a priority threshold (high need + low service-use, uncertainty-adjusted); document as an analytical judgment call since no workshop validation is scheduled | 4 |
| H4.2 | Contextual barrier narrative, drawing on the existing AS-IS pain-points doc | 3 |
| **Subtotal** | | **7** |

### Epic H5 — Recommendation Report & Executive Summary
| Item | Description | Est. (hrs) |
|---|---|---|
| H5.1 | Draft `docs/07_gap_analysis.md` (already named in README roadmap) | 3 |
| H5.2 | Draft `docs/08_solution_requirements.md` | 3 |
| H5.3 | Draft `reports/01_findings_and_recommendations.md` + `02_executive_summary.md` | 5 |
| H5.4 | Safe-messaging review pass on any self-harm/suicidality content (NFR-03) before finalising | 1 |
| **Subtotal** | | **12** |

### Epic H6 — Documentation & Reproducibility
| Item | Description | Est. (hrs) |
|---|---|---|
| H6.1 | Notebook documentation/cleanup pass | 3 |
| H6.2 | Update README status/roadmap to reflect actual completion | 1 |
| H6.3 | Draft `docs/09_use_cases.md` (named in README roadmap, not yet written) | 2 |
| **Subtotal** | | **6** |

**Raw total: 59 hours.** With a ~25% contingency for the rework that always shows up in real data work (a header format that doesn't match assumptions, a metric that needs recomputing) → **~74 hours planned.**

## Sprint plan (revised 21/07/2026 — 8 sprints total at ~4 hrs/week, secondary-project pace)

Dates use Australian day/month/year format. Sprint 1 ran at full pace before the secondary-project change (it's the only sprint not subject to the revised ~4hr/week assumption, which is why it delivered 15 hours of work in one window rather than the ~8 hours the new pace implies per sprint). Sprint 2 onward assumes ~8 hours of capacity per 2-week sprint.

| Sprint | Dates | Contents | Hours | Status | Sprint goal / Definition of Done |
|---|---|---|---|---|---|
| **1** | 13/07/2026 – 26/07/2026 | H1.1, H1.2, H1.3, H1.4, H1.5 (all of Epic H1) | 15 | ✅ Complete, delivered within week 1 (by 19/07/2026) | `data_processed/national_state_indicators.csv` + `phn_modelled_indicators.csv` populated with verified row counts — **Charter Milestone M1 closes here** |
| **2** | 27/07/2026 – 09/08/2026 | H2.1, H2.2, H2.3 (all of Epic H2) | 9 | **Committed start date — see stakeholder communication in `08_governance_communication_plan.md`** | Treatment-gap metrics computed with uncertainty bounds attached — **Charter Milestone M2 closes here** |
| **3** | 10/08/2026 – 23/08/2026 | H3.1, H3.2 | 7 | Not started | Benchmark table/chart and PHN comparison view complete |
| **4** | 24/08/2026 – 06/09/2026 | H3.3, H4.1 | 7 | Not started | Demographic breakdown complete; priority-population threshold applied — Epic H3 closes here |
| **5** | 07/09/2026 – 20/09/2026 | H4.2, H5.1 | 6 | Not started | Barrier narrative drafted; `07_gap_analysis.md` drafted — Epic H4 closes here |
| **6** | 21/09/2026 – 04/10/2026 | H5.2, H5.3 | 8 | Not started | `08_solution_requirements.md` and both report drafts exist — **Charter Milestone M3 closes here** |
| **7** | 05/10/2026 – 18/10/2026 | H5.4, H6.1, H6.2, H6.3 | 7 | Not started | Safe-messaging review complete, notebooks documented, README current — Epics H5 and H6 close here |
| **8** | 19/10/2026 – 01/11/2026 | Contingency buffer | ~11 available | Not started | Absorbs rework from unknowns hit in Sprints 2–7 — **Charter Milestone M4 closes here, project done** |

Epics are now spread thinner across more, smaller sprints rather than several epics per sprint — a direct consequence of ~8 hours of capacity per sprint instead of ~14. Buffer is concentrated in Sprint 8 rather than spread evenly, same reasoning as the original plan: early sprints hit unknowns that create rework demand later.

## Total time estimate

**Revised: ~15 weeks from today (21/07/2026) to project completion (01/11/2026), across 8 sprints — Sprint 1 already done, 7 more at ~4 hrs/week.** This is roughly 5 weeks longer than the original ~10-week estimate, directly reflecting the secondary-project capacity reduction, not new scope — total hours (74 with contingency) are unchanged from the original plan.

Sensitivity — same 74-hour scope at different weekly capacity (unchanged from original publication, still holds):
| Weekly capacity | Total duration |
|---|---|
| 4 hrs/week (current assumption) | ~18–19 weeks total |
| 7 hrs/week (original assumption, before secondary-project change) | ~10 weeks total |
| 10 hrs/week | ~7–8 weeks total |

## Solo-delivery ceremony adaptation

Per `08_governance_communication_plan.md` (no team cadence required for solo delivery): each sprint gets a short self-written planning note (what/why, 10 min) and a short retro note at close (what worked, what to adjust for the next sprint's estimates). This is lightweight by design, but keep the written record — it's genuine evidence of iterative delivery discipline for the same portfolio audience the Stakeholder Register already names.
