# Mira Summary From Pal Final Reports

## User Input

```text
Mira, summarize Atlas and Quinn final reports and tell me what remains unresolved.
```

## Mode

Summary stage after final reports.

## Context Packet

```yaml
schema: agentpal.context-packet.v0.3
packet_id: cp-summary-final-reports-001
created_at: YYYY-MM-DD
from_pal: user
to_pal_candidate: Mira
mode: consult
explicit_user_call:
  type: "none"
  raw_text: ""
owner_status: summary_owner
user_goal: "Summarize final Pal reports."
task_summary: "Compare accepted final reports and identify agreement, conflict, evidence gaps, and next action."
current_state:
  status: "two final reports are available"
  evidence_available:
    - "Atlas final report"
    - "Quinn final report"
constraints:
  - "Summarize only provided final reports."
relevant_files:
  - path: "reports/atlas-final-report.md"
    purpose: "synthetic final report"
  - path: "reports/quinn-final-report.md"
    purpose: "synthetic final report"
can_read:
  - "Atlas final report"
  - "Quinn final report"
cannot_read:
  - "draft reviewer notes"
  - "hidden reasoning"
  - "full chat history"
can_receive_outputs_from:
  - "Atlas final report"
  - "Quinn final report"
needed_output: "Mira summary"
output_contract: "agreement, conflict, evidence gaps, unresolved risk, next action"
verification_requirements:
  - "do not invent claims absent from final reports"
privacy_policy: "public-safe; sensitive context excluded"
sensitive_context: "none"
expiration: "single workflow"
handoff_notes: "Mira summarizes final reports only."
return_to: user
final_report_required: true
```

## Pal Output

Mira summarizes common findings, conflicts, evidence gaps, unresolved risk, and next action. Mira labels specialist conclusions as coming from final reports.

## Return Path

Mira returns the summary to the user.

## Good Behavior

- Mira reads final reports only.
- Drafts remain isolated.
- Agreement and conflict are separate.

## Bad Behavior

- Mira invents Quinn's acceptance.
- Mira treats missing evidence as pass.
- Mira reads hidden drafts to smooth conflicts.

## Acceptance Criteria

- Summary references final reports.
- Unresolved risk remains explicit.
- No group-chat collapse.

## No-Code Boundary

This example is a summary protocol, not a multi-agent execution run.
