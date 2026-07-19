# High-Level Requirements / Epics / Capabilities

*Corresponds to item F. Business Requirements below are [CONFIRMED] and already fully specified with rationale + acceptance criteria in `../04_business_requirements.md` — referenced, not duplicated. Everything else in this document is [NET NEW], extending that existing analysis-requirements set into the fuller taxonomy and a delivery-shaped epic list.*

## 1. Business Requirements (existing — referenced)

| ID | Title | Priority | Source |
|---|---|---|---|
| BR-01 | WA treatment gap overview | High | `../04_business_requirements.md` |
| BR-02 | Regional treatment gap insights | High | same |
| BR-03 | Priority populations and barrier profiling | Medium | same |
| BR-04 | Decision-ready recommendations | High | same |
| BR-05 | Transparent, reusable analytical workflow | Medium | same |

## 2. User Requirements (net new)

| ID | As a... | I need... | So that... | Priority | Open questions |
|---|---|---|---|---|---|
| UR-01 | State health planner | A WA-vs-national/state comparison view | I can justify investment priorities to leadership | High | None |
| UR-02 | PHN planner | PHN-level treatment-gap metrics | I can commission services in my catchment | High | Does PHN naming match consistently across all 3 source archives? [OPEN] |
| UR-03 | Community NGO representative | Evidence of unmet need in specific communities | I can support advocacy for community-based supports | Medium | What granularity survives suppression rules (R-02)? |
| UR-04 | GP / primary care provider | A short, non-technical summary | I understand local referral pressure without reading the full report | Low | None |
| UR-05 | Analyst / student | Documented, reproducible notebooks | I can learn from and reuse the method | Medium | None |

## 3. Functional Capabilities (net new)

| ID | Title | Description | Rationale | Priority | Source |
|---|---|---|---|---|---|
| FC-01 | Data ingestion & cleaning | Parse multi-sheet `.xlsx` workbooks from all 3 `data_raw/*.zip` archives into structured, analysis-ready tables | Nothing currently exists past raw zips | High | New |
| FC-02 | Treatment-gap computation | Derive gap metric (need − service use) at national/state/PHN level | Core analytical output the whole project exists to produce | High | BR-01, BR-02 |
| FC-03 | Comparative visualisation | Generate WA-vs-benchmark and PHN-comparison charts/tables | Needed for decision-friendly presentation (BR-01 acceptance criteria) | High | BR-01, BR-02 |
| FC-04 | Priority-population/region identification | Rank/flag regions and groups with high need + low service use | Directly required by BR-03 | Medium | BR-03 |
| FC-05 | Recommendation generation | Link findings to concrete, stakeholder-owned recommendations | Required by BR-04 | High | BR-04 |

## 4. Non-Functional Requirements (net new)

| ID | Title | Description | Priority | Source |
|---|---|---|---|---|
| NFR-01 | Reproducibility | Notebooks run end-to-end from raw data with no undocumented manual steps | High | BR-05 |
| NFR-02 | Aggregation floor | No output presents data at finer granularity than the source's built-in suppression threshold | High | R-02 |
| NFR-03 | Sensitive-content handling | Self-harm/suicidality reporting follows a documented safe-messaging style | High | R-03. [GAP] No style guide currently referenced in repo — needs sourcing (e.g. a recognised safe-reporting guideline) before Phase 3 |
| NFR-04 | Traceability | Every claim in the final report traces to a specific processed-data artifact | Medium | BR-05 |
| NFR-05 | Currency labelling | Every output states data vintage prominently (2020–2022 survey / 2024 publication) | High | R-04 |

## 5. Reporting / Analytics Requirements (net new)

| ID | Title | Description | Priority | Source |
|---|---|---|---|---|
| RA-01 | Benchmark table/chart | WA vs. national and vs. at least one other state | High | BR-01 |
| RA-02 | PHN comparison view | Treatment-gap ranking across WA PHNs | High | BR-02 |
| RA-03 | Demographic breakdown | Age/sex splits where source tables allow | Medium | BR-03 |
| RA-04 | Executive summary | 1–2 page, non-technical | High | BR-04, UR-04 |
| RA-05 | *(Stretch — not authorised by current charter)* Interactive dashboard | Explorable version of RA-01–03 | Deferred | Business Case Option 2 |

## 6. Security / Privacy Requirements (net new)

| ID | Title | Description | Priority | Source |
|---|---|---|---|---|
| SP-01 | Aggregate data only | No individual/unit-record data used at any point | High (hard constraint) | `../02_scope_and_assumptions.md` |
| SP-02 | No re-identification attempts | Suppressed/small-cell data is not manipulated to infer values | High | R-02 |
| SP-03 | Public-repo hygiene | Published notebooks/code contain nothing beyond already-public source data | Medium | Portfolio context |
| SP-04 | Non-endorsement disclaimer | Public-facing outputs state this is independent analysis, not an official publication of any named organisation | High | R-08 |

## 7. Integration / Data Requirements (net new)

| ID | Title | Description | Priority | Source |
|---|---|---|---|---|
| ID-01 | Multi-workbook parsing | Handle 17 + 8 + 9 `.xlsx` tables across 3 archives with differing internal layouts | High | Confirmed via direct inspection of `data_raw/` |
| ID-02 | Geographic key alignment | Standardise PHN/state identifiers across National, State/Territory, and PHN-modelled sources | High | [OPEN QUESTION] not yet verified whether naming is consistent |
| ID-03 | External system integration | None required for Option 1 (static report) | N/A | Explicitly out of scope — unlike JobSearchCopilot's Adzuna API dependency, this project has no live external data dependency |

## 8. Epic List (delivery backlog — net new)

Maps the capabilities above into buildable increments for Phase 2/3, per the Project Charter's authorised scope (Option 1 only; Epic H7 is logged but not authorised).

| Epic | Covers | Authorised by charter? |
|---|---|---|
| **H1 — Data Ingestion & Processing Pipeline** | FC-01, ID-01, ID-02 | Yes |
| **H2 — Treatment-Gap Metric Computation** | FC-02 | Yes |
| **H3 — Regional & Demographic Comparative Reporting** | FC-03, RA-01–03 | Yes |
| **H4 — Priority Population & Barrier Analysis** | FC-04, BR-03 | Yes |
| **H5 — Recommendation Report & Executive Summary** | FC-05, RA-04, BR-04 | Yes |
| **H6 — Documentation & Reproducibility** | NFR-01, NFR-04, BR-05 | Yes |
| **H7 — Interactive Dashboard** *(stretch)* | RA-05 | **No — Business Case Option 2, not current charter scope** |

Suggested build order: H1 → H2 → H3 → H4 → H5, with H6 (documentation) running continuously rather than as a discrete final step, matching how `docs/` has already been maintained well throughout discovery.
