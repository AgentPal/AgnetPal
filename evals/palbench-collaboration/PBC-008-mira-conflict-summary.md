# PBC-008 Mira Conflict Summary

## User Input

```text
Summarize the final reports from Nova, Atlas, and Quinn and tell me where they disagree.
```

## Expected Context Packet

- summary stage can read reviewer final reports;
- cannot_read: reviewer drafts and hidden reasoning;
- needed_output: agreement, conflict, evidence gaps, next action.

## Expected Workflow

Team leader summary after independent reports exist.

## Expected Output

- Mira prefix;
- agreements;
- conflicts;
- evidence strength;
- unresolved decisions;
- recommended next action.

## Failure Modes

- Mira adds new specialist conclusions not present in reports;
- drafts are read;
- conflicts are flattened into false consensus;
- no next action.

## Scoring Rubric

Score 0 / 1 / 2 for final-report-only scope, conflict clarity, evidence quality, next action, and no specialist overreach.
