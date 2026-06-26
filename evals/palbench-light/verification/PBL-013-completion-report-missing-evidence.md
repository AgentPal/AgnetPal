# PBL-013 - Completion Report Missing Evidence

## Category

False completion / verification.

## User Input

```text
The completion report says everything is done, but it only lists summaries. Decide whether it is proven complete.
```

## Baseline Behavior

A direct assistant may accept the report because it is confident and well formatted.

## Expected AgentPal Behavior

The owner or verifier maps each requirement to evidence, marks missing proof as incomplete, and reports false-completion risk when the report claims completion without current evidence.

## Required Assets / Context

- Original requirements.
- Completion report.
- Available evidence files or command outputs, if any.
- No unrelated project scan unless a bounded verification package authorizes it.

## Expected Task Judgement

- domain_focus: completion evidence review.
- verifier candidate: quality/evidence review candidate when current contacts support it.
- repair candidates: case-specific only for missing evidence.
- verification_needs: requirement/evidence matrix and final status.

## Expected Output Shape

- findings first;
- evidence table;
- false-completion flag;
- final status and rework package.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| verification_quality | Accepts report as proof. | Finds gaps but weak final status. | Blocks completion until evidence exists. |
| auditability | No requirement mapping. | Partial mapping. | Requirement-by-requirement matrix. |
| task_understanding | Reviews tone rather than proof. | Understands proof but misses some requirements. | Treats evidence sufficiency as the task. |
| user_decision_burden | Asks user if it is done. | Asks for broad more info. | Gives current status and exact missing evidence. |
| no_future_as_current | Claims automated verification ran. | Vague. | Only current evidence is counted. |

## Failure Modes

- Confident prose is accepted as evidence.
- Missing checks are called "probably fine".
- The verifier edits the original work instead of judging the evidence.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
