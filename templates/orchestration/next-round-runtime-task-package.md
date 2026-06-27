# Next-Round Runtime Task Package

Use this template to turn a Project Conductor task map into a bounded next-round task for Codex, Claude Code, OpenCode, OpenHands, Gemini CLI, or another host Runtime.

The host Runtime executes. AgentPal does not execute.

```yaml
schema: agentpal.next_round_runtime_task_package.v0.1
round_goal: ""
target_runtime_candidate:
  name: ""
  reason: ""
  evidence_required: []
previous_runtime_context:
  previous_runtime: ""
  memory_snapshot_used: ""
  routing_memory_summary: []
  runtime_skill_usage_memory_summary: []
  not_a_fixed_route: true
target_model_or_reasoning_candidate:
  model: ""
  reasoning: ""
  reason: ""
context_budget_plan: ""
read_tier:
  initial: 1
  max: 4
  allowed: []
prompt_shaping_notes:
  - ""
model_or_reasoning_candidate:
  model: ""
  reasoning: ""
  reason: ""
cost_sensitivity: ""
quality_target: ""
verification_cost_reason: ""
context_usage_report_required: true
runtime_skill_candidates:
  - name: ""
    type: "" # Agent Skill | plugin | MCP | browser | office document | repo analysis | other
    reason: ""
    evidence_required: []
    usage_memory_considered: ""
required_context: []
forbidden_context: []
task_scope:
  in_scope: []
  out_of_scope: []
steps:
  - ""
acceptance_criteria:
  - ""
verification_plan:
  verifier_candidate: ""
  evidence_required: []
  result_record_template: ""
final_report_format:
  must_include:
    - files_read_or_changed
    - runtime_skills_used_or_not_run
    - memory_snapshot_used_or_not_run
    - memory_writeback_candidate
    - evidence
    - verification_result
    - context_usage_report
    - blockers
memory_writeback_required:
  required: true
  candidates:
    - pal_project_memory_snapshot
    - routing_memory_record
    - runtime_skill_usage_memory_record
    - verification_memory
stop_conditions:
  - ""
```

## Rules

- `target_runtime_candidate` is not a fixed route.
- `context_budget_plan` and `read_tier` guide context use; they are not exact token meters.
- `prompt_shaping_notes` and `model_or_reasoning_candidate` are candidates for the host Runtime / user, not automatic selectors.
- `runtime_skill_candidates` are executed only by the host Runtime when available and authorized.
- `previous_runtime_context` is continuity evidence, not proof of current capability.
- Memory writeback is performed only by the host Runtime when authorized and evidenced.
- The package must not imply AgentPal has already performed the work.
- Verification must not be skipped to reduce cost; report `not-run` or `blocked` when evidence is missing.
- If a stop condition occurs, the Runtime should stop and report evidence or blocker state.
