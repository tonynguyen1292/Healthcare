# LinkedIn post draft

*Plain text below is written for direct copy-paste into LinkedIn (no markdown syntax will render there). Repo confirmed publicly visible before linking.*

---

Turning a self-directed case study into a properly scoped delivery initiative this week — sharing what that looked like end to end.

The project: quantifying the mental health treatment gap in Western Australia — the difference between how many people need care and how many actually get it — using national survey data (ABS National Study of Mental Health and Wellbeing) at state and Primary Health Network level.

The discovery work was already solid: problem statement, stakeholder analysis, business requirements, data source mapping. What was missing was everything a real delivery initiative needs to actually start — a business case with a genuine options analysis (including "do nothing"), a project charter, stakeholder and risk registers, and requirements broken into an actual backlog.

A few things I'd call out as the real BA/PO work here, not just paperwork:

- Resequenced the standard document order — built the risk register before the business case, because for health data, risk should gate scope commitments, not follow them.
- Before estimating any delivery work, I opened the actual source files rather than estimating from folder names. Found two genuinely different data schemas hiding under one dataset, which changed the engineering estimate materially.
- Recommended against the more exciting option (an interactive dashboard) in favour of finishing the originally-scoped static report first — deliberately avoiding scope creep before the core analysis is even proven out.

Net result: a 5-sprint, ~10-week delivery plan with hour-level estimates per work item, the repo restructured to match it, and the backlog exported ready for Jira.

What's next, sprint by sprint:
Sprint 1-2 — data ingestion pipeline for the raw survey tables
Sprint 2 — treatment-gap computation, with statistical uncertainty carried through, not dropped
Sprint 3 — regional and demographic comparative reporting
Sprint 3-4 — priority-population and barrier analysis
Sprint 4-5 — final recommendation report and executive summary

Repo (public, work in progress): github.com/tonynguyen1292/Healthcare

Built this planning phase with AI-assisted tooling to move fast from repo audit to sprint plan — happy to talk through the process with anyone curious about it.

#BusinessAnalysis #ProductOwner #HealthcareAnalytics #WesternAustralia #MentalHealth #Agile #DataAnalytics #ICTBA
