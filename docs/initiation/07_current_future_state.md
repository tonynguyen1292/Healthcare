# Current State / Future State Process Outline

*Corresponds to item E. AS-IS is [CONFIRMED] and already documented in full in `../06_as-is_process.md` — summarised, not rewritten, below. The To-Be, decision points, escalation points, and process metrics are [NET NEW] — that document explicitly says "a future TO-BE process... [is] not in scope for this initial project phase," which this document now addresses.*

## Current state actors
Individual experiencing symptoms (and their family/friends), GP/primary care, public specialist mental health services, community/NGO mental health services. [CONFIRMED, `../06_as-is_process.md` §2]

## Current workflow summary (AS-IS)
Six-step journey: experience symptoms → decide whether to seek help → first contact (usually GP) → assessment/referral → either engage with specialist/community services, or no service accessed (the treatment gap outcome). Full detail, including pain points at each step, is in `../06_as-is_process.md` — not repeated here.

## Pain points / bottlenecks (summarised from existing doc)
Mental health literacy/stigma at symptom recognition; awareness/cost/stigma at the help-seeking decision; GP shortages and short consultation times at first contact; long waitlists, travel distance, and inconsistent telehealth at referral; workforce shortages and fragmented coordination at engagement.

## Data issues (net new — specific to this project's use of the AS-IS process, not the health system itself)
- The AS-IS process is described at a *system* level from national survey evidence, not from local WA process mapping or stakeholder interviews. [CONFIRMED — the existing doc says this explicitly: "based on high-level patterns reported in national surveys and public evidence rather than detailed local process mapping"]
- No WA-specific process data exists to validate whether this generic AS-IS holds true for, say, remote PHNs specifically versus metro Perth. [GAP — a workshop-validation item, see final deliverables list]

## Future state vision (net new)
This project's "future state" is not a proposal to redesign WA's mental health service pathway (explicitly out of scope — see `03_problem_statement_change_request.md`). It is a future state for **decision-making**: planners and commissioners have a clear, evidence-based, region-specific view of where the AS-IS pathway is failing (Step 6 — no service accessed) most severely, and can target investment accordingly.

## Key process changes (decision-support process, not clinical pathway)
| AS-IS (today) | TO-BE (this project's target state) |
|---|---|
| Planners rely on national-level averages and anecdote to judge where gaps are worst | Planners have a WA/PHN-specific treatment-gap view, benchmarked and ranked |
| No structured link between survey evidence and specific funding/commissioning decisions | Recommendation report explicitly links each priority finding to a responsible stakeholder group (BR-04) |
| Discovery and requirements exist, but no one has actually looked at the data | Data has been ingested, processed, and turned into a decision-ready artifact (Business Case Option 1) |

## Decision points (net new)
1. Which regions/populations qualify as "priority" (FC-04) — a threshold decision the PO/BA currently owns provisionally, [TO BE CONFIRMED] by planner stakeholders in a workshop.
2. Whether findings are published broadly or shared only within the "as-if commissioned" stakeholder group — governance decision, see `08_governance_communication_plan.md`.
3. Whether to proceed to Business Case Option 2 (dashboard) after Option 1 ships — explicitly deferred, not decided now.

## Escalation points (net new)
- Data quality/suppression blocking a planned breakdown (R-02) → escalate to PO/BA to re-scope that specific requirement rather than force an unsupported claim.
- Sensitive-content framing question (R-03) → escalate to an editorial review step before publication (see governance plan) rather than resolved unilaterally mid-analysis.

## Process metrics to track (net new)
- % of planned notebooks/reports actually completed vs. README roadmap (currently 0% for Phase 2/3).
- Time from "data ingested" to "first draft recommendation" (baseline not yet established).
- Number of findings in the final report that trace cleanly to a processed-data artifact (NFR-04) — target: 100%.

## As-Is process flow (text form)
```
Symptom experience
   -> Help-seeking decision (stigma/awareness/cost factors)
       -> First contact (usually GP)
           -> Assessment + possible referral
               -> [Path A] Access specialist/community service -> receive care
               -> [Path B] No service accessed -> TREATMENT GAP (this project's focus)
```

## To-Be process flow (text form — decision-support process, not a clinical redesign)
```
Raw NSMHW data (data_raw/)
   -> Ingestion & cleaning (Epic H1)
       -> Treatment-gap computation, national/state/PHN (Epic H2)
           -> Regional & demographic comparative reporting (Epic H3)
               -> Priority population/region identification (Epic H4)
                   -> Recommendation report, linked to responsible stakeholders (Epic H5)
                       -> [Decision point] Planner/commissioner reviews recommendations
                           -> Targeted investment/commissioning decision (outside this project's scope, but the intended real-world consequence)
```
