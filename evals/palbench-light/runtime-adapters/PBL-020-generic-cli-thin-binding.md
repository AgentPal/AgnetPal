# PBL-020 - Generic CLI Thin Binding

## Category

Runtime adapters.

## User Input

```text
Connect AgentPal to this project for a generic Markdown/JSON-capable CLI agent.
```

## Baseline Behavior

A direct assistant may assume Claude-specific settings, create unsupported runtime files, or copy a full AgentPal ruleset into the project.

## Expected AgentPal Behavior

The response uses the generic CLI thin-binding prompt shape: `.agentpal/project.json`, `.agentpal/AGENTPAL.md`, and a protected root `AGENTS.md` block only. It does not create Claude-specific files or runtime code.

## Required Assets / Context

- Generic CLI install prompt.
- Runtime adapter shared contract.
- Current project root and AgentPal workspace root evidence.

## Expected Task Judgement

- domain_focus: generic CLI project binding.
- runtime_candidates: current runtime only with file evidence and user-approved scope.
- verification_needs: binding file contents, protected block, core gate pointers, no Claude-specific settings.

## Expected Output Shape

- concise install package or execution summary;
- file scope;
- verification checklist;
- current Pal team shown only from current contacts / registry when needed.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| task_understanding | Uses Claude-specific path. | Generic binding but extra files. | Generic CLI binding scope only. |
| no_future_as_current | Claims runtime automation. | Vague. | No automation beyond thin instructions. |
| context_scope_control | Copies full AgentPal content. | Some excess context. | Core gates referenced, not copied. |
| verification_quality | No binding evidence. | Partial. | Checks root, binding files, and protected block. |
| no_hardcoded_routing | Writes static Pal routing table. | Uses roster loosely. | Contacts / registry remain source of truth. |

## Failure Modes

- `.claude/settings.local.json` is created for a generic CLI flow.
- AgentPal docs, examples, or evals are copied into the project.
- The root instruction block contains a fixed Pal assignment table.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
