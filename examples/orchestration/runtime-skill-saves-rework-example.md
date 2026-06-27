# Runtime Skill Saves Rework Example

## User Input

Package a document conversion task and reduce manual rework if the host Runtime has a document rendering Skill.

## Context Budget Plan

```yaml
schema: agentpal.context_budget_plan.v0.1
budget_id: cbp-runtime-skill-example
task_type: document
risk_level: medium
quality_target: usable
cost_sensitivity: medium
initial_read_tier: 1
max_read_tier: 4
index_known_paths: [document workflow template, source inventory]
memory_to_use: [runtime_skill_usage_memory_summary]
profiles_to_read: [document Skill profile]
summary_sources: [source document summary]
full_content_required:
  - path: selected source document
    reason: conversion scope and headings must be verified
forbidden_context: [unrelated documents, credentials]
runtime_skill_candidates:
  - name: document-rendering Skill candidate
    availability_check_required: true
verification_context: [rendered sample, output path, layout notes]
not_a_token_meter: true
```

## Prompt Shaping Notes

Use medium reasoning. If the Skill is unavailable, fall back to a manual task package with stricter output review.

## Runtime Skill Candidates

Document rendering Skill candidate may save repeated manual layout inspection, but only after current availability evidence.

## Verification Plan

Rendered output must be checked against source preservation and layout requirements. Skill output is not automatically accepted.

## Context Usage Report

Record Skill availability, whether it saved rework, and missing evidence.

## Routing Memory Candidate

Record successful Skill usage as a candidate for similar document tasks, not as a required route.

## No-code Boundary Note

AgentPal does not run the document tool or install document dependencies.
