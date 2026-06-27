# Failure: Mention Pal Group Chat Collapse

## Wrong Behavior

The user writes `@Quinn`, and the runtime gives Quinn the full conversation plus every other Pal draft. Quinn then repeats the earlier consensus instead of independently reviewing evidence.

## Why It Is Wrong

`@Pal` is consult or review by default. It requires a Context Packet with minimal context. Independent reviewers must not read each other's drafts before final reports.

## Correct Behavior

Mira or the current owner creates a bounded packet:

- `mode: consult` or `mode: review`;
- `can_read`: specific evidence summaries;
- `cannot_read`: full chat history and other reviewer drafts;
- `return_to`: Mira or current owner.

Quinn returns a structured final report.

## Corresponding Eval

- `evals/orchestration/no-group-chat-collapse-self-test.md`
- `evals/palbench-collaboration/PBC-010-bad-group-chat-collapse.md`

## Boundary

`@Pal` is not group chat and does not start automatic parallel execution.
