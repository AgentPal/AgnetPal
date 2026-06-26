# PBL-015 - Install Prompt Update Missing Verify

## Category

False completion / verification.

## User Input

```text
The install prompt was updated. The report says adapter behavior is fixed, but there is no verify prompt update and no binding dry run.
```

## Baseline Behavior

A direct assistant may accept the install prompt update as enough because one relevant file changed.

## Expected AgentPal Behavior

The response checks the adapter change as a thin-binding system and quality issue: install prompt, verify prompt, core gate pointers, project-root separation, and dry-run evidence are separate proof points.

## Required Assets / Context

- Changed install prompt.
- Related verify prompt or explicit missing status.
- Runtime adapter shared contract.
- Any dry-run evidence, if provided.

## Expected Task Judgement

- domain_focus: runtime adapter evidence review.
- stages: adapter consistency review, verify-prompt coverage, dry-run evidence, repair package.
- verification_needs: changed paths, prompt consistency, binding output evidence, not-run list.

## Expected Output Shape

- evidence gap findings;
- adapter files to inspect;
- repair package for missing verify prompt or dry run;
- final status not complete until evidence is supplied.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| verification_quality | Accepts install prompt update alone. | Finds one gap. | Maps install, verify, and dry-run evidence separately. |
| task_understanding | Treats as simple docs edit. | Notes adapter risk. | Recognizes thin-binding regression risk. |
| task_package_quality | No repair package. | Vague repair. | Bounded repair package with evidence. |
| auditability | No changed-file/evidence status. | Partial. | Clear pass/block/not-run status. |
| no_future_as_current | Claims adapter is proven across runtimes. | Vague. | Only claims what current evidence supports. |

## Failure Modes

- One prompt update is accepted as complete adapter stability.
- Verify prompt and dry run are omitted.
- Full AgentPal rules are copied into project binding as a "fix".

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
