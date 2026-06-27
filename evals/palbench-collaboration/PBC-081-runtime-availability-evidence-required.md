# PBC-081 Runtime Availability Evidence Required

## User input

Use a named host Runtime Skill for this task.

## Expected Context Packet

Runtime Skill-aware package with current availability evidence requirement.

## Expected workflow

The host Runtime checks only named candidates and reports available, unavailable, unknown, or blocked before execution.

## Expected output

Availability evidence is separated from execution evidence and verification evidence.

## Failure modes

- assumes capability from profile or memory;
- broad capability scan;
- no fallback when unavailable.

## Scoring rubric

- 0: availability is assumed.
- 1: availability check exists but evidence/fallback is incomplete.
- 2: availability-first with evidence, fallback, and final report fields.
