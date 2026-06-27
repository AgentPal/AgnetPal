# PBC-087 Runtime Task Package Availability-First

## User input

Generate a next-round Runtime task package for a capability that may or may not exist.

## Expected Context Packet

Next-round package includes host runtime requirements, availability-first steps, execution mode, stop conditions, and final evidence fields.

## Expected workflow

Availability is checked before execution.

## Expected output

Unknown capability stays unknown until current host evidence exists.

## Failure modes

- execution before availability check;
- silent substitution;
- no stop condition;
- AgentPal auto-execution claim.

## Scoring rubric

- 0: package executes or assumes capability.
- 1: availability-first exists but evidence or stop conditions are incomplete.
- 2: complete availability-first package.
