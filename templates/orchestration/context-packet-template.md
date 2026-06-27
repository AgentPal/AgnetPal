# Context Packet Template

```yaml
schema: agentpal.context-packet.v0.3
packet_id: cp-example-001
created_at: YYYY-MM-DD
from_pal: Mira
to_pal_candidate: Quinn
mode: review
explicit_user_call:
  type: "@Pal"
  raw_text: "@Quinn"
owner_status: reviewer_candidate
user_goal: "<original user goal or concise safe summary>"
task_summary: "<what this recipient is being asked to do>"
current_state:
  status: "<known state>"
  evidence_available:
    - "<evidence item or none>"
constraints:
  - "No runtime code."
  - "No fixed routing."
relevant_files:
  - path: "relative/path.md"
    purpose: "<why it may be relevant>"
can_read:
  - "relative/path.md"
  - "accepted owner final report"
cannot_read:
  - "full chat history"
  - "private user memory"
  - "credentials, tokens, secrets"
  - "other independent reviewer drafts"
can_receive_outputs_from:
  - "Mira task judgement"
needed_output: "<exact deliverable>"
output_contract: "<named contract or bullet structure>"
verification_requirements:
  - "<evidence needed for pass/fail>"
privacy_policy: "public-safe; sensitive context excluded by default"
sensitive_context: "none"
expiration: "single workflow or YYYY-MM-DD"
handoff_notes: "<candidate recipient is not a fixed route; current v0.3 is no-code staged protocol only>"
return_to: Mira
final_report_required: true
```

## Use Notes

- Do not paste full chat history into `user_goal`.
- Keep `to_pal_candidate` as a candidate, not a route.
- `mode` must be one of `consult`, `delegate`, `handoff`, `review`, `owner_transfer`, or `direct_owner`.
- `explicit_user_call` records whether the user used `/pal Name`, `@Pal`, a handoff phrase, or no explicit call.
- `owner_status` states whether the recipient is an owner candidate, consultant candidate, reviewer candidate, delegated sub-output candidate, or accepted owner after transfer.
- `return_to` names who receives the result: Mira, the current owner Pal, or the user.
- `final_report_required` defaults to `true`.
- Use relative public paths in release examples.
- Use `cannot_read` to protect private memory, secrets, and independent-review isolation.
- Do not include unauthorized private memory, credentials, raw private logs, or full chat history.
- If a runtime executes from this packet, it remains the execution layer and must return evidence.

## Field Reference

- `to_pal_candidate`: candidate recipient chosen by current AI judgement, not a permanent route.
- `can_read`: exact files, summaries, outputs, or evidence the recipient may use.
- `cannot_read`: excluded material, including full chat history and unrelated memory.
- `can_receive_outputs_from`: accepted prior final reports or summaries the recipient may read.
- `needed_output`: the exact response expected from the recipient.
- `verification_requirements`: evidence or checks required before the packet result can be accepted.
- `privacy_policy`: how sensitive context is excluded, summarized, or explicitly approved.
