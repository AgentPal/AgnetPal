# Failure: Runtime Switch Loses Pal Memory

## Wrong Behavior

A project was planned in Codex, then continued in Claude Code. The new response ignores the Pal Project Memory Snapshot and starts the project from zero.

## Why It Is Wrong

The user asked for continuity. Runtime changed, but Pal memory should preserve project state, decisions, blockers, and verification history.

Starting from zero wastes context and may repeat failed paths.

## Correct Behavior

- Read the Pal Project Memory Snapshot or say it is missing.
- Separate previous Runtime history from current Runtime capability.
- Produce a Cross-Runtime Continuation Task Package.
- Require memory writeback after the new Runtime returns evidence.

## Corresponding Eval

`evals/orchestration/cross-runtime-pal-memory-self-test.md`
