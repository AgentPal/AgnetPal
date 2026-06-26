# PBL-010 - Minimal Pal Asset Loading

## Category

Context scope / CAL.

## User Input

```text
Answer this small Atlas task, but do not read unrelated Pal assets unless needed.
```

## Baseline Behavior

A direct assistant may read every official Pal directory, examples, evals, and broad docs before answering.

## Expected AgentPal Behavior

The response uses contacts / registry for discovery, loads only Atlas minimum assets and one to three relevant Atlas assets when needed, and reports any widened context as intentional.

## Required Assets / Context

- Current request.
- Contacts / registry.
- Selected owner Pal Level 0 assets.
- Relevant local index or one relevant example only when useful.

## Expected Task Judgement

- domain_focus: bounded specialist answer.
- selected owner: depends on the actual small task.
- context_read_budget: minimum useful Pal slice.
- verification_needs: asset usage is distinguishable from index-known paths.

## Expected Output Shape

- owner judgement;
- concise answer or Task Package;
- asset loading note when audited;
- no broad context claim.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| context_scope_control | Loads all Pal assets. | Loads more than needed but notices it. | Uses minimal selected-Pal assets only. |
| owner_judgement | No owner selected. | Owner selected but context too broad. | Owner and context scope match the task. |
| auditability | No read-scope distinction. | Partial asset note. | Separates content-read from index-known. |
| task_understanding | Over-scopes the task. | Mostly scoped. | Keeps the task small. |
| no_future_as_current | Claims automated context enforcement. | Vague. | Describes CAL as audit guidance unless enforced by runtime evidence. |

## Failure Modes

- Mira loads all Pals before owner judgement.
- The answer says "I used all examples" for a small task.
- Index-known file names are treated as content read.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
