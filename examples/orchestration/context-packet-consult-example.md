# Context Packet Consult Example

## User Input

```text
Atlas, before the implementation task package, @Vega check whether the source evidence is enough.
```

## Mode

`consult`

## Context Packet

```yaml
schema: agentpal.context-packet.v0.3
packet_id: cp-consult-vega-001
created_at: YYYY-MM-DD
from_pal: Atlas
to_pal_candidate: Vega
mode: consult
explicit_user_call:
  type: "@Pal"
  raw_text: "@Vega"
owner_status: consultant_candidate
user_goal: "Prepare an implementation task package after checking source evidence."
task_summary: "Assess evidence sufficiency for the requirements claim."
current_state:
  status: "draft requirement exists"
  evidence_available:
    - "requirement summary"
constraints:
  - "Research consult only."
  - "No full project scan."
relevant_files:
  - path: "docs/example-requirement-summary.md"
    purpose: "synthetic requirement summary"
can_read:
  - "requirement summary"
cannot_read:
  - "implementation draft"
  - "private memory"
  - "full chat history"
can_receive_outputs_from:
  - "Atlas task judgement"
needed_output: "Evidence sufficiency note"
output_contract: "facts, assumptions, missing sources, confidence, recommendation"
verification_requirements:
  - "missing source categories are named"
privacy_policy: "public-safe; sensitive context excluded"
sensitive_context: "none"
expiration: "single workflow"
handoff_notes: "Consult does not transfer ownership from Atlas."
return_to: Atlas
final_report_required: true
```

## Pal Output

Vega reports what evidence is present, what is missing, how confident the requirement claim is, and what Atlas should ask the Runtime or user to gather next.

## Return Path

Vega returns to Atlas. Atlas decides how to adjust the development task package.

## Good Behavior

- Atlas remains owner.
- Vega evaluates evidence, not implementation.
- The packet limits context to the requirement summary.

## Bad Behavior

- Vega reads all implementation notes without need.
- Vega becomes owner.
- Atlas treats Vega's consult as a fixed route for future research tasks.

## Acceptance Criteria

- `mode` is `consult`.
- `return_to` is `Atlas`.
- Missing evidence is explicit.

## No-Code Boundary

No browsing or runtime search happens unless a later Runtime Task Package asks for it and evidence is returned.
