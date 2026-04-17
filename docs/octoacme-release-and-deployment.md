# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted
- Rollback / mitigation plan documented
- Smoke tests prepared

**Ownership:**
- **Release Manager** — runs the pre-release gate review and confirms all criteria are met before production deployment
- **QA/Test Engineer** — provides formal quality sign-off confirming acceptance criteria are verified and regression tests pass
- **Security Lead** — confirms security scan results are reviewed; no unresolved critical/high findings; provides security sign-off
- **SRE/Operations / Platform Engineer** — verifies staging environment health, deployment pipeline readiness, and post-deploy monitoring alerts

## Deployment Checklist
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Announce release to stakeholders and support

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - **SRE/Operations / Platform Engineer** triggers incident response, monitors production signals, and executes rollback to last known-good release
  - **Release Manager** notifies stakeholders and coordinates communications during the incident
  - **QA/Test Engineer** verifies the rollback is stable and acceptance criteria still hold after recovery
  - **Security Lead** is engaged if the incident has a security dimension (data exposure, auth failure, etc.)
  - Triage root cause and capture action items in a post-mortem (owned by SRE/Release Manager)

> See [`octoacme-role-handoffs-checklist.md`](octoacme-role-handoffs-checklist.md) for the full release sign-off checklist and post-release handoff steps.

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
