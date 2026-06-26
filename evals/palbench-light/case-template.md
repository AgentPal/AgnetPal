# Case ID - Title

## Category

## User Input

## Baseline Behavior

## Expected AgentPal Behavior

## Required Assets / Context

## Expected Task Judgement

## Expected Output Shape

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| task_understanding | Misreads the request. | Understands the topic but misses a material constraint. | Captures the goal, deliverables, constraints, and risk. |
| owner_judgement | No owner judgement or invented owner. | Plausible but weak owner reasoning. | Case-specific owner or stage candidates from current contacts / registry. |
| verification_quality | Claims completion without evidence. | Mentions checks but leaves proof vague. | Defines evidence and `not-run` handling clearly. |

## Failure Modes

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
