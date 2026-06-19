# Fable Release Gate

A criterion passes only when its evidence field identifies an actual proof-table row, test, log, artifact, or reproducible observation.

## Decision

`ship` | `final-slice` | `pivot` | `archive`

| Criterion | Status | Evidence | Blocking gap or caveat |
|---|---|---|---|
| Works in intended environment | `pass/fail` | [receipt] | [gap] |
| Representative evaluation completed | `pass/fail` | [receipt] | [gap] |
| Primary acceptance threshold met | `pass/fail` | [receipt] | [gap] |
| Failure modes documented | `pass/fail` | [receipt] | [gap] |
| Fallback, escalation, or rollback defined | `pass/fail/n/a` | [receipt or justification] | [gap] |
| Result reproducible or demonstrable | `pass/fail` | [receipt] | [gap] |
| External claims trace to evidence | `pass/fail/n/a` | [receipt or justification] | [gap] |
| Locked target actually solved | `pass/fail` | [receipt] | [gap] |

## Blocking gaps

- [Only gaps that prevent the selected decision]

## Minimum final slice

Include only for `final-slice`:

1. [Proof-producing action]
2. [Proof-producing action]
