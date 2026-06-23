# Task Judgement Packet Template

Use this template when a task needs explicit scheduling judgement. It is optional in v0.1 and mainly useful for audits, PalBench, or future orchestration.

```yaml
schema: agentpal.task-judgement.v0.1
task_goal:
task_type_candidates:
  - candidate:
    why_candidate:
complexity: simple | medium | complex
risk_level: low | medium | high
needs_file_read: false
needs_file_write: false
needs_command: false
needs_external_knowledge: false
needs_skill: false
needs_plugin: false
needs_verification: false
preferred_latency: fast | balanced | quality
budget_sensitivity: low | medium | high
context_scope:
  project_scope:
  pal_asset_scope:
  memory_scope:
recommended_mode:
  candidate: fast_route | single_owner | owner_plus_verifier | plan_execute_verify | parallel_independent_review | sequential_chain | best_of_n_runtime
  note: candidate only; not a hard rule
candidate_owner_pals:
  - pal_id:
    reason:
candidate_capabilities:
  runtimes: []
  models: []
  reasoning_profiles: []
  skills: []
  plugins: []
  mcp: []
context_access_list_needed: false
evidence_required:
open_questions:
do_not_do:
```
