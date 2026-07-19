# Delivery Plan — Timeline, Sprints, Work Items

*Extends the initiation pack beyond the original A–H document set, per direct request. Fills the `[TO BE CONFIRMED: target dates]` placeholder left in `05_project_charter.md`'s milestone table. Scope = Business Case Option 1 (static report) only, per Charter authorisation — Epic H7 (dashboard) is not included.*

## Planning assumptions [state these explicitly — adjust and re-run the math if wrong]

- **Solo delivery**, ~6–8 hours/week (midpoint 7 used below). This is a working assumption, not confirmed capacity — see sensitivity table at the end.
- **2-week sprints** — long enough for a solo, part-time contributor to complete meaningful, demonstrable work each sprint, short enough to keep momentum and catch estimate drift early.
- Estimates below are grounded in the actual data structure inspected directly (see chat response) — two distinct parser schemas, uncertainty data (RSE/MoE/RRMSE/CI) present and to be carried through, messy multi-row publication headers.
- No workshops/stakeholder validation time is budgeted — this is solo, self-directed delivery per the Governance Plan; the "workshop" items from the initiation pack are logged as open gaps, not scheduled work.

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

## Sprint plan (5 sprints × 2 weeks = 10 weeks, at 7 hrs/week)

| Sprint | Weeks | Contents | Hours | Sprint goal / Definition of Done |
|---|---|---|---|---|
| **1** | 1–2 | H1.1, H1.2, H1.3 | 11 | Both parsers run against one sample file each from their respective schemas; geographic keys reconciled |
| **2** | 3–4 | H1.4, H1.5, H2.1, H2.2, H2.3 | 13 | `data_processed/wa_treatment_gap_summary.csv` exists and is populated with uncertainty bounds attached — **Charter Milestone M1 + M2 both close here** |
| **3** | 5–6 | H3.1, H3.2, H3.3, H4.1 | 14 | Benchmark and PHN comparison views complete; priority shortlist drafted |
| **4** | 7–8 | H4.2, H5.1, H5.2, H5.3 | 14 | `07_gap_analysis.md`, `08_solution_requirements.md`, and both report drafts exist — **Charter Milestone M3 closes here** |
| **5** | 9–10 | H5.4, H6.1, H6.2, H6.3, contingency buffer | ~7 used + buffer | Safe-messaging review complete, notebooks documented, README current — **Charter Milestone M4 closes here, project done** |

Buffer is deliberately concentrated in Sprint 5 rather than spread evenly — early sprints hit unknowns (a header format that parses differently than expected) that create rework demand later, so back-loading slack is more realistic than pretending every sprint is equally predictable.

## Total time estimate

**~10 weeks at 7 hrs/week (74 hours with contingency), across 5 sprints.**

Sensitivity — same 74-hour scope at different weekly capacity:
| Weekly capacity | Total duration |
|---|---|
| 4 hrs/week | ~18–19 weeks (9 sprints) |
| 7 hrs/week (assumed above) | ~10 weeks (5 sprints) |
| 10 hrs/week | ~7–8 weeks (4 sprints) |

## Solo-delivery ceremony adaptation

Per `08_governance_communication_plan.md` (no team cadence required for solo delivery): each sprint gets a short self-written planning note (what/why, 10 min) and a short retro note at close (what worked, what to adjust for the next sprint's estimates). This is lightweight by design, but keep the written record — it's genuine evidence of iterative delivery discipline for the same portfolio audience the Stakeholder Register already names.
