# OctoAcme — Project Planning

## Purpose
Turn an approved initiative into an actionable plan and backlog for delivery.

## Objectives
- Break work into shippable increments
- Identify dependencies and risks
- Align timelines, releases, and responsibilities

## Activities
1. Kickoff meeting with stakeholders and delivery team
2. Create prioritized backlog with acceptance criteria
3. Estimate scope (T-shirt sizing or story points)
4. Define Definition of Done (DoD)
5. Identify dependencies and integration points
6. Create release plan and milestone map

## Backlog Item Template
- Title:
- Description:
- Acceptance criteria:
- Priority:
- Estimate:
- Owner:
- Related docs/links:

## Definition of Ready (DoR)

A backlog item is **Ready** to be pulled into a sprint when all of the following are true:

- [ ] Clear, testable acceptance criteria are written
- [ ] All dependencies are identified (internal and external)
- [ ] The item is sized / estimated (T-shirt size or story points)
- [ ] An owner / assignee is identified
- [ ] Test notes or a test approach are included (even if brief)
- [ ] Design or UX notes are attached (if UI/API changes are involved)
- [ ] The item is small enough to complete within one sprint; if not, it has been split

> **Tip**: If an item does not meet DoR at sprint planning, return it to the backlog for refinement before pulling it in.

## Definition of Done (DoD)

An item is **Done** when all of the following are satisfied:

- [ ] All acceptance criteria are met and verified
- [ ] Unit tests written and passing (coverage meets team standard)
- [ ] Integration / end-to-end tests updated where applicable
- [ ] Code reviewed and approved per team PR policy
- [ ] Security scan passes (no new high/critical findings unaddressed)
- [ ] Observability: logs, metrics, or alerts added/updated for new behavior
- [ ] Documentation updated (user-facing docs, API docs, or internal runbooks)
- [ ] Rollout considerations documented (feature flags, phased rollout, or N/A noted)
- [ ] Demo or walkthrough completed with PM / PdM (for significant features)
- [ ] Release notes entry drafted

> **Note**: DoD applies to every item regardless of size. If a criterion is not applicable, note why.

## Sprint / Iteration Planning
- Timebox planning to agreed sprint length
- Pull only items that meet the **Definition of Ready (DoR)** (see above)
- Confirm items can be completed and meet the **Definition of Done (DoD)** (see above) within the sprint
- Ensure team capacity is respected

## Risk & Dependency Management
- Capture in Risk Register:
  - ID, Description, Impact, Probability, Owner, Mitigation
- Mark cross-team dependencies in the project board and escalate during weekly syncs

## Planning Checklist
- [ ] Project kickoff held
- [ ] Backlog prioritized and estimated
- [ ] Release timeline and milestones agreed
- [ ] Definition of Done documented
- [ ] Initial test plan / QA approach drafted
