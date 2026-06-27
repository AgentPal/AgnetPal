# Owner + Verifier Doc Update Verification

This synthetic example shows independent verification for a documentation change.

## User Input

```text
Update the orchestration guide and verify the result against the requested headings.
```

## Owner Candidate

Morgan is the owner candidate because the requested deliverable is documentation structure and clarity.

## Verifier Candidate

Quinn is the verifier candidate because the user asks for acceptance verification against headings and evidence.

## Owner Output

```yaml
owner_pal_candidate: Morgan
owner_claim: "The orchestration guide now includes all requested sections."
expected_deliverables:
  - updated guide
  - heading checklist
acceptance_criteria:
  - every requested heading is present
  - no unrelated sections were removed
  - no current runtime capability is overstated
evidence_required_for_verification:
  - changed guide path
  - heading scan
  - diff summary
```

## Verifier Context Packet

```yaml
schema: agentpal.verifier-context-packet.v0.3
packet_id: vcp-doc-update-001
from_pal: Morgan
to_verifier_candidate: Quinn
verification_mode: acceptance_check
user_goal: "Verify the updated guide against requested headings."
owner_pal: Morgan
owner_claim: "All requested headings are present."
expected_deliverables:
  - updated orchestration guide
acceptance_criteria:
  - "Requested headings are present."
  - "No future runtime is described as current automatic behavior."
  - "No unrelated docs were changed."
evidence_to_check:
  - type: file_content
    source: "updated guide"
    expected_signal: "heading list present"
  - type: diff
    source: "git diff --name-only"
    expected_signal: "scoped documentation change"
allowed_files:
  - "docs/05-orchestration-methodology/"
cannot_read:
  - private_user_memory
  - secrets
known_risks:
  - "future design language presented as current runtime"
false_completion_patterns:
  - completion_report_treated_as_evidence
needed_output:
  - verdict
  - missing_evidence
  - risks
  - repair_required
  - confidence
return_to: Morgan
```

## Verification Result Record

```yaml
schema: agentpal.verification-result-record.v0.3
verification_id: vrr-doc-update-001
verifier_candidate: Quinn
mode: acceptance_check
verdict: pass
confidence: medium
checked_evidence:
  - evidence: "heading scan"
    source: "file read"
    result: "all requested headings present"
  - evidence: "diff summary"
    source: "runtime output"
    result: "docs-only"
missing_evidence: []
risks:
  - "Future copied guides should repeat the boundary note."
false_completion_caught:
  caught: false
  pattern:
required_repairs: []
recommended_next_step: "Owner may provide final summary."
return_to: Morgan
notes: "Pass is limited to the supplied guide and diff evidence."
```

## Mira / Owner Synthesis

Morgan reports the pass verdict, evidence checked, residual risk, and final doc path.

## Good Behavior

- Verification uses the changed file and diff, not only the doc owner's statement.
- Future runtime claims are checked.

## Bad Behavior

- Saying "guide updated" without heading evidence.
- Accepting a pass after only reading the completion report.

## Acceptance Criteria

- All requested sections appear.
- Result record verdict is evidence-backed.
- Synthesis preserves the verifier confidence.

## No-Code Boundary Note

This is a documentation verification workflow. It does not activate automatic orchestration.
