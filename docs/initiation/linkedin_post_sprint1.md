# LinkedIn post draft — Sprint 1 / deliberate PO-BA approach

*Plain text below for direct copy-paste (no markdown will render on LinkedIn). Contrasts this project's approach with WA_Mining's on purpose, per instruction — this is a career-narrative post to Vy's own network, a different context from the repo-embedded docs (which were deliberately made self-contained, see docs/initiation/02_risk_register.md and related).*

---

I'm building this project differently from my last one, on purpose.

My last portfolio project, WA_Mining, I built as a software engineer: I designed the architecture, wrote the API and frontend, set up CI/CD, wrote the deployment runbook. It's a solid demonstration of build capability. But it's one story, and I have two credentials — I recently passed my ECBA (IIBA), and I wanted a project that actually proves the Business Analyst side, not just states it on a CV.

So for this one — quantifying the mental health treatment gap in Western Australia — I made a deliberate call: no analysis code until the delivery discipline was in place first. Business case with a genuine options analysis (including "do nothing"). Project charter. Stakeholder register. Risk register — built before the business case, specifically, because for health data the risks should shape the scope commitments, not get discovered after. Requirements broken into a real backlog. A governance plan honest about the fact that no real sponsor exists yet.

That's the Product Owner / BA side. Sprint 1 just wrapped, and it's the proof the discipline isn't just paperwork:

I built the data ingestion pipeline against real Australian Bureau of Statistics survey data — not a clean sample dataset, the actual multi-sheet publication format. Two genuinely different table structures hiding under one folder. Three real bugs along the way worth naming rather than glossing over: a header-detection routine that matched a sheet's own description text instead of the real header row, a unit-label parser that misclassified error-margin columns because their labels contain the other metric's keyword, and one source table using different sheet-naming than the other sixteen. All caught, all fixed, all verified against manual spot-checks before I trusted the output.

73,000+ rows extracted, zero nulls, and one detail I like: the pipeline independently found exactly 31 distinct region codes in the data — which is the real, official number of Primary Health Networks in Australia. Nobody told the code that number. It just fell out of correct extraction.

Repos, both public:
WA_Mining — github.com/tonynguyen1292/WA_Mining
Healthcare Treatment Gap — github.com/tonynguyen1292/Healthcare

Next up: Sprint 2, turning this ingested data into the actual treatment-gap metrics.

#BusinessAnalysis #ProductOwner #HealthcareAnalytics #WesternAustralia #DataEngineering #Agile #ICTBA
