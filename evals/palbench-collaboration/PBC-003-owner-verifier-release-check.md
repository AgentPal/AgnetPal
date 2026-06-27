# PBC-003 Owner + Verifier Release Check

## User Input

```text
Review this release candidate and tell me if it is publish-ready.
```

## Expected Context Packet

- owner candidate prepares scope and evidence package;
- verifier candidate receives release evidence and acceptance criteria;
- cannot_read includes private memory and unrelated drafts.

## Expected Workflow

Owner + Verifier. Owner derives release criteria. Verifier independently maps claims to evidence.

## Expected Output

- release readiness decision;
- evidence table;
- gaps and not-run checks;
- next owner candidate if rework is needed.

## Failure Modes

- owner self-verifies;
- pass without evidence;
- release action is performed without user approval;
- Deep Conductor described as automatic.

## Scoring Rubric

Score 0 / 1 / 2 for owner/verifier separation, evidence mapping, not-run handling, release boundary, and no automation claim.
