# Memory Reuse Saves Context Example

## User Input

Continue the previous documentation cleanup without rereading everything.

## Context Budget Plan

```yaml
schema: agentpal.context_budget_plan.v0.1
budget_id: cbp-memory-reuse-example
task_type: continuation
risk_level: medium
quality_target: usable
cost_sensitivity: high
initial_read_tier: 2
max_read_tier: 4
index_known_paths: [RESOURCE_INDEX.md, docs index]
memory_to_use: [pal_project_memory_snapshot, routing_memory_summary]
profiles_to_read: []
summary_sources: [previous task summary]
full_content_required:
  - path: selected changed document
    reason: exact current content must be verified before editing
forbidden_context: [private project memory not named in package]
verification_context: [diff, changed file list, not-run items]
not_a_token_meter: true
```

## Prompt Shaping Notes

Use memory summary first, then selected current files. Memory saves context but does not prove the current file state.

## Runtime Skill Candidates

None required. A repository diff capability may be named if available.

## Verification Plan

Compare current files against the requested change. Report stale memory or missing files.

## Context Usage Report

Record context saved by memory reuse and the full files still needed for current evidence.

## Routing Memory Candidate

Future similar continuation tasks may start at Tier 2 when a fresh memory snapshot exists. This is a candidate, not a fixed rule.

## No-code Boundary Note

No automatic memory sync is implied.
