# OctoAcme — Responsibility Matrix Template

This template provides a RACI-style view of how OctoAcme roles map to key activities across the project lifecycle. Copy this template for each project and adjust assignments as needed.

**RACI Key:**
- **R** — Responsible (does the work)
- **A** — Accountable (owns the outcome; approves)
- **C** — Consulted (provides input before / during)
- **I** — Informed (notified of outcome)

> Role abbreviations used in the matrix:
> PM = Project Manager | PdM = Product Manager | Dev = Developer(s) | EM = Engineering Manager/Tech Lead |
> QA = QA/Test Engineer | UX = UI/UX Designer | RelM = Release Manager | SecL = Security Lead |
> TW = Technical Writer | SRE = SRE/Operations/Platform Engineer | Stk = Stakeholder/Executive Sponsor

---

## Phase 1 — Initiation

| Activity | PM | PdM | Dev | EM | QA | UX | RelM | SecL | TW | SRE | Stk |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Define problem statement & business goals | C | A/R | I | C | I | C | I | I | I | I | A |
| Identify stakeholders and sponsors | R | C | I | I | I | I | I | I | I | I | A |
| Draft project charter / one-pager | A/R | C | I | C | I | I | I | C | I | I | C |
| Initial security and compliance review | I | C | I | C | I | I | I | A/R | I | C | I |
| Approve project charter | C | C | I | I | I | I | I | I | I | I | A |

---

## Phase 2 — Planning

| Activity | PM | PdM | Dev | EM | QA | UX | RelM | SecL | TW | SRE | Stk |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Define scope, milestones, and release plan | A/R | C | C | C | C | C | C | I | I | I | I |
| Backlog creation and refinement | C | A/R | C | C | C | C | I | I | I | I | I |
| Define acceptance criteria | C | A | R | C | C | C | I | I | I | I | I |
| UX research and wireframes | I | C | C | I | I | A/R | I | I | I | I | I |
| Test strategy and test plan | C | I | C | C | A/R | I | C | C | I | I | I |
| Threat modeling and security requirements | C | C | C | C | I | I | I | A/R | I | C | I |
| Infrastructure and deployment planning | C | I | C | A/C | I | I | C | C | I | A/R | I |
| Documentation plan | I | I | I | I | C | C | C | I | A/R | I | I |
| Risk register (initial) | A/R | C | C | C | C | I | C | C | I | C | I |

---

## Phase 3 — Execution

| Activity | PM | PdM | Dev | EM | QA | UX | RelM | SecL | TW | SRE | Stk |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Feature implementation | I | C | A/R | C | C | C | I | I | I | I | I |
| Code review | I | I | A/R | A/C | I | I | I | C | I | I | I |
| UI implementation and design review | I | C | R | C | I | A/C | I | I | I | I | I |
| Automated testing and CI | I | I | C | C | A/R | I | I | C | I | C | I |
| Security scanning and finding triage | I | I | C | C | I | I | I | A/R | I | I | I |
| Draft documentation | I | C | C | I | C | C | I | I | A/R | I | I |
| Risk register updates | A/R | C | C | C | C | I | C | C | I | C | I |
| Blocker escalation (Level 1 & 2) | A/R | C | R | C | C | I | I | C | I | I | I |
| Blocker escalation (Level 3 — business impact) | C | C | I | I | I | I | I | I | I | I | A/R |

---

## Phase 4 — Release

| Activity | PM | PdM | Dev | EM | QA | UX | RelM | SecL | TW | SRE | Stk |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Pre-release gate review | C | C | C | C | C | I | A/R | C | C | C | I |
| QA sign-off | I | I | I | I | A/R | I | C | I | I | I | I |
| Security sign-off | I | I | I | C | I | I | C | A/R | I | I | I |
| Documentation sign-off | I | C | I | I | C | I | C | I | A/R | I | I |
| Deployment to production | I | I | R | C | I | I | A/C | I | I | A/R | I |
| Go/no-go decision | C | C | I | C | C | I | A | C | I | C | I |
| Release announcement | C | C | I | I | I | I | R | I | R | I | I |
| Sponsor / executive notification | C | C | I | I | I | I | C | I | I | I | A/R |
| Post-deploy monitoring | I | I | C | C | I | I | C | C | I | A/R | I |
| Rollback decision and execution | C | C | C | C | I | I | A/C | C | I | R | I |

---

## Phase 5 — Retrospective & Continuous Improvement

| Activity | PM | PdM | Dev | EM | QA | UX | RelM | SecL | TW | SRE | Stk |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Retrospective facilitation | A/R | C | C | C | C | C | C | I | I | I | I |
| Action item ownership assignment | A/R | C | C | C | C | C | C | C | C | C | I |
| Post-release documentation updates | I | C | C | I | C | C | I | I | A/R | I | I |
| Incident post-mortem (if applicable) | C | I | C | C | C | I | C | C | I | A/R | I |
| Security retrospective findings | I | I | C | C | I | I | I | A/R | I | C | I |
| Success metrics review | C | A/R | I | I | I | I | I | I | I | I | C |

---

## Notes for Teams

- A given project may not require all roles; mark unused roles as N/A and note the reason.
- No activity should have more than one **A** — if conflict arises, escalate to PM or EM to clarify.
- This matrix should be reviewed and agreed on at project kick-off and updated if roles change mid-project.
- See [`octoacme-roles-and-personas.md`](octoacme-roles-and-personas.md) for full role descriptions and interaction details.
- See [`octoacme-role-handoffs-checklist.md`](octoacme-role-handoffs-checklist.md) for handoff checklists between phases.
