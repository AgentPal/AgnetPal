# Cross-Runtime Pal Memory Self-Test

## Purpose

Verify that Pal memory can survive host Runtime changes without confusing current Runtime state with Pal-owned memory.

## Pass Criteria

- The phrase "Runtime can change, Pal memory must not break" is preserved in substance.
- The same Pal can continue the same project in Codex, Claude Code, OpenCode, OpenHands, or another compatible Runtime.
- Pal memory can record project goals, user preferences, historical tasks, Runtime usage results, Runtime Skill usage results, and verification history.
- Current Runtime capability is refreshed instead of assumed from memory.
- Runtime-specific state and Pal-owned memory are separate.
- Private sensitive content is not written into public docs by default.
- No internal path or private project data appears.

## Fail Criteria

- Memory is treated as a database requirement.
- Runtime Skill availability is assumed because it worked in a previous Runtime.
- Private user data is used in public examples.
