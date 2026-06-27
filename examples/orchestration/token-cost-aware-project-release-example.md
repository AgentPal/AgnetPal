# Token / Cost-aware Project Release Example

## User Input

Prepare a release-readiness package for a public Markdown / JSON workspace. Keep the check bounded and do not read the whole repository unless a release risk requires escalation.

## Context Budget Plan

```yaml
schema: agentpal.context_budget_plan.v0.1
budget_id: cbp-release-example
task_type: release
risk_level: high
quality_target: release_gate
cost_sensitivity: medium
initial_read_tier: 1
max_read_tier: 5
index_known_paths: [RESOURCE_INDEX.md, RELEASE_CHECKLIST.md, CHANGELOG.md]
memory_to_use: [routing_memory_summary]
profiles_to_read: [runtime_profile, reasoning_profile]
summary_sources: [previous_release_summary]
full_content_required:
  - path: RELEASE_CHECKLIST.md
    reason: release gate wording must be exact
forbidden_context: [private memory, credentials, raw local logs]
verification_context: [git status, release checklist evidence, public-safe scan result]
not_a_token_meter: true
```

## Prompt Shaping Notes

Use a strong / high reasoning candidate because release readiness is high-risk and evidence-sensitive. Ask for exact `pass`, `fail`, `blocked`, and `not-run` items.

## Runtime Skill Candidates

- Repository analysis Skill candidate, only if the host Runtime reports availability.
- Git command surface, only for bounded status / diff evidence.

## Verification Plan

Verification must include current file status, checklist mapping, changed files, and any not-run checks. It cannot be removed to reduce context.

## Context Usage Report

Report read tiers used, release files fully read, memory reused, profiles read, verification context used, missing evidence, and next-time recommendation. Do not claim exact token count.

## Routing Memory Candidate

Record that release work may need Tier 4 or Tier 5 evidence when public-safety or release claims are involved. This remains a candidate, not a fixed route.

## No-code Boundary Note

This example produces a release task package and evidence checklist only. It does not publish, tag, create automation, run a service, or calculate exact cost.
