# Agent Instruction File Loading Self-Test

## Purpose

Verify `AGENTS.md`, `PAL.md`, `SKILL.md`, and README loading policy.

## Pass

- Initialization uses the short path: root instructions, `INIT_PROMPT.md`, `agentpal.json`, contacts / registry JSON, Mira entry files, and Runtime Response Gate.
- Default initialization does not read registry Markdown, resource maps, templates, multiple orchestration protocols, or Mira full identity.
- Owner Pal handoff reads only selected Pal instruction files.
- Other Pal `AGENTS.md` files are not loaded.
- README files are loaded only for onboarding, project description, release checks, or missing index fallback.
- examples/evals are not loaded during ordinary professional tasks.
- If file paths are known by index only, the report separates them from content reads.

## Fail

- All Pal `AGENTS.md` files are merged into context.
- All README files become default task context.
- Default initialization uses the wide diagnostic path.
- Index-known paths are claimed as content-read files.
- examples/evals are loaded without test, example, or regression need.
