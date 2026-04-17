# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## UI/UX Designer

### Role Summary
UI/UX Designers ensure that OctoAcme products are usable, accessible, and visually consistent. They translate user needs and product requirements into wireframes, prototypes, and design specifications that guide engineering implementation.

### Responsibilities
- Conduct user research and usability testing to inform design decisions
- Create wireframes, mockups, and interactive prototypes
- Maintain and evolve the design system and component library
- Review implemented UIs for fidelity to designs and accessibility standards
- Document design decisions and rationale for future reference

### Goals
- Deliver intuitive, accessible interfaces that reduce user friction
- Ensure design consistency across the product
- Provide engineering with clear, unambiguous design specifications

### Typical Communication
- Design reviews and critique sessions with Product Managers and Developers
- Handoff annotations in design tools (e.g., Figma)
- Participation in sprint planning to scope design work alongside engineering tasks

### Interactions
- **Product Managers**: collaborate to translate user stories and product vision into design direction; participate in backlog refinement to clarify acceptance criteria
- **Developers**: provide design specs and assets; review implementations and provide feedback; pair on edge-case and responsive-layout questions
- **Project Managers**: report design task status; flag dependencies or scope changes that affect timelines
- **QA/Test Engineer**: review test cases against design specs to ensure UI acceptance criteria are testable
- **Technical Writer**: coordinate on in-product help text, tooltips, and error messages

---

## Release Manager

### Role Summary
Release Managers own the coordination, scheduling, and execution of OctoAcme releases. They serve as the central point of contact for release planning, gate reviews, and post-release monitoring, ensuring releases are safe, well-communicated, and reversible.

### Responsibilities
- Maintain the release calendar and communicate release windows to all stakeholders
- Run pre-release gate reviews to confirm readiness criteria are met
- Coordinate deployment activities across engineering, QA, and SRE/Operations
- Author and distribute release notes
- Oversee rollback execution and post-incident follow-up when needed

### Goals
- Ship releases on schedule with minimal production incidents
- Ensure every release has a tested rollback plan
- Maintain a clear, auditable record of what changed and when

### Typical Communication
- Release readiness stand-ups in the week before each release
- Release notes and change announcements to stakeholders and support teams
- Incident notifications and status updates during rollback events

### Interactions
- **Project Managers**: align on milestone dates; escalate blockers that threaten release windows
- **Developers**: confirm all PRs are merged and CI is green before release cut-off
- **QA/Test Engineer**: verify sign-off on acceptance criteria and smoke tests before production deploy
- **Security Lead**: confirm security scan results and any required remediations are complete before release
- **SRE/Operations / Platform Engineer**: coordinate deployment windows, environment readiness, and post-deploy monitoring alerts
- **Stakeholder / Executive Sponsor**: provide go/no-go recommendation at release gate; communicate high-impact delays

---

## Technical Writer

### Role Summary
Technical Writers own the accuracy and clarity of user-facing and internal documentation. They partner with engineering, product, and QA to ensure that documentation is complete, correct, and published in sync with feature releases.

### Responsibilities
- Write and maintain end-user guides, API references, and internal runbooks
- Work with Developers and Product Managers to document new features and breaking changes
- Ensure docs are updated before each release and reflected accurately in release notes
- Establish and enforce documentation style standards
- Identify and close documentation gaps discovered during support escalations or retrospectives

### Goals
- Ensure users and teammates can self-serve answers through clear documentation
- Reduce support load caused by missing or outdated documentation
- Keep documentation in sync with the product at every release

### Typical Communication
- Feature doc reviews with Developers and Product Managers before release
- Doc readiness check-ins with Release Manager during pre-release gate
- Style guide updates and shared templates via the docs repository

### Interactions
- **Developers**: interview for technical accuracy; review code-level comments and README updates
- **Product Managers**: align on user-facing language, feature names, and messaging
- **QA/Test Engineer**: review documentation for accuracy by cross-checking against tested acceptance criteria
- **Release Manager**: confirm documentation is ready as part of the release gate checklist
- **UI/UX Designer**: coordinate on in-product copy, tooltips, and onboarding flows

---

## Security Lead

### Role Summary
The Security Lead advises on security requirements, conducts risk assessments, and ensures that OctoAcme's development and release processes comply with security standards. They are the point of escalation for security findings and incidents.

### Responsibilities
- Define and maintain security standards, threat models, and compliance requirements for the project
- Review architecture and code changes that have security implications
- Triage and prioritize findings from automated security scans (SAST, dependency audits)
- Own the security incident runbook and lead response for security-related incidents
- Provide security training and awareness resources for the team

### Goals
- Prevent security vulnerabilities from reaching production
- Ensure all known vulnerabilities are tracked, prioritized, and remediated within agreed SLAs
- Maintain audit-ready security documentation

### Typical Communication
- Security review sign-off as a gate in the release process
- Weekly or per-sprint triage of security scan results with Developers
- Incident notifications and post-mortems for security events

### Interactions
- **Developers**: pair on secure coding practices; review security-sensitive PRs; provide remediation guidance for scan findings
- **Product Managers**: flag security risks that affect product priorities or require scope adjustments
- **Project Managers**: report open security findings as project risks; escalate unresolved issues to appropriate sponsors
- **Release Manager**: provide explicit sign-off (or block) on releases that have open critical/high findings
- **SRE/Operations / Platform Engineer**: collaborate on infrastructure security, secret management, and production monitoring for security events

---

## QA/Test Engineer

### Role Summary
QA/Test Engineers validate that features meet acceptance criteria and are production-ready. They own the test strategy, maintain test automation, and serve as the quality gate before releases.

### Responsibilities
- Develop and maintain the test plan, test cases, and automated test suites
- Execute manual and automated testing across feature and regression scenarios
- Reproduce, document, and verify bugs identified during testing
- Participate in sprint planning and backlog refinement to define testable acceptance criteria
- Provide quality sign-off as a prerequisite for release gate approval

### Goals
- Prevent defects from reaching production
- Maintain a comprehensive and up-to-date automated test suite
- Ensure acceptance criteria are verifiable and tests are aligned with them

### Typical Communication
- QA status updates in sprint reviews and release readiness check-ins
- Bug reports and test result summaries shared with Developers and PM
- Test plan documentation maintained alongside feature specs

### Interactions
- **Developers**: collaborate on acceptance criteria; verify fixes; co-own test automation where applicable
- **Product Managers**: align on what "done" means for each feature; flag edge cases that need acceptance criteria clarification
- **Project Managers**: report testing blockers and quality risks; raise issues that may delay release
- **Release Manager**: provide formal test sign-off before production deployments
- **Security Lead**: coordinate on security-specific test cases (e.g., auth, input validation)
- **UI/UX Designer**: validate UI implementations against design specs and accessibility requirements

---

## Engineering Manager / Tech Lead

### Role Summary
The Engineering Manager (or Tech Lead on smaller teams) provides technical direction and ownership of the engineering team's health, practices, and output. They bridge strategic product goals and day-to-day engineering execution.

### Responsibilities
- Set and uphold technical standards, architecture guidelines, and engineering practices
- Lead technical design reviews and approve significant architectural decisions
- Support career development and performance of engineers
- Remove systemic blockers and address cross-team technical dependencies
- Own technical risk identification and mitigation planning

### Goals
- Maintain a high-quality, sustainable engineering culture
- Ensure technical decisions align with long-term product goals
- Deliver velocity improvements through better tooling, practices, and team health

### Typical Communication
- Technical design reviews and architecture decision records (ADRs)
- 1:1s and team retrospectives for engineering health
- Engineering updates to PM/PdM during planning cycles

### Interactions
- **Developers**: mentor and coach on technical practices; own escalation path for technical blockers
- **Product Managers**: translate technical constraints into product trade-off discussions; negotiate scope and technical debt
- **Project Managers**: provide engineering team capacity and risk inputs for project planning
- **Security Lead**: co-own architecture security reviews and technical remediation plans
- **SRE/Operations / Platform Engineer**: align on reliability requirements, deployment pipelines, and infrastructure standards
- **Release Manager**: approve engineering readiness for releases; escalate significant technical risks

---

## Stakeholder / Executive Sponsor

### Role Summary
Stakeholders and Executive Sponsors provide strategic direction, funding, and decision-making authority for OctoAcme projects. They are engaged at key milestones and escalation points, and are ultimately accountable for project outcomes.

### Responsibilities
- Define and communicate high-level business objectives and success criteria
- Approve project charter, major scope changes, and budget decisions
- Unblock cross-organizational dependencies that escalate above team and PM level
- Receive and review milestone and release updates
- Champion the project within the broader organization

### Goals
- Ensure projects deliver measurable business value
- Make timely, informed decisions at escalation points and decision gates
- Maintain organizational alignment on project priorities

### Typical Communication
- Monthly or milestone-based stakeholder updates from PM/PdM
- Go/no-go decisions at major release and phase gates
- Escalation calls when business-impacting blockers arise

### Interactions
- **Project Managers**: receive status updates, risk summaries, and escalation requests; provide decisions on scope, timeline, and budget
- **Product Managers**: align on roadmap priorities and business impact; approve significant backlog changes
- **Release Manager**: receive go/no-go recommendation; approve or override release gates for business-critical situations
- **Engineering Manager / Tech Lead**: review major technical risks and investment decisions with business impact

---

## SRE/Operations / Platform Engineer

### Role Summary
SRE/Operations and Platform Engineers own the reliability, deployment infrastructure, and observability of OctoAcme systems in production. They partner with development teams to ensure applications are deployable, monitorable, and recoverable.

### Responsibilities
- Design, maintain, and improve deployment pipelines and infrastructure-as-code
- Establish and maintain observability standards (logging, metrics, alerting, tracing)
- Define and track reliability targets (SLOs/SLAs) and error budgets
- Respond to production incidents as on-call engineers; lead or support post-mortems
- Review production readiness of new features and services before release

### Goals
- Achieve and maintain agreed reliability and performance targets
- Minimize mean time to detection (MTTD) and recovery (MTTR) for incidents
- Enable self-service, safe, and auditable deployments for engineering teams

### Typical Communication
- Production readiness reviews before significant releases
- On-call handoffs, incident timelines, and post-mortem reports
- Infrastructure change proposals reviewed with Engineering Manager and Security Lead

### Interactions
- **Developers**: advise on deployment requirements, environment configs, and observability instrumentation
- **Release Manager**: coordinate deployment windows, environment health checks, and rollback procedures
- **Engineering Manager / Tech Lead**: collaborate on infrastructure investments, reliability standards, and on-call health
- **Security Lead**: implement infrastructure security controls; share production access logs and audit trails
- **Project Managers**: flag infrastructure risks or platform changes that may affect project timelines

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- See [`octoacme-responsibility-matrix-template.md`](octoacme-responsibility-matrix-template.md) for a RACI view of how these roles map to project lifecycle activities.
- See [`octoacme-role-handoffs-checklist.md`](octoacme-role-handoffs-checklist.md) for handoff checklists between lifecycle phases.

