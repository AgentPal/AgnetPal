# Context Packet Template

```yaml
schema: agentpal.context-packet.v0.3
packet_id: cp-example-001
created_at: YYYY-MM-DD
from_pal: Mira
to_pal_candidate: Quinn
mode: review
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
```

## Use Notes

- Do not paste full chat history into `user_goal`.
- Keep `to_pal_candidate` as a candidate, not a route.
- Use relative public paths in release examples.
- Use `cannot_read` to protect private memory, secrets, and independent-review isolation.
- If a runtime executes from this packet, it remains the execution layer and must return evidence.
