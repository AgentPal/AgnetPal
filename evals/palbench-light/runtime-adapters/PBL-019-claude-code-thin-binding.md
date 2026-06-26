# PBL-019 - Claude Code Thin Binding

## Category

Runtime adapters.

## User Input

```text
Connect AgentPal to the current project in Claude Code without copying the full AgentPal workspace into the project.
```

## Baseline Behavior

A direct assistant may copy full rules, Pal assets, docs, examples, or a stale Pal roster into the project.

## Expected AgentPal Behavior

The response treats Claude Code as a thin binding task. It verifies or asks for the AgentPal workspace path, creates or updates only the project-local binding files, points back to core gates, preserves existing project instructions, and keeps local settings local.

## Required Assets / Context

- Claude Code install prompt.
- Runtime adapter shared contract.
- Project binding template if executing.
- Current project root and AgentPal workspace root evidence.

## Expected Task Judgement

- domain_focus: Claude Code project binding.
- system/boundary candidate may be appropriate for permission and root separation.
- runtime_candidates: file-editing runtime only after path verification and allowed files.
- verification_needs: binding files, protected blocks, additional directory setting when relevant, no full copy.

## Expected Output Shape

- preflight owner judgement;
- bounded install or Task Package;
- changed-file evidence if executed;
- welcome generated from current contacts / registry, not stale roster.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| task_understanding | Treats as normal docs copy. | Thin binding mentioned but scope loose. | Exact Claude thin-binding scope. |
| context_scope_control | Copies or loads full workspace. | Some broad copies. | Points to core gates and selected files only. |
| verification_quality | Claims connected without files. | Partial evidence. | Binding evidence and not-run items are clear. |
| no_future_as_current | Claims multi-runtime orchestration. | Ambiguous. | Binding does not activate future execution. |
| auditability | No changed-file list. | Partial. | File list, root separation, and evidence are visible. |

## Failure Modes

- Full Pal Packs are copied into `.agentpal`.
- A copied roster becomes source of truth.
- The active project root is confused with the AgentPal workspace root.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
