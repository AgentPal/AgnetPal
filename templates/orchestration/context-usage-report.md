# Context Usage Report

Use this report after a Context Budget Plan, Deep Conductor package, Project Conductor package, or Runtime Task Package returns results.

This report gives auditable context usage. It is not an exact token count. `not_exact_token_count: true` must remain present unless the host Runtime provides exact metering evidence in a separate field.

```yaml
schema: agentpal.context_usage_report.v0.1
report_id: ""
task_id: ""
short_summary:
  read_strategy_used: ""
  what_was_saved: []
  what_was_not_read: []
  verification_context_preserved: true
read_tiers_used:
  - tier: 0
    reason: ""
index_known_paths_count: 0
memory_used:
  used: false
  sources: []
  privacy_notes: []
profiles_read:
  - profile: ""
    type: ""
    reason: ""
summary_sources_count: 0
full_content_files_count: 0
runtime_skills_used:
  - name: ""
    status: "" # used | not-run | unavailable | unknown | blocked
    evidence: ""
verification_context_used:
  - ""
context_saved_by_reuse:
  - ""
context_saved_by_avoiding:
  full_workspace_read: false
  duplicate_research: false
  unnecessary_pal_assets: false
  unnecessary_profiles: false
quality_tradeoffs:
  - ""
missing_context:
  - ""
next_time_recommendation:
  recommendation: ""
  not_a_fixed_route: true
not_exact_token_count: true
```

## Use

Use this report for Routing Memory and PalBench Collaboration evidence. It helps future AI judgement understand which context was sufficient, which reuse saved effort, and which missing evidence caused risk.

Recommendations are candidates only. They must not become fixed Pal, Runtime, Skill, model, or context routes.
