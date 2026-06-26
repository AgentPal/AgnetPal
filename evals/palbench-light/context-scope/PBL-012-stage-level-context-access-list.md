# PBL-012 - Stage-Level Context Access List

## Category

Context scope / CAL.

## User Input

```text
Create a staged package for research, implementation, and verification. Each stage should know only what it needs.
```

## Baseline Behavior

A direct assistant may give every stage the same full context or omit access boundaries.

## Expected AgentPal Behavior

The response creates stage-level Context Access List summaries with recipient candidates, can-read paths/summaries, cannot-read boundaries, needed output, content-read budget, and verification requirements.

## Required Assets / Context

- Context Access List protocol.
- Task Package output contract.
- User goal and known stage inputs.

## Expected Task Judgement

- domain_focus: staged workflow context control.
- stages: research, implementation, verification.
- each stage: recipient candidate, task, allowed context, forbidden context, output contract, evidence.
- v0.2 boundary: CAL is audit guidance, not automatic enforcement.

## Expected Output Shape

- staged Task Package;
- CAL table or YAML-like summary per stage;
- explicit forbidden context;
- evidence and not-run handling.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| context_scope_control | Same broad context for all stages. | Some boundaries. | Stage-specific read and cannot-read boundaries. |
| deliverable_awareness | No stage distinction. | Stages named but outputs vague. | Stage outputs and verification are explicit. |
| task_package_quality | No executable package. | Partial package. | Complete staged package with CAL summaries. |
| auditability | Cannot inspect context use. | Some notes. | Read budgets and output contracts are visible. |
| no_future_as_current | Claims automatic CAL enforcement. | Vague. | States current audit-only boundary. |

## Failure Modes

- Verification reads hidden drafts or all raw material without need.
- Implementation receives raw research traces when an accepted summary is enough.
- The package claims Deep Conductor executed the stages.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
