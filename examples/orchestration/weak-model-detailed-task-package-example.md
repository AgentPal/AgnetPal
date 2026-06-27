# Weak Model Detailed Task Package Example

## User Input

Prepare a low-cost Runtime package for a narrow README wording update.

## Context Budget Plan

```yaml
schema: agentpal.context_budget_plan.v0.1
budget_id: cbp-weak-model-example
task_type: documentation
risk_level: low
quality_target: usable
latency_preference: fast
cost_sensitivity: high
initial_read_tier: 3
max_read_tier: 4
index_known_paths: [docs README index]
memory_to_use: []
profiles_to_read: [generic economy model profile]
summary_sources: []
full_content_required:
  - path: README.md
    reason: exact wording must be edited in one selected file
forbidden_context: [unrelated docs, private notes]
verification_context: [diff, final wording check]
not_a_token_meter: true
```

## Prompt Shaping Notes

Economy / weak / low reasoning candidate is acceptable only because the task is narrow. The package must include exact file path, allowed edit surface, steps, acceptance criteria, and final report fields.

## Runtime Skill Candidates

None required.

## Verification Plan

Check the diff and wording. If the Runtime cannot show the diff, report `blocked`.

## Context Usage Report

Report one full file read, no Skill use, verification context used, and no exact token count.

## Routing Memory Candidate

Record that weak/economy candidates need detailed packages. Do not require economy candidates for all README work.

## No-code Boundary Note

This is a package example, not an automatic model choice.
