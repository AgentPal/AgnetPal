# Owner + Verifier PalSmith Created Pal Health Check

This synthetic example shows a Pal creation health check after PalSmith prepares a Pal Pack.

## User Input

```text
PalSmith created a Pal. Arrange independent acceptance review before I use it.
```

## Owner Candidate

PalSmith is the owner candidate because the claim concerns a generated or repaired Pal Pack.

## Verifier Candidate

Quinn is the verifier candidate because the user asks for quality acceptance evidence. Another quality-capable Pal could be chosen in a different case.

## Owner Output

```yaml
owner_pal_candidate: PalSmith
owner_claim: "The created Pal Pack has required identity, output contract, examples, and boundaries."
expected_deliverables:
  - Pal Pack health summary
  - required file inventory
  - known gaps
acceptance_criteria:
  - PAL.md exists
  - pal.json is valid JSON if present
  - core/output-contract.md exists
  - examples or fallback method are present
  - no private data is included
evidence_required_for_verification:
  - file inventory
  - JSON parse result
  - output contract read
  - privacy risk notes
```

## Verifier Context Packet

```yaml
schema: agentpal.verifier-context-packet.v0.3
packet_id: vcp-palsmith-health-001
from_pal: PalSmith
to_verifier_candidate: Quinn
verification_mode: acceptance_check
user_goal: "Review a created Pal before use."
owner_pal: PalSmith
owner_claim: "The Pal Pack is healthy enough to use."
expected_deliverables:
  - health check verdict
acceptance_criteria:
  - "Required Pal files are present."
  - "JSON files parse."
  - "Output contract is usable."
  - "No private data appears in public assets."
evidence_to_check:
  - type: file_inventory
    source: "created Pal directory listing"
    expected_signal: "required files present"
  - type: json_check
    source: "pal.json parse result"
    expected_signal: "valid JSON"
  - type: content_read
    source: "core/output-contract.md"
    expected_signal: "clear output rules"
allowed_files:
  - "created Pal Pack path supplied by owner"
cannot_read:
  - private_user_memory
  - unrelated Pal Packs
  - secrets
known_risks:
  - "Generated Pal looks complete but lacks output contract"
false_completion_patterns:
  - completion_report_treated_as_evidence
  - owner_claim_without_artifact_or_command_output
needed_output:
  - verdict
  - missing_evidence
  - risks
  - repair_required
  - confidence
return_to: PalSmith
```

## Verification Result Record

```yaml
schema: agentpal.verification-result-record.v0.3
verification_id: vrr-palsmith-health-001
verifier_candidate: Quinn
mode: acceptance_check
verdict: fail
confidence: high
checked_evidence:
  - evidence: "file inventory"
    source: "directory listing"
    result: "PAL.md present, output contract missing"
missing_evidence:
  - "core/output-contract.md"
risks:
  - "Pal may answer without a stable output contract."
false_completion_caught:
  caught: true
  pattern: owner_claim_without_artifact_or_command_output
required_repairs:
  - "Add or repair core/output-contract.md."
recommended_next_step: "Return to PalSmith for repair package."
return_to: PalSmith
notes: "Fail is based on missing required artifact."
```

## Mira / Owner Synthesis

PalSmith accepts the verifier result, prepares a repair package for the missing output contract, and returns the repaired Pal for re-check.

## Good Behavior

- PalSmith owns creation and repair.
- Verifier checks the actual Pal Pack evidence.
- Missing output contract becomes a failed criterion.

## Bad Behavior

- Accepting "created successfully" as proof.
- Reading unrelated Pal Packs to infer health.

## Acceptance Criteria

- Required files are checked.
- Missing required assets are named.
- Repair package is created after failure.

## No-Code Boundary Note

This workflow reviews Pal Pack assets. It does not install, activate, or run an external Agent.
