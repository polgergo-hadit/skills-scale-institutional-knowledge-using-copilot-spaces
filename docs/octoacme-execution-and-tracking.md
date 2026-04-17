# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

## Workflows
- Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)

## Quality & Testing
- Unit tests for new logic — owned by **Developers**
- Integration tests where applicable — owned by **Developers** and **QA/Test Engineer**
- End-to-end smoke tests for critical flows before release — owned by **QA/Test Engineer**
- Security scanning in CI — findings triaged by **Security Lead** in partnership with Developers
- Manual QA for feature acceptance — owned by **QA/Test Engineer**; sign-off required before items move to "Done"

> The QA column on the project board represents work actively being validated by the QA/Test Engineer. Items in QA must not be counted as "Done" until the QA/Test Engineer confirms acceptance criteria are met.

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation
- Level 1: Team-level triage in daily standup — **Developers** and **QA/Test Engineer** flag blockers; **Engineering Manager / Tech Lead** resolves technical blockers
- Level 2: **PM** escalates to **Product Lead** and dependent teams; **Security Lead** engaged for security-related blockers; **Release Manager** notified if the blocker threatens a release window
- Level 3: **Sponsor-level** escalation for business-impacting issues — **PM** escalates to **Stakeholder / Executive Sponsor** with impact summary and options

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly
