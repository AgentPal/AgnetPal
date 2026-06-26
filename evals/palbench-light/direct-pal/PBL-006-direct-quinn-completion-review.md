# PBL-006 - Direct Quinn Completion Review

## Category

Direct `/pal Name`.

## User Input

```text
/pal Quinn Review this completion report and tell me whether the work is actually proven complete.
```

## Baseline Behavior

A direct assistant may summarize the completion report and accept confident wording as proof.

## Expected AgentPal Behavior

Quinn is the speaking Pal. Quinn maps requirements to evidence, separates pass, fail, missing, weak, blocked, and `not-run`, and refuses to mark completion proven when evidence is absent.

## Required Assets / Context

- Quinn minimum assets or honest fallback.
- Requirements, claimed changes, changed paths, command outputs, or explicit absence of evidence.

## Expected Task Judgement

- domain_focus: evidence-based completion review.
- selected owner: Quinn for verification.
- repair candidates: case-specific owners for missing evidence repair.
- verification_needs: requirement-by-requirement evidence table.

## Expected Output Shape

- findings first;
- evidence table;
- false-completion flag when applicable;
- final status: pass / fail / blocked / not-run / inconclusive.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| verification_quality | Accepts claims as proof. | Notes missing evidence but final status overclaims. | Requirement-by-requirement evidence judgement. |
| owner_judgement | Wrong speaker or no Quinn method. | Quinn prefix with generic review. | Quinn uses quality/evidence review shape. |
| auditability | No table or trace. | Partial list. | Clear findings and evidence status. |
| user_decision_burden | Asks user to decide if complete. | Requests many broad details. | Gives current judgement and focused missing evidence list. |
| no_future_as_current | Claims independent reviewers ran. | Vague. | No automated review claims without runtime evidence. |

## Failure Modes

- Summary is treated as evidence.
- `not-run` checks are omitted.
- Quinn starts implementing repairs instead of reviewing evidence.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
