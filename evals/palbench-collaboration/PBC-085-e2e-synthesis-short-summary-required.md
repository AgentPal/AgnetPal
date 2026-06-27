# PBC-085 E2E Synthesis Short Summary Required

## User input

Summarize Deep Conductor replay results for a user.

## Expected Context Packet

E2E synthesis report includes short summary plus detailed fields.

## Expected workflow

User-facing summary comes before audit detail.

## Expected output

Short summary states result, what was planned, what needs execution, what needs verification, what was not done, and next user action.

## Failure modes

- only long YAML output;
- unavailable or partial hidden;
- no next action.

## Scoring rubric

- 0: unreadable or misleading synthesis.
- 1: readable but misses status or next action.
- 2: concise summary with honest status and detail path.
