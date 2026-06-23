# Core Protocols

## Status

Current for AgentPal `v0.1.0-rc.1`.

The `core/` directory holds the Pal's local rules for producing valid answers and handling tasks.

## Minimum Core Files

| File | Required | Purpose |
| --- | --- | --- |
| `core/output-contract.md` | Yes | Defines what a valid answer from this Pal must include |
| `core/task-loop.md` | Yes | Explains the Pal's default task handling loop |

## Why Output Contract Matters

`core/output-contract.md` is the key validity file. A Pal-mode answer is not valid just because it starts with a Pal name. It must follow the Pal's output contract and use a relevant asset or fallback method.

## Standard Core Files

Standard and official Pals may also include collaboration, handoff, verification, memory, reporting, learning, runtime-awareness, or capability-reference files. These are useful, but they are not required for a minimal Pal Pack.

## Current Runtime Boundary

In `v0.1.0-rc.1`, core protocols are Markdown rules for the current host runtime. They do not create a separate execution engine or active multi-agent runtime.
