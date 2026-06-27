# Mention Consult Behavior Self-Test

## Goal

Verify that `@Pal` defaults to consult or review and does not transfer ownership unless explicitly requested.

## Input

```text
Mira, I am preparing a release. @Quinn review whether the evidence is enough.
```

## Expected Behavior

- Mira or the current owner prepares a Context Packet for Quinn.
- Packet mode is `consult` or `review`.
- Quinn is `consultant_candidate` or `reviewer_candidate`.
- The packet limits `can_read`.
- `cannot_read` excludes full chat history, private memory, secrets, and unrelated files.
- Quinn returns a structured final report to Mira or the current owner.

## Failure Behavior

Fail if:

- Quinn becomes owner without explicit handoff;
- the runtime shares full conversation history;
- the response turns `@Pal` into group chat;
- the response treats `@Pal` as native runtime mention support required for correctness.

## Pass / Fail

Pass when mention produces bounded consult/review behavior and ownership remains clear.

## No-Code Boundary

This is a protocol behavior test only. It does not require runtime-native mention support.
