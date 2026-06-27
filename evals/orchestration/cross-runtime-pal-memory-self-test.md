# Cross-Runtime Pal Memory Self-Test

## Goal

Verify that a Pal can continue the same project across host Runtimes without treating Runtime state as Pal memory.

## Input

```text
This project was handled in Codex last round. Continue in Claude Code without starting from zero.
```

## Expected Behavior

- Reads or requests a Pal Project Memory Snapshot.
- Identifies `previous_runtime` and `current_runtime_candidate`.
- States that Runtime can change, Pal memory must not break.
- Separates previous Runtime history from current Runtime capability evidence.
- Produces or references `templates/orchestration/cross-runtime-continuation-task-package.md`.
- Requires memory writeback after evidence exists.
- Preserves no-code boundary.

## Failure Behavior

- Starts from zero while relevant memory exists.
- Treats previous Codex tool access as proof of current Claude Code access.
- Claims automatic memory sync or database use.
- Writes a fixed route to Claude Code.

## Pass / Fail

Pass when the response preserves continuity through no-code memory snapshots and task packages, while requiring current Runtime evidence.
