# Subagent Task Package

Use this no-code package only when a host Runtime explicitly supports a subagent-style capability and the current task package permits it.

AgentPal does not start the subagent. The host Runtime or user handles any real invocation and must return evidence.

```yaml
schema: agentpal.subagent_task_package.v0.1
package_id: ""
user_goal: ""
subagent_status: <available | unavailable | unknown | blocked>
status_reason: ""
host_runtime_availability:
  runtime: ""
  subagent_support: <available | unavailable | unknown | blocked>
  evidence_source: ""
  permission_notes: []
owner_pal_candidate:
  pal: ""
  reason: ""
subagent_candidate:
  role: ""
  reason: ""
bounded_task:
  goal: ""
  allowed_actions: []
  forbidden_actions: []
  can_read: []
  cannot_read: []
  expected_output: []
verification:
  evidence_required: []
  verifier_candidate: ""
  result_record_required: true
fallback_if_unavailable:
  - "Do not call a subagent."
  - "Use manual host Runtime task package or ask the user for another Runtime."
  - "Report unavailable, unknown, blocked, or not-run."
no_code_boundary:
  agentpal_starts_subagent: false
  host_runtime_manual_execution: true
  agentpal_auto_execution: false
not_a_fixed_route: true
```
