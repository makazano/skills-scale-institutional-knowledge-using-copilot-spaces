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
- Unit tests for new logic
- Integration tests where applicable
- End-to-end smoke tests for critical flows before release
- Security scanning in CI
- Manual QA for feature acceptance when needed

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation

### Escalation Levels
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

### Escalation Decision Tree

Use the following decision tree when a blocker or risk surfaces:

```
Is the blocker resolved within 1 business day?
├── YES → No escalation needed. Document in standup notes.
└── NO  → Is the blocker within the team's control?
          ├── YES → Escalate to Level 1: raise in next standup;
          │         assign owner and due date.
          └── NO  → Does it affect the release date or business commitments?
                    ├── NO  → Escalate to Level 2: PM notifies Product Lead
                    │         and dependent team leads; add to risk register.
                    └── YES → Escalate to Level 3: PM escalates to Sponsor/
                              Executive with impact summary, options, and
                              recommended action. Log in Decision Log
                              (see octoacme-decision-log-and-raci.md).
```

## WIP Limits & Aging Work Items

Limiting work-in-progress reduces context switching and surfaces bottlenecks earlier.

- **WIP Limit Guidance**: Each team member should have no more than 2 items "In Progress" at any time. The team-level WIP limit for the "In Progress" column should not exceed 1.5× the team size.
- **Aging Thresholds**: Flag items that have been "In Progress" for more than:
  - **3 days** (for items estimated ≤ 2 story points): discuss in standup.
  - **5 days** (for larger items): PM reviews with assignee; consider splitting the item.
  - **7+ days**: automatic escalation topic in weekly delivery sync.
- **Board Hygiene**: Review aging items weekly. Items that haven't moved in 7 days should be reassigned, split, or explicitly blocked/parked.

## Meeting Notes — Lightweight Format

Keep meeting notes short and actionable. Attach them to the relevant GitHub Issue or PR so context is preserved alongside the work.

```markdown
## Meeting Notes — [Meeting Type] — YYYY-MM-DD

**Attendees**: [Names / roles]
**Facilitator**: [Name]

### Decisions Made
- [Decision 1 — link to Decision Log entry if significant]

### Action Items
| Action | Owner | Due Date |
|--------|-------|----------|
|        |       |          |

### Parking Lot / Follow-ups
- [Items deferred to a future meeting or async discussion]
```

**Where to store notes**: Post as a comment on the relevant GitHub Issue, or store in `/docs/meeting-notes/YYYY-MM-DD-[type].md`. Link the note from any related PRs or issues for traceability.

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly
