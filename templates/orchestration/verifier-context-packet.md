# Verifier Context Packet Template

Use this packet to give a verifier candidate enough bounded context to check evidence without copying the full conversation or relying on an owner self-report.

```yaml
schema: agentpal.verifier-context-packet.v0.3
packet_id:
from_pal:
to_verifier_candidate:
verification_mode:
user_goal:
owner_pal:
owner_claim:
expected_deliverables:
  - <deliverable>
acceptance_criteria:
  - <criterion>
evidence_to_check:
  - type:
    source:
    expected_signal:
allowed_files:
  - <path-or-pattern>
cannot_read:
  - private_user_memory
  - unrelated_pal_assets
  - secrets
  - full_chat_history_by_default
known_risks:
  - <risk>
false_completion_patterns:
  - completion_report_treated_as_evidence
  - owner_claim_without_artifact_or_command_output
  - hidden_not_run_check
needed_output:
  - verdict
  - missing_evidence
  - risks
  - repair_required
  - confidence
return_to:
```

`to_verifier_candidate` is a candidate selected for the current case, not a permanent route. The verifier should request missing evidence instead of guessing a pass. The verifier should not read full chat history or private memory by default.
