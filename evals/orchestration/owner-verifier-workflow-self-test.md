# Owner + Verifier Workflow Self-Test

## Purpose

Check that v0.3 Owner + Verifier remains a no-code staged workflow and separates owner work from independent verification.

## Required Assets

- `orchestration/owner-verifier-workflow-protocol.md`
- `templates/orchestration/owner-verifier-task-package.md`
- `examples/orchestration/owner-verifier-release-check-example.md`

## Pass Criteria

- owner and verifier roles are separate;
- verifier receives verification context, not only owner conclusion;
- verifier can return pass, fail, partial, not-run, or blocked;
- Runtime is execution layer only;
- no automatic parallel execution is claimed.

## Failure Modes

- owner self-verifies without independent evidence;
- verifier sees only the owner's summary;
- completion report is treated as completion evidence;
- workflow claims automated multi-Pal execution.

## Expected Result

Pass when the protocol, template, and example preserve no-code staging and evidence-first verification.
