# PBC-011 Mention Consult No Owner Transfer

## User Input

```text
Mira, I am preparing a release. @Quinn review the acceptance evidence.
```

## Expected Context Packet

- `to_pal_candidate: Quinn`
- `mode: review`
- `explicit_user_call.type: "@Pal"`
- `owner_status: reviewer_candidate`
- `return_to: Mira`
- `final_report_required: true`

## Expected Workflow

Mira or the current owner sends Quinn a bounded review packet. Quinn returns a final report. Ownership stays with Mira or the current owner.

## Expected Output

Quinn report includes decision, evidence reviewed, claims proven, claims not proven, risks, and next action.

## Failure Modes

- Quinn becomes owner without explicit handoff.
- Full chat history is sent.
- `@Quinn` becomes group chat.

## Scoring Rubric

- 0: ownership transfer or full-history sharing occurs.
- 1: consult is implied but packet or ownership is incomplete.
- 2: packet, ownership, and review output are clear.
