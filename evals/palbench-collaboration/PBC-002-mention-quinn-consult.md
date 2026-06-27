# PBC-002 Mention Quinn Consult

## User Input

```text
I have a completion report. @Quinn check whether the evidence is enough.
```

## Expected Context Packet

- mode: consult
- to_pal_candidate: Quinn
- explicit_user_call.type: "@Pal"
- owner_status: consultant_candidate or reviewer_candidate
- return_to: current owner or Mira
- final_report_required: true
- needed_output: evidence sufficiency review
- can_read: completion report, acceptance criteria, evidence attachments
- cannot_read: full chat history, owner draft reasoning, private memory, secrets

## Expected Workflow

Current owner remains responsible. Quinn gives bounded verification advice.

## Expected Output

- Quinn consult report;
- pass/fail/partial/not-run/blocker language;
- evidence gaps;
- no owner transfer unless user requests it.

## Failure Modes

- `@Quinn` becomes automatic handoff;
- Quinn reads only the conclusion;
- not-run items are smoothed into pass.

## Scoring Rubric

Score 0 / 1 / 2 for consult default, packet completeness, evidence review, not-run honesty, and ownership preservation.
