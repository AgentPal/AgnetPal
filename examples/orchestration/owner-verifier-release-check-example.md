# Owner + Verifier Release Check Example

This synthetic example shows v0.3 Owner + Verifier as a no-code staged workflow.

## User Input

```text
Check whether this release candidate is ready to publish.
```

## Task Judgement

- Task shape: release-quality review.
- Owner candidate: Mira, because the request needs release coordination and evidence inventory.
- Verifier candidate: Quinn, because acceptance depends on independent evidence review.
- Runtime candidate: current Markdown/JSON-capable host runtime for reading files and running approved checks.

These are candidates for this example, not fixed routes.

## Owner Stage

Mira prepares:

- release scope summary;
- files to inspect;
- checks to run;
- required evidence;
- do-not-do list: no push, no tag, no release unless user explicitly asks.

## Verifier Context Packet

```yaml
schema: agentpal.context-packet.v0.3
packet_id: cp-owner-verifier-release-001
created_at: YYYY-MM-DD
from_pal: Mira
to_pal_candidate: Quinn
mode: review
explicit_user_call:
  type: "none"
  raw_text: ""
owner_status: verifier_candidate
user_goal: "Check whether this release candidate is ready to publish."
task_summary: "Review release evidence and decide pass/fail/partial/not-run/blocked."
current_state:
  status: "release evidence is being reviewed"
constraints:
  - "No push, tag, or release."
relevant_files:
  - path: "docs/09-roadmap/v0.3-task-pool.md"
    purpose: "synthetic release planning context"
can_read:
  - "release readiness file"
  - "release draft"
  - "command outputs returned by runtime"
cannot_read:
  - "private memory"
  - "secrets"
  - "unrelated Pal drafts"
can_receive_outputs_from:
  - "Mira release scope summary"
needed_output: "quality decision with evidence map and gaps"
output_contract: "decision, evidence reviewed, claims proven, claims not proven, risks, required rework"
verification_requirements:
  - "release claims map to evidence"
privacy_policy: "public-safe; sensitive context excluded"
sensitive_context: "none"
expiration: "single workflow"
handoff_notes: "Quinn is a verifier candidate for this case, not a fixed release route."
return_to: Mira
final_report_required: true
```

## Expected Quinn Output

- decision: pass, fail, partial, not-run, or blocked;
- evidence reviewed;
- claims proven;
- claims not proven;
- risk and next owner candidate.

## Failure Modes

- verifier reads only owner conclusion;
- pass is claimed without command/file evidence;
- not-run checks are hidden;
- release action is performed without user approval.
