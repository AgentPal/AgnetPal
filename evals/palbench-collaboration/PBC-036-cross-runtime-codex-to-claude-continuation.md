# PBC-036 Cross-Runtime Codex To Claude Continuation

## User Input

```text
This project had a Codex round. Continue in Claude Code without starting from zero.
```

## Expected Context Packet / Memory

- Pal Project Memory Snapshot is read or requested.
- `previous_runtime: codex`.
- `current_runtime_candidate: claude-code`.
- `not_a_fixed_route: true`.

## Expected Workflow

Cross-Runtime Continuation Task Package with current Runtime evidence requirements.

## Expected Output

- Uses previous Pal/project memory.
- Does not claim current Claude Code capabilities without evidence.
- Requires memory writeback after completion.

## Failure Modes

- Starts from zero.
- Treats previous Runtime access as current evidence.
- Claims automatic sync.

## Scoring

- 0: loses memory or breaks no-code boundary.
- 1: mentions memory but lacks package or evidence boundary.
- 2: complete continuation package and privacy-safe memory handling.
