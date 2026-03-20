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

## Deployment Checklist
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Announce release to stakeholders and support

## Release Readiness Checklist

Before any release goes to production, verify the following:

- [ ] All planned features are behind feature flags or fully validated in staging
- [ ] Monitoring and alerting configured for new functionality (dashboards, error budgets, PagerDuty rules)
- [ ] Communications plan drafted: who is notified, via which channel, and when
- [ ] Support team briefed on new features and known edge cases; runbook or FAQ updated
- [ ] Rollback procedure documented and tested in staging (not just described)
- [ ] Release notes reviewed and approved by PM / PdM
- [ ] Go/no-go sign-off obtained from Release Manager and QA Lead (see [RACI](./octoacme-decision-log-and-raci.md))

## Change Management

Significant releases that affect users, operators, or downstream systems require a lightweight change management plan:

1. **Stakeholder Communications**: Identify impacted stakeholders using the [RACI](./octoacme-decision-log-and-raci.md). Send release notices at least 24 hours before production deployment for non-trivial changes; 5 business days for breaking changes.
2. **Release Notes Distribution**: Share finalized release notes via the agreed channel (e.g., GitHub Release, team Slack channel, email). Tag the Customer Success Manager (CSM) if user-facing changes are included.
3. **Training / Enablement**: For features requiring behavior change, create or update onboarding materials (e.g., short video, updated docs, FAQ). Coordinate with the CSM and support team to ensure readiness before launch.
4. **Post-release Confirmation**: Confirm stakeholders have received communications and that support channels are staffed for the first 24–48 hours post-release.

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
