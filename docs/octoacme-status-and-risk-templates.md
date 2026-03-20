# OctoAcme — Status Report & Risk Register Templates

## Purpose
Provide lightweight, copy-pasteable templates for weekly status reporting and risk tracking. Consistent formats reduce reporting overhead, make status easy to scan, and ensure risks are visible before they become issues.

## When to Use
- **Status Report**: Weekly, or at any stakeholder checkpoint.
- **Risk Register**: Created at project kickoff; updated at least weekly throughout the project lifecycle.

---

## Weekly Status Report Template

Copy this template into your project's status update (GitHub Discussion, wiki page, email, or recurring issue comment).

```markdown
## Status Report — Week of YYYY-MM-DD

**Project**: [Project Name]
**PM**: [Name]
**Status**: 🟢 On Track | 🟡 At Risk | 🔴 Off Track

### Progress This Week
- [Completed item 1]
- [Completed item 2]

### Next Steps (Coming Week)
- [Planned item 1]
- [Planned item 2]

### Key Metrics
| Metric              | Target | Actual | Trend |
|---------------------|--------|--------|-------|
| Stories completed   |        |        |       |
| Open bugs           |        |        |       |
| Test pass rate      |        |        |       |

### Risks & Issues
| ID     | Risk / Issue | Owner | Status |
|--------|-------------|-------|--------|
| RSK-01 |             |       |        |

### Decisions Needed
- [Decision needed from whom, by when, and why it is blocking]

### Notes / Shoutouts
- [Any context, wins, or acknowledgements]
```

---

## Risk Register Table Template

Maintain one risk register per project. Update it at least weekly and review it in the weekly delivery sync.

```markdown
## Risk Register — [Project Name]

Last updated: YYYY-MM-DD

| ID     | Category        | Description                               | Probability | Impact | Score (P×I) | Owner | Mitigation / Contingency         | Status   |
|--------|-----------------|-------------------------------------------|-------------|--------|-------------|-------|----------------------------------|----------|
| RSK-01 | Technical       | [Risk description]                        | H/M/L       | H/M/L  |             |       | [How we reduce/avoid the risk]   | Open     |
| RSK-02 | Schedule        | [Risk description]                        | H/M/L       | H/M/L  |             |       | [How we reduce/avoid the risk]   | Open     |
| RSK-03 | Dependency      | [Risk description]                        | H/M/L       | H/M/L  |             |       | [How we reduce/avoid the risk]   | Mitigated|
| RSK-04 | Resource        | [Risk description]                        | H/M/L       | H/M/L  |             |       | [How we reduce/avoid the risk]   | Closed   |
```

### Risk Scoring Definitions

| Probability | Definition |
|-------------|-----------|
| **H** (High) | Likely to occur (>60%) |
| **M** (Medium) | May occur (20–60%) |
| **L** (Low) | Unlikely (<20%) |

| Impact | Definition |
|--------|-----------|
| **H** (High) | Significant effect on scope, schedule, cost, or quality |
| **M** (Medium) | Moderate effect; manageable with effort |
| **L** (Low) | Minor effect; easily absorbed |

**Score**: Use H/M/L combination — e.g., H×H = critical; L×L = monitor only.

### Example Risk Register Entry

| ID     | Category  | Description                                      | Probability | Impact | Score | Owner | Mitigation                                         | Status |
|--------|-----------|--------------------------------------------------|-------------|--------|-------|-------|----------------------------------------------------|--------|
| RSK-01 | Technical | Third-party API may change before our integration | M           | H      | M×H   | PM    | Pin API version; create adapter layer; monitor changelog | Open |
| RSK-02 | Schedule  | QA resources unavailable during release week      | L           | H      | L×H   | PM    | Pre-book QA calendar; identify backup QA resource  | Open   |

---

## Suggested Cadence

| Artifact       | Frequency        | Owner | Review Forum           |
|----------------|-----------------|-------|------------------------|
| Status Report  | Weekly           | PM    | Stakeholder channel / issue comment |
| Risk Register  | Weekly update    | PM    | Weekly delivery sync   |
| Risk deep-dive | When score rises | PM + Risk Owner | Ad-hoc or sprint review |

## Where to Store Artifacts

- Store status reports as comments on a recurring GitHub Issue (e.g., "Weekly Status — [Project]") or in a `/docs/status/` subfolder.
- Store the Risk Register in `/docs/risk-register.md` or as a GitHub Project board column with labels.
- Link both from the Project Charter and the project `README.md`.
- Cross-reference open risks in the [Decision Log](./octoacme-decision-log-and-raci.md) when a risk triggers a decision.
