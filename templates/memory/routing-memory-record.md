# Routing Memory Record

This template combines routing decision and result fields for public-safe examples or private project memory.

Routing Memory is AI Judgement input. It is not a route table and not an automatic dispatch rule.

```yaml
schema: agentpal.routing_memory_record.v0.1
record_id: ""
created_at: ""
task_summary: ""
project_id: ""
pal_candidates:
  - pal: ""
    role_candidate: ""
    reason: ""
owner_pal_selected:
  pal: ""
  reason: ""
verifier_candidates:
  - pal: ""
    reason: ""
runtime_candidates:
  - runtime: ""
    reason: ""
    current_evidence_required: true
runtime_selected:
  runtime: ""
  evidence: ""
model_or_reasoning_candidate:
  model: ""
  reasoning: ""
  reason: ""
runtime_skill_candidates:
  - name: ""
    type: "" # Agent Skill | plugin | MCP | browser | office document | repo analysis | other
    reason: ""
runtime_skills_used:
  - name: ""
    used: false
    evidence: ""
pal_owned_skills_used:
  - pal: ""
    skill_or_method: ""
    purpose: ""
context_budget:
  context_budget_used: false
  read_tiers_used: []
  context_saved_by_memory_reuse: ""
  runtime_skill_saved_effort: ""
  verification_cost: ""
  rework_cost: ""
  next_time_context_budget_recommendation: ""
  context_read_count: 0
  profile_read_count: 0
  memory_used: false
verification_result: "" # pass | fail | partial | not-run | blocked
rework_count: 0
user_accepted: "" # true | false | unknown
what_worked:
  - ""
what_failed:
  - ""
next_time_recommendation: ""
not_a_fixed_route: true
privacy_notes:
  public_safe: false
  private_content_excluded: true
  desensitized: true
```

## Rules

- `next_time_recommendation` is a suggestion, not a rule.
- `next_time_context_budget_recommendation` is a candidate for future judgement, not a fixed context route.
- `read_tiers_used` records qualitative tiers, not exact token counts.
- Memory reuse and Runtime Skill usage may reduce effort, but current task judgement and verification still decide the next package.
- `not_a_fixed_route: true` must remain present.
- Do not record sensitive content, credentials, raw logs, full files, or local absolute paths.
