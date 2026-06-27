# Direct Pal Atlas Development Task

## User Input

```text
/pal Atlas Help me turn this feature request into a Codex development task package.
```

## Mode

`direct_owner`

## Context Packet

```yaml
schema: agentpal.context-packet.v0.3
packet_id: cp-direct-atlas-dev-001
created_at: YYYY-MM-DD
from_pal: user
to_pal_candidate: Atlas
mode: direct_owner
explicit_user_call:
  type: "/pal"
  raw_text: "/pal Atlas"
owner_status: current_owner_candidate
user_goal: "Turn a feature request into a Codex development task package."
task_summary: "Judge the development shape and prepare a task package if the scope is sufficient."
current_state:
  status: "feature request provided by user"
  evidence_available:
    - "user feature summary"
constraints:
  - "No runtime code is created by AgentPal."
  - "No fixed routing."
relevant_files:
  - path: "docs/02-getting-started/multi-pal-collaboration-prompt-cards.md"
    purpose: "usage reference"
can_read:
  - "user feature summary"
  - "selected project files only if user allows"
cannot_read:
  - "full chat history"
  - "private memory"
  - "credentials, tokens, secrets"
can_receive_outputs_from:
  - "none"
needed_output: "Runtime Task Package"
output_contract: "orchestration/task-package-output-contract.md"
verification_requirements:
  - "acceptance criteria and evidence required are explicit"
privacy_policy: "public-safe; sensitive context excluded"
sensitive_context: "none"
expiration: "single workflow"
handoff_notes: "Atlas is a direct owner candidate, not a permanent route."
return_to: user
final_report_required: true
```

## Pal Output

Atlas should state that it accepts current owner-candidate status, judge whether the feature request is single-stage or composite, name any stage candidates, and produce a development task package if enough context exists.

## Return Path

Atlas returns directly to the user. Mira resumes only if Atlas recommends conductor coordination or the user asks.

## Good Behavior

- Atlas applies core gates.
- Atlas uses development task-package shape.
- Atlas marks Runtime as execution layer only.
- Atlas names Quinn, Rhea, Vega, or other Pals only as case-specific candidates when useful.

## Bad Behavior

- Mira silently takes over the direct call.
- Atlas claims every stage because the request contains development language.
- `/pal` is treated as a native CLI command requirement.

## Acceptance Criteria

- `mode` is `direct_owner`.
- `owner_status` is `current_owner_candidate`.
- No fixed route appears.
- Completion evidence is required.

## No-Code Boundary

This example is a Markdown protocol example. It does not launch an Agent, subagent, CLI command, or background process.
