# Cross-Runtime Continuation Task Package

Use this package when a project was previously handled in one host Runtime and now continues in another.

Example scenario:

```text
This project had one Codex round. Continue it in Claude Code without starting from zero.
```

```yaml
schema: agentpal.cross_runtime_continuation_task_package.v0.1
user_goal: ""
previous_runtime: ""
current_runtime_candidate:
  name: ""
  reason: ""
  current_evidence_required: true
pal_memory_snapshot:
  snapshot_id: ""
  path_or_reference: ""
  summary: ""
project_state_summary: ""
routing_memory_summary:
  records_considered: []
  lessons:
    - lesson: ""
      not_a_fixed_route: true
what_to_continue:
  - ""
what_not_to_repeat:
  - ""
required_context:
  - ""
forbidden_context:
  - ""
runtime_skill_candidates:
  - name: ""
    type: ""
    reason: ""
    evidence_required: []
next_steps:
  - ""
verification_plan:
  evidence_required: []
  verifier_candidates: []
  result_record_template: ""
final_report_format:
  must_include:
    - previous_runtime
    - current_runtime_evidence
    - memory_snapshot_used
    - runtime_skills_used_or_not_run
    - files_read_or_changed
    - verification_result
    - memory_writeback_candidate
memory_writeback_required: true
not_a_fixed_route: true
privacy_notes:
  private_memory_minimized: true
  raw_chat_history_excluded: true
```

## Rules

- `current_runtime_candidate` is not a fixed route.
- Read the Pal memory snapshot before treating the task as new.
- Do not repeat previously failed paths unless the package explains why conditions changed.
- After completion, prepare memory writeback candidates for Pal Memory, Project Memory, Routing Memory, Runtime Skill Usage Memory, and Verification Memory when relevant.
- The host Runtime executes; AgentPal does not.
