# Incident Post-Mortem: [INC-XXXX — Short Summary]

- **Date / Duration:** YYYY-MM-DD | HH:MM – HH:MM UTC (Total: XX mins)
- **Severity:** SEV-1 | SEV-2 | SEV-3
- **Incident Commander:** `@name`
- **Customer Impact:** Describe affected services, error rates, and user impact.

## Timeline (UTC)
| Time | Event |
| :--- | :--- |
| `HH:MM` | Monitoring alert triggered for elevated 5xx error rate |
| `HH:MM` | On-call engineer acknowledged and began triage |
| `HH:MM` | Root cause isolated; mitigation applied |
| `HH:MM` | Service metrics returned to baseline; incident resolved |

## Root Cause Analysis (5 Whys)
1. **Why did the service fail?** ...
2. **Why did that condition occur?** ...
3. **Why wasn't it caught before production?** ...

## What Went Well / What Needs Improvement
- **Went Well:** Fast alert detection, clear communication channel.
- **Needs Improvement:** Missing canary gate or automated rollback threshold.

## Action Items
| Action | Owner | Priority | Tracking Ticket |
| :--- | :--- | :---: | :--- |
| Add automated rollback trigger on 5xx spike | `@owner` | P1 | `OPS-101` |
| Update staging load test scenario | `@owner` | P2 | `OPS-102` |
