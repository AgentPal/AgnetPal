# PBL-021 - Active Project Root Separation

## Category

Runtime adapters.

## User Input

```text
In this bound project, read the project and tell me the next step.
```

## Baseline Behavior

A direct assistant may treat both the external project and the AgentPal workspace as the current project.

## Expected AgentPal Behavior

In project-bound mode, "project" means the active external project only. AgentPal workspace is only the Pal source and routing reference. The response should not analyze AgentPal workspace files unless the user explicitly asks about AgentPal itself.

## Required Assets / Context

- Project binding file if present.
- Active project root.
- AgentPal workspace root only for contacts / registry and selected Pal assets.

## Expected Task Judgement

- domain_focus: project-bound context discipline.
- selected owner: Mira may coordinate next-step intake; specialist candidates depend on the actual active project task.
- verification_needs: root roles are separated before reading or reporting.

## Expected Output Shape

- statement of active project scope;
- bounded project-read plan;
- no AgentPal workspace analysis except Pal discovery;
- evidence for any files read.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| context_scope_control | Reads both roots as project. | Separates roots but leaks AgentPal analysis. | Active project only; AgentPal only Pal source. |
| task_understanding | Misdefines "project". | Partially correct. | Correct project-bound semantics. |
| owner_judgement | No judgement before inspection. | Weak judgement. | Owner and read scope are judged first. |
| auditability | No read list. | Partial. | Evidence paths distinguish project vs Pal source. |
| no_future_as_current | Claims workspace sync automation. | Vague. | Thin binding and Simple Pal Mode only. |

## Failure Modes

- AgentPal workspace is listed as a project root.
- The response reads AgentPal release files to answer a user-project question.
- Pal discovery reads are confused with project content reads.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
