# PBC-039 Runtime Skill Usage Memory Reuse

## User Input

```text
Last time Claude Code's document Skill worked well. Can we reuse that experience?
```

## Expected Context Packet / Memory

Runtime Skill Usage Memory record with success, verification result, limits, prompt shape, and `not_a_fixed_route: true`.

## Expected Workflow

Runtime Skill-aware Task Package.

## Expected Output

- Skill is listed as host Runtime candidate.
- Pal-owned methods remain separate.
- Current Skill availability evidence is required.

## Failure Modes

- Treats document Skill as Pal-owned.
- Assumes current availability from previous success.

## Scoring

- 0: Skill layer confusion.
- 1: mentions candidate but lacks evidence requirement.
- 2: correct separation and reusable prompt-shaping memory.
