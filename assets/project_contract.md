# Fable Project Contract

## Mode

`start` | `recover`

## Locked target

Deliver **[artifact/outcome]** for **[user/problem]** by **[decision date]**, accepted when **[measurable evidence]**, in **[intended environment]**, within **[constraints]**.

## Keep sacred

- [Public behavior, data, interface, policy, or invariant that must not regress]

## Forbidden outcomes

- [Destructive, unsafe, misleading, or incompatible result]

## Non-goals

- [Explicit exclusion]

## Recovery audit

Include only in `recover` mode.

| Existing item | Current receipt/state | Keep/Cut/Park | Required action |
|---|---|---|---|
| [artifact, branch, feature, or plan] | [what is demonstrably true] | [decision] | [next action or none] |

## Evidence-producing slices

| Slice | Risk or unknown resolved | Decisive check | Evidence location |
|---|---|---|---|
| Thin end-to-end path | [highest-risk unknown] | [check that can fail] | [proof row/path] |
| Representative behavior | [critical capability] | [evaluation] | [proof row/path] |
| Intended-environment run | [integration/operational risk] | [runtime check] | [proof row/path] |

## Change gate

A scope or stack change requires:

1. new user evidence, safety/compliance need, failed acceptance criterion, or demonstrated infeasibility;
2. the observed blocker and affected criterion;
3. expected risk reduction greater than migration cost.

## Immediate next check

[Smallest action that resolves the highest-risk unknown and produces evidence]
