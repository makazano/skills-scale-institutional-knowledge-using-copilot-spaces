# OctoAcme — Decision Log & RACI Guide

## Purpose
Capture significant project decisions and clarify who is responsible for what. Use this document to reduce ambiguity, prevent revisiting settled decisions, and give new team members fast context.

## When to Use
- Any decision that affects scope, architecture, timeline, or team structure.
- Any decision that is non-obvious, involves trade-offs, or may be questioned later.
- Staffing or vendor choices, major technical designs, release strategies.

---

## Decision Log Template

Copy this block for each decision. Store the log in your project repo or link it from your Project Charter.

```
| Field               | Details |
|---------------------|---------|
| Date                | YYYY-MM-DD |
| Decision ID         | DEC-NNN |
| Decision            | One-sentence statement of what was decided |
| Context             | Why this decision was needed; background |
| Options Considered  | Option A — brief description; Option B — brief description |
| Chosen Option       | Option A (or B, etc.) |
| Owner               | Name / role accountable for this decision |
| Stakeholders        | Names / roles consulted or informed |
| Impact              | Scope / timeline / cost / risk impact |
| Follow-up Actions   | Who does what by when as a result of this decision |
```

### Example Decision Log Entry

| Field               | Details |
|---------------------|---------|
| Date                | 2025-06-15 |
| Decision ID         | DEC-001 |
| Decision            | Adopt feature flags for all new features in the Q3 release |
| Context             | The team needs to decouple deployment from release to reduce release-day risk |
| Options Considered  | Option A — feature flags via LaunchDarkly; Option B — maintain separate release branches |
| Chosen Option       | Option A — feature flags via LaunchDarkly |
| Owner               | Release Manager |
| Stakeholders        | PM, Tech Lead, QA Lead, Operations Engineer |
| Impact              | Minor increase in configuration overhead; significant reduction in rollback risk |
| Follow-up Actions   | Tech Lead to add LaunchDarkly SDK by 2025-06-22; PM to update Release Plan |

---

## RACI Template

RACI defines who is **R**esponsible, **A**ccountable, **C**onsulted, and **I**nformed for each activity.

| Role           | Definition |
|----------------|-----------|
| **Responsible** | Does the work. One or more people. |
| **Accountable** | Ultimately owns the outcome. Exactly one person per activity. |
| **Consulted**   | Provides input before or during the work. Two-way communication. |
| **Informed**    | Kept up-to-date on progress/outcomes. One-way communication. |

### RACI Table Template

```
| Activity / Decision    | PM | PdM | Dev | QA Lead | Release Mgr | Ops Eng | CSM | Stakeholders |
|------------------------|----|-----|-----|---------|-------------|---------|-----|--------------|
| Activity 1             |    |     |     |         |             |         |     |              |
| Activity 2             |    |     |     |         |             |         |     |              |
| Activity 3             |    |     |     |         |             |         |     |              |
```

Fill each cell with **R**, **A**, **C**, or **I** (leave blank if no involvement).

### Worked Example — Release Planning

| Activity / Decision          | PM | PdM | Dev | QA Lead | Release Mgr | Ops Eng | CSM | Stakeholders |
|------------------------------|----|-----|-----|---------|-------------|---------|-----|--------------|
| Define release scope         | C  | A   | C   | C       | R           | I       | C   | I            |
| Approve release go/no-go     | C  | C   | I   | C       | A           | R       | I   | C            |
| Execute deployment           | I  | I   | R   | I       | A           | R       | I   | I            |
| Communicate release to users | R  | C   | I   | I       | C           | I       | A   | I            |
| Conduct post-release review  | A  | C   | R   | R       | C           | R       | C   | I            |

---

## Guidance: Referencing Decisions and RACI from Other Docs

- **Project Charter / One-pager**: Reference the RACI table so stakeholders know who owns what from day one.
- **Sprint / Iteration Planning** (see [octoacme-project-planning.md](./octoacme-project-planning.md)): Link to the relevant Decision Log entry when a story is shaped by a previous decision.
- **Release Plan** (see [octoacme-release-and-deployment.md](./octoacme-release-and-deployment.md)): Include the Release Manager and Ops Engineer from the RACI in the release readiness checklist.
- **Status Reports** (see [octoacme-status-and-risk-templates.md](./octoacme-status-and-risk-templates.md)): Reference open decision IDs in the "Decisions Needed" section.
- **Retrospectives**: Review the Decision Log to check if decisions held up; add learnings to the log if useful.

Keep the Decision Log and RACI in the project's `/docs` folder or in a dedicated wiki page, and link from the top-level `README.md` for discoverability.
