# OctoAcme — Role Handoffs Checklist

This checklist covers the key handoff points across the OctoAcme project lifecycle. At each phase transition, the outgoing and incoming owners should run through the relevant section together and confirm all items are complete before the next phase begins.

---

## Handoff 1 — Initiation → Planning

**Outgoing owner:** Project Manager / Product Manager
**Incoming owner:** Full project team (Developers, QA, UX, Security Lead, Technical Writer, SRE)

### Checklist

- [ ] Project charter / one-pager is approved by Stakeholder / Executive Sponsor
- [ ] Business goals, success metrics, and out-of-scope items are documented and shared
- [ ] Key stakeholders identified and agreed communication cadence established
- [ ] High-level timeline and milestone dates agreed with Stakeholder and PM
- [ ] Initial risk register created (at least top 3–5 risks with owners)
- [ ] Security Lead briefed on project scope; initial compliance/regulatory requirements noted
- [ ] All required roles confirmed and assigned (refer to the [responsibility matrix](octoacme-responsibility-matrix-template.md))
- [ ] Access to relevant tools and repositories granted to team members
- [ ] Kick-off meeting scheduled and agenda shared

**Sign-off required from:** PM, PdM, Stakeholder/Executive Sponsor

---

## Handoff 2 — Planning → Execution

**Outgoing owner:** Project Manager / Product Manager
**Incoming owner:** Developers, QA/Test Engineer, UI/UX Designer

### Checklist

- [ ] Backlog is refined, prioritized, and sized for the first sprint/iteration
- [ ] Acceptance criteria defined for all items in the first sprint
- [ ] UX designs and assets are ready and shared for items entering development
- [ ] Test plan and test strategy documented and reviewed with QA
- [ ] Threat model and security requirements documented by Security Lead
- [ ] CI pipeline configured (tests, linting, security scanning)
- [ ] Deployment environments (staging, production) confirmed ready by SRE
- [ ] Definition of Done agreed and shared with the team
- [ ] Documentation plan agreed with Technical Writer (scope, owner, timeline)
- [ ] Communication cadence confirmed (standups, demos, syncs)
- [ ] Risk register reviewed and assigned owners confirmed

**Sign-off required from:** PM, EM/Tech Lead

---

## Handoff 3 — Execution → Release

**Outgoing owner:** Developers, QA/Test Engineer, Security Lead
**Incoming owner:** Release Manager, SRE/Operations, Technical Writer

### Checklist

#### Engineering Readiness
- [ ] All planned features implemented, PRs merged, and CI is green
- [ ] No open critical or high defects (or exceptions documented and accepted by PM/PdM)
- [ ] Code reviewed and approved per team policy
- [ ] Feature flags configured correctly for the release (if applicable)

#### Quality Readiness
- [ ] QA sign-off provided: all acceptance criteria verified
- [ ] Regression test suite passing
- [ ] Smoke tests prepared and verified on staging
- [ ] Known issues documented with agreed mitigations or deferral decisions

#### Security Readiness
- [ ] Security scan results reviewed; no open critical/high findings (or exceptions approved by Security Lead)
- [ ] Security Lead sign-off provided
- [ ] Secrets/credentials rotated or confirmed valid for production

#### Documentation Readiness
- [ ] User-facing documentation updated and reviewed by Technical Writer
- [ ] Release notes drafted (changes, known issues, migration steps)
- [ ] Internal runbooks updated (deployment steps, rollback procedure)

#### Infrastructure Readiness
- [ ] Deployment window scheduled and communicated by Release Manager
- [ ] Staging deployment verified by SRE
- [ ] Rollback plan documented and tested where feasible
- [ ] Monitoring and alerting configured for new features/services

**Sign-off required from:** QA/Test Engineer, Security Lead, Technical Writer, SRE, Release Manager

---

## Handoff 4 — Release → Retrospective

**Outgoing owner:** Release Manager, SRE/Operations
**Incoming owner:** Project Manager, full team

### Checklist

#### Post-Release Confirmation
- [ ] Production deployment verified (post-deploy smoke tests passed)
- [ ] Release announcement sent to stakeholders and support teams
- [ ] Success metrics baseline recorded (errors, latency, usage dashboards)
- [ ] On-call schedule confirmed for the post-release monitoring window
- [ ] Any incidents during release documented with timeline and impact

#### Retrospective Preparation
- [ ] Retrospective scheduled within one week of release
- [ ] PM has collected feedback from team members before the retro (async input encouraged)
- [ ] Open action items from previous retrospective reviewed for status
- [ ] Release metrics and quality data compiled for review

#### Knowledge Transfer
- [ ] Post-mortem completed if any incidents occurred during release (owned by SRE/Release Manager)
- [ ] Updated runbooks and documentation committed to the repository
- [ ] Lessons learned captured from Security Lead, QA, SRE for retro discussion
- [ ] Stakeholder / Executive Sponsor notified of release outcome and key metrics

#### Closure
- [ ] Project board updated to reflect released items
- [ ] Any deferred issues or follow-on work added to the backlog with appropriate priority
- [ ] Risk register closed or transitioned to ongoing operations team

**Sign-off required from:** PM, Release Manager, SRE

---

## General Guidance

- Each handoff should be reviewed synchronously (even if brief) between the outgoing and incoming owners.
- Incomplete items must be addressed before the next phase begins, or explicitly accepted with documented risk by PM or EM.
- Use this checklist alongside the [responsibility matrix](octoacme-responsibility-matrix-template.md) to confirm ownership is clear at each step.
- If a handoff is blocked, escalate immediately per the escalation path in [`octoacme-execution-and-tracking.md`](octoacme-execution-and-tracking.md).
