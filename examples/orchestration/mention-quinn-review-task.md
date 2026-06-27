# Mention Quinn Review Task

## User Input

```text
Mira, I am preparing a release. @Quinn review whether the completion report is trustworthy.
```

## Mode

`review`

## Context Packet

```yaml
schema: agentpal.context-packet.v0.3
packet_id: cp-mention-quinn-review-001
created_at: YYYY-MM-DD
from_pal: Mira
to_pal_candidate: Quinn
mode: review
explicit_user_call:
  type: "@Pal"
  raw_text: "@Quinn"
owner_status: reviewer_candidate
user_goal: "Review whether a completion report proves release readiness."
task_summary: "Check claims against allowed evidence and return a quality final report."
current_state:
  status: "completion report and evidence summary are available"
  evidence_available:
    - "completion report summary"
    - "command result summary"
constraints:
  - "No full chat history."
  - "No publish or release action."
relevant_files:
  - path: "reports/example-completion-report.md"
    purpose: "synthetic review target"
can_read:
  - "completion report summary"
  - "accepted command result summary"
cannot_read:
  - "full chat history"
  - "private memory"
  - "unrelated project files"
can_receive_outputs_from:
  - "Mira task judgement"
needed_output: "Quinn final report with pass/fail/partial/not-run/blocked"
output_contract: "Quality review: decision, evidence, gaps, risks, next action"
verification_requirements:
  - "claims are mapped to evidence"
privacy_policy: "public-safe; sensitive context excluded"
sensitive_context: "none"
expiration: "single workflow"
handoff_notes: "@Quinn is review consult by default, not owner transfer."
return_to: Mira
final_report_required: true
```

## Pal Output

Quinn returns a structured final report with decision, evidence reviewed, claims proven, claims not proven, risks, and next action.

## Return Path

Quinn returns to Mira. Mira summarizes Quinn's final report for the user.

## Good Behavior

- Quinn receives a bounded packet.
- Quinn does not need full history.
- Ownership stays with Mira or the current owner.

## Bad Behavior

- The runtime dumps all conversation history to Quinn.
- Quinn becomes owner without explicit handoff.
- Mira rewrites Quinn's professional conclusion without labeling it.

## Acceptance Criteria

- Packet has `mode: review`.
- Packet excludes full chat history.
- Quinn final report is structured.

## No-Code Boundary

This is a manual protocol path. It does not run an automatic reviewer process.
