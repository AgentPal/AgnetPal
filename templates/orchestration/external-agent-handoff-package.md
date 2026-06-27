# External Agent Handoff Package

Use this no-code package when work may be handed to an external Agent by a user or by a host Runtime that explicitly supports and permits external Agent calls.

AgentPal does not call the external Agent.

```yaml
schema: agentpal.external_agent_handoff_package.v0.1
handoff_id: ""
user_goal: ""
handoff_status: <available | unavailable | unknown | blocked>
status_reason: ""
host_runtime_availability:
  runtime: ""
  external_agent_support: <available | unavailable | unknown | blocked>
  evidence_source: ""
  permission_notes: []
owner_pal_candidate:
  pal: ""
  reason: ""
external_agent_candidate:
  name_or_type: ""
  reason: ""
context_packet:
  can_read: []
  cannot_read: []
  can_receive_outputs_from: []
  required_output: []
verification_requirements:
  - ""
final_report_required:
  must_include:
    - verdict
    - evidence_checked
    - missing_evidence
    - actions_taken_or_not_run
    - unavailable_or_blocked_capabilities
    - risks
    - recommended_repairs
fallback_if_unavailable:
  - "Use host Runtime manual execution package."
  - "Mark external Agent execution as not-run."
  - "Return missing evidence and next candidate check."
no_code_boundary:
  agentpal_calls_external_agent: false
  host_runtime_or_user_may_handoff: true
  unavailable_is_not_fail: true
not_a_fixed_route: true
```
