# OctoAcme Project Management Docs

This folder centralizes OctoAcme's project management process documentation. It serves as the single source of truth for delivery workflows, roles, and best practices—making knowledge searchable, version-controlled, and reusable across teams. Use these docs to onboard new teammates, reference process guidance during delivery, and provide context to GitHub Copilot Spaces.

## How to Use These Docs

1. **New to OctoAcme?** Start with the [Project Management Overview](octoacme-project-management-overview.md) and [Roles & Personas](octoacme-roles-and-personas.md).
2. **Starting a project?** Follow [Project Initiation](octoacme-project-initiation.md) → [Project Planning](octoacme-project-planning.md).
3. **In active delivery?** Refer to [Execution & Tracking](octoacme-execution-and-tracking.md) and [Risks & Communication](octoacme-risks-and-communication.md).
4. **Releasing?** Use the [Release & Deployment Guide](octoacme-release-and-deployment.md).
5. **Wrapping up a sprint or project?** See [Retrospective & Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md).

## Project Management Process Overview

OctoAcme's project management follows a lightweight end-to-end lifecycle built around customer value, iterative delivery, clear ownership, and data-informed decisions. Work moves through **Initiation → Planning → Execution/Tracking → Release/Deployment → Retrospective/Continuous Improvement**, with each phase producing simple, shareable artifacts:

- **Project one-pager / charter** — problem statement, goals, stakeholders, high-level timeline
- **Prioritized backlog** — user stories with acceptance criteria and a Definition of Done
- **Risk register** — identified risks with impact/likelihood assessment, owner, and mitigation plan
- **Release notes** — summary of changes, known issues, and rollback plan
- **Retrospective actions** — a short list of owned, trackable improvement items

### Personas & Roles

| Role | Primary Responsibility |
|---|---|
| **Project Manager (PM)** | Coordinates timelines, risks, meetings, and cross-team communications |
| **Product Manager (PdM)** | Defines outcomes, prioritizes backlog, measures success |
| **Developers** | Implement features; own testability, maintainability, and code reviews |
| **QA/Testing** | Validates acceptance criteria and release readiness |
| **Stakeholders** | Provide inputs and approvals at key decision gates |

### Communication Cadence & Escalation

- **Daily standups** — progress, blockers, dependencies
- **Weekly delivery sync** — PM + PdM alignment; risk and dependency review
- **Monthly stakeholder updates** — milestone progress and decisions needed
- **Escalation path:** Team triage → PM → Product Lead → Sponsor (security incidents follow the security incident runbook)

### Quality Assurance & Release Readiness

OctoAcme treats quality as a continuous requirement: unit tests for new logic, integration tests where appropriate, and end-to-end smoke tests for critical flows—all enforced by CI (tests, linting, security scans). A release is ready when acceptance criteria are met, CI is green, release notes are drafted, and rollback/mitigation planning is complete. Staged deployment with smoke tests precedes production rollout and stakeholder announcements.

## Process Docs Index

| Document | Description |
|---|---|
| [Project Management Overview](octoacme-project-management-overview.md) | Principles, roles, key artifacts, and lifecycle at a glance |
| [Project Initiation](octoacme-project-initiation.md) | Kickoff checklist, one-pager template, stakeholder alignment |
| [Project Planning](octoacme-project-planning.md) | Scope, milestones, backlog setup, Definition of Done |
| [Execution & Tracking](octoacme-execution-and-tracking.md) | Sprint/iteration workflow, project board, PR practices |
| [Risks & Communication](octoacme-risks-and-communication.md) | Risk register format, escalation paths, status templates |
| [Release & Deployment](octoacme-release-and-deployment.md) | Release checklist, deployment steps, post-deploy verification |
| [Retrospective & Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md) | Retro format, action tracking, improvement culture |
| [Roles & Personas](octoacme-roles-and-personas.md) | Detailed responsibilities and communication norms per role |

## Key Artifacts Quick Reference

| Artifact | Where to find / create it |
|---|---|
| Project one-pager / charter | Project repo root; template in [Project Initiation](octoacme-project-initiation.md) |
| Sprint/iteration backlog | Project board; guidance in [Project Planning](octoacme-project-planning.md) |
| Definition of Done | Agreed by team; reference in [Project Planning](octoacme-project-planning.md) |
| Risk register | Maintained by PM; format in [Risks & Communication](octoacme-risks-and-communication.md) |
| Release notes | Drafted pre-release; process in [Release & Deployment](octoacme-release-and-deployment.md) |
| Retro action items | Captured post-sprint; tracked in [Retrospective & Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md) |
