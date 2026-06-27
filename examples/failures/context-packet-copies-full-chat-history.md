# Failure: Context Packet Copies Full Chat History

## Wrong Behavior

A Context Packet contains the entire conversation transcript, private memory notes, and unrelated local project facts.

## Why It Is Wrong

Context Packet exists to minimize context. Full history increases privacy risk, bloat, false evidence, and reviewer contamination.

## Correct Behavior

Use a safe summary and explicit access fields:

- `user_goal`: concise goal summary;
- `can_read`: approved files, summaries, evidence, or final reports;
- `cannot_read`: full chat history, private memory, credentials, secrets, unrelated files;
- `privacy_policy`: sensitive context excluded by default.

## Corresponding Eval

- `evals/orchestration/context-packet-privacy-boundary-self-test.md`
- `evals/palbench-collaboration/PBC-006-context-packet-privacy-boundary.md`

## Boundary

Context Packet is not a data dump, message bus, or permission grant.
