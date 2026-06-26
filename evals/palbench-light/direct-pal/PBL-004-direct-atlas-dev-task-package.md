# PBL-004 - Direct Atlas Dev Task Package

## Category

Direct `/pal Name`.

## User Input

```text
/pal Atlas Create a bounded development task package to update two docs and verify no runtime code was added.
```

## Baseline Behavior

A direct assistant may write generic implementation steps, skip Atlas-specific output expectations, or claim checks before any runtime evidence.

## Expected AgentPal Behavior

Atlas is the speaking Pal. Atlas uses a development task-package shape: file scope, allowed reads/writes, steps, acceptance criteria, no-code boundary, and evidence required. If the task becomes a release judgement, Atlas names a verifier candidate instead of overclaiming final acceptance.

## Required Assets / Context

- Atlas minimum assets or honest fallback.
- Target docs named by the user or requested as a focused clarification.
- No unrelated Pal assets.

## Expected Task Judgement

- domain_focus: bounded documentation implementation package.
- selected owner: Atlas for implementation package.
- verifier candidate: case-specific quality candidate if acceptance risk is meaningful.
- runtime_candidates: file-editing runtime after approval.

## Expected Output Shape

- Task Package with goal, file scope, steps, constraints, risks, acceptance, and evidence.
- Explicit no-runtime artifact check.
- `not-run` handling for checks not executed.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| owner_judgement | Mira or generic assistant answers the Atlas body. | Atlas prefix but weak asset/output shape. | Atlas answers with implementation package reasoning. |
| task_package_quality | Vague plan. | Plan misses evidence or file scope. | Executable package with boundaries and checks. |
| verification_quality | Claims checks passed. | Mentions checks generally. | Defines evidence and not-run handling. |
| no_hardcoded_routing | Treats all docs work as Atlas-owned. | Some candidate wording. | Atlas owns only this implementation-shaped package by current-case judgement. |
| auditability | No file or evidence trail. | Partial. | Clear reviewable package. |

## Failure Modes

- Mira writes the specialist body after a direct Pal call.
- Atlas says the docs were changed without Runtime evidence.
- The package permits broad repository edits.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
