# Owner + Verifier Dev Task Example

This synthetic example shows a development task with a separate verification review.

## User Input

```text
Update the docs for the adapter prompt and have someone verify the change.
```

## Owner Candidate

Atlas is the owner candidate because this case needs developer-facing change planning and implementation-shaped acceptance criteria.

## Verifier Candidate

Quinn is the verifier candidate because the user asked for independent quality verification of the completed change.

## Owner Output

```yaml
owner_pal_candidate: Atlas
owner_claim: "The adapter prompt docs were updated and no runtime behavior was changed."
expected_deliverables:
  - changed adapter prompt document
  - evidence that no runtime files changed
acceptance_criteria:
  - documentation explains the new prompt behavior
  - no code, scripts, installers, or CLI files are added
  - changed files are listed
evidence_required_for_verification:
  - git diff summary
  - changed file paths
  - no-runtime file extension check
```

## Verifier Context Packet

```yaml
schema: agentpal.verifier-context-packet.v0.3
packet_id: vcp-dev-task-001
from_pal: Atlas
to_verifier_candidate: Quinn
verification_mode: evidence_audit
user_goal: "Update adapter prompt docs and verify the change."
owner_pal: Atlas
owner_claim: "Docs changed; runtime files did not."
expected_deliverables:
  - adapter documentation update
acceptance_criteria:
  - "Only Markdown docs changed."
  - "No runtime dependency or script was added."
evidence_to_check:
  - type: diff
    source: "git diff --name-status"
    expected_signal: "Markdown-only change"
  - type: file_content
    source: "changed adapter prompt doc"
    expected_signal: "mentions no-code boundary"
allowed_files:
  - "core/runtime-adapter-shared-contract.md"
  - "prompts/"
cannot_read:
  - private_user_memory
  - unrelated_pal_assets
known_risks:
  - "doc update smuggling a runtime feature claim"
false_completion_patterns:
  - owner_claim_without_artifact_or_command_output
needed_output:
  - verdict
  - missing_evidence
  - risks
  - repair_required
  - confidence
return_to: Atlas
```

## Verification Result Record

```yaml
schema: agentpal.verification-result-record.v0.3
verification_id: vrr-dev-task-001
verifier_candidate: Quinn
mode: evidence_audit
verdict: pass
confidence: high
checked_evidence:
  - evidence: "git diff --name-status"
    source: "runtime output"
    result: "Markdown-only"
  - evidence: "changed prompt text"
    source: "file read"
    result: "no-code boundary present"
missing_evidence: []
risks:
  - "Future adapter docs may drift if copied manually."
false_completion_caught:
  caught: false
  pattern:
required_repairs: []
recommended_next_step: "Owner can summarize the verified change."
return_to: Atlas
notes: "Pass is evidence-backed."
```

## Mira / Owner Synthesis

Atlas summarizes the verified doc change, includes Quinn's pass verdict, and names the evidence checked.

## Good Behavior

- Development owner and verifier have different jobs.
- Verification checks the diff and the content.
- Pass is tied to evidence.

## Bad Behavior

- Verifier only repeats "Atlas says it is done."
- A runtime feature is described as current behavior without evidence.

## Acceptance Criteria

- Owner output defines work and evidence.
- Verifier result maps evidence to criteria.
- Runtime remains only an execution layer.

## No-Code Boundary Note

This example uses docs and evidence only. It does not create a script, scanner, validator, CLI, UI, daemon, or service.
