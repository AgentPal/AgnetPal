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
from_pal: Mira
to_pal_candidate: Quinn
mode: verification
task_summary: "Review release evidence and decide pass/fail/partial/not-run/blocked."
can_read:
  - "release readiness file"
  - "release draft"
  - "command outputs returned by runtime"
cannot_read:
  - "private memory"
  - "secrets"
  - "unrelated Pal drafts"
needed_output: "quality decision with evidence map and gaps"
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
