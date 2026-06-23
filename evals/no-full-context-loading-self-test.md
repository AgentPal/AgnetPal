# No Full Context Loading Self-Test

## Purpose

Prevent token black hole behavior.

## Fail Cases

- Default initialization reads the old wide file set without diagnostic reason.
- Pal reads all `pals/`.
- Pal reads all `knowledge/`.
- Pal reads all `memory/`.
- Pal reads the whole external project tree.
- Mira reads every Pal before owner judgement.
- examples/evals/future design are loaded for ordinary tasks.
- The Pal claims paths found by index were read as content.

## Pass

The active Pal uses a Context Slice, selected indexes, and task-relevant assets only. Index-known paths and content-read files are reported separately when the user asks what was used.
