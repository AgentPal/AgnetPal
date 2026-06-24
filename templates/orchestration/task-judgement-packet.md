# Task Judgement Packet Template

Use this template when a task needs explicit scheduling judgement. It is optional in v0.1 and mainly useful for audits, PalBench, or future orchestration.

```yaml
schema: agentpal.task-judgement.v0.1
task_goal:
domain_focus:
deliverables:
  content_deliverables:
    - deliverable:
      acceptance_note:
  final_deliverables:
    - deliverable:
      acceptance_note:
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
work_stages:
  - stage_id:
    stage_goal:
    capability_needs:
      - need:
    pal_candidates:
      - pal_id:
        candidate_role: content_stage_owner | implementation_stage_owner | verifier | consultant | conductor
        why_candidate:
        not_a_fixed_route: true
    runtime_candidates:
      - runtime_id:
        why_candidate:
        not_a_fixed_route: true
    skill_candidates:
      - skill_id:
        why_candidate:
        not_a_fixed_route: true
    verification_needs:
      - need:
overall_conductor:
  default: Mira
  current_conductor:
  note:
recommended_mode:
  candidate: fast_route | single_owner | staged_task_package | owner_plus_verifier | plan_execute_verify | parallel_independent_review | sequential_chain | best_of_n_runtime
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
decision_basis:
  - user_goal
  - deliverables
  - capability_needs
  - available_pals
  - available_runtime
  - context
  - risk
hardcoded_routing_policy:
  fixed_keyword_routes_allowed: false
  task_domain_fixed_routes_allowed: false
  candidates_are_not_routes: true
context_access_list_needed: false
evidence_required:
open_questions:
do_not_do:
  - do_not_use_keyword_routing
  - do_not_collapse_multi_stage_task_to_domain_owner
  - do_not_let_runtime_bypass_pal_layer
```
