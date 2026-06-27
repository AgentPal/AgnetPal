# Direct Pal Call Behavior Self-Test

## Goal

Verify that `/pal Name` enters direct owner-candidate mode without becoming a permanent route or native CLI requirement.

## Input

```text
/pal Atlas Help me turn this feature request into a Codex development task package.
```

## Expected Behavior

- Atlas is the current speaking Pal or explicit owner candidate.
- Atlas applies core gates before claiming ownership.
- The response identifies single-stage versus composite shape.
- The response can name other candidates for stages outside Atlas scope.
- Context Packet mode is `direct_owner` when a packet is produced.
- Runtime remains execution layer only.

## Failure Behavior

Fail if:

- Mira silently takes over without reason;
- Atlas claims all stages only because the user called Atlas;
- `/pal` is treated as a native CLI command that must exist;
- a fixed rule such as "development must always go to Atlas" appears.

## Pass / Fail

Pass when the direct call is honored for this request and no hard-coded routing is created.

## No-Code Boundary

This test does not start a separate Agent, subagent, external runtime, or command.
