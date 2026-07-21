# Communication and Governance Plan

*Corresponds to item H. Fully net-new. Deliberately last in the build sequence — it operationalises the Charter's governance section and the Stakeholder Register's engagement column, so it had nothing to operationalise until those existed.*

## Governance structure
Given no real sponsor currently exists (R-07), governance is intentionally lightweight and honest about that:

| Layer | Who (current reality) | Who (if run as a real engagement) |
|---|---|---|
| Sponsor / approval authority | None — PO/BA self-approves | WA Dept of Health / Mental Health Commission [TO BE CONFIRMED] |
| Steering / review | None | WAPHA + Dept of Health working group [TO BE CONFIRMED] |
| Delivery | Product Owner / BA (Vy Nguyen) — solo | Same, potentially supported by a data analyst if this project ever gains additional contributors |

## Decision forums
[TO BE CONFIRMED if real stakeholders are ever engaged] Proposed cadence *if* this becomes a simulated or real stakeholder engagement: a single findings-review session before publication, rather than an ongoing steering committee — proportionate to project size.

## SteerCo / sponsor cadence
N/A at current governance maturity (no sponsor). If introduced: one review at Charter approval, one at draft-report stage, one at publication sign-off — three touchpoints total, not a recurring meeting series, given project scale.

## Working group cadence
N/A — no working group currently exists. The Stakeholder Register's Medium/High-influence rows (WAPHA, Dept of Health) would be the natural working-group membership if this were activated.

## Delivery team cadence
Solo delivery — no team cadence required. Self-imposed checkpoint: review progress against the Charter's M1–M4 milestones at each work session, since there's no external accountability forcing it.

## Escalation path
1. Data/methodology issue (e.g. suppression blocking a planned breakdown) → resolved by PO/BA directly, logged in `02_risk_register.md`.
2. Sensitive-content judgement call (self-harm/suicidality framing, R-03) → **not** resolved unilaterally — held against NFR-03's safe-messaging standard before any publication; if that standard isn't sourced, publication of those specific findings is blocked until it is.
3. Scope question (e.g. "should we build the dashboard now?") → escalates to a Business Case amendment, not an ad-hoc decision mid-delivery — directly enforces the Charter's Option-1-only authorisation.

## Status reporting approach
Given solo delivery, formal status reports are disproportionate. Recommended lightweight approach: keep the Charter's milestone table (`05_project_charter.md`) up to date as the single source of truth on progress, rather than maintaining a separate status report artifact.

**Exception, applied 21/07/2026**: when a capacity/timeline assumption changes materially (here: this project became secondary to WA_Mining, extending the plan from 5 to 8 sprints), an update-the-table approach isn't enough — stakeholders need an active communication, not a passive document they'd have to go looking for. See `stakeholder_communication_phase2.md` for that specific instance. This is a deliberate, one-off exception to the general policy above, not a reversal of it — routine progress still just lives in the milestone table.

## Stakeholder communication matrix

| Stakeholder | What they receive | When | Channel |
|---|---|---|---|
| Dept of Health / Mental Health Commission | Executive summary + full report | At publication | [TO BE CONFIRMED — no real contact exists] |
| WAPHA / PHN planners | Full report, PHN-level detail emphasised | At publication | [TO BE CONFIRMED] |
| Community NGOs | Executive summary | At publication | [TO BE CONFIRMED] |
| GPs / primary care | Short summary only | At publication | [TO BE CONFIRMED] |
| Researchers / students / portfolio reviewers | Full repo, including notebooks | Continuously (public repo) | GitHub |
| All of the above | Interim commitment update (Sprint 2 start date + revised timeline) | 21/07/2026, ad hoc — triggered by the capacity change, not a recurring cadence | `stakeholder_communication_phase2.md` |

## RAID management approach
Consolidated RAID summary lives in `05_project_charter.md`; the full Risk detail lives in `02_risk_register.md`. No separate RAID log tool — proportionate to project scale; would move to a tracked backlog (GitHub Issues/Projects) if this project ever gains a second contributor.

## Change control approach
Any change to authorised scope (Charter §Scope/Out of scope) — most notably any move toward Business Case Option 2 (dashboard) or Option 3 (ongoing monitoring) — requires a Charter amendment, not an informal decision. This is the single governance rule this plan most wants enforced, directly because R-06 (scope creep instead of finishing Option 1) is rated the highest-priority open risk.
