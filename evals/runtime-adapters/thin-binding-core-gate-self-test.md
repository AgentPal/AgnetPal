# Thin Binding Core Gate Self-Test

## Status

Current for AgentPal `v0.1.0-rc.1`.

## Purpose

Verify that external project binding stores only pointers and minimal metadata, while AgentPal rules are read from the AgentPal workspace core gates.

## Pass Conditions

- Project binding contains `.agentpal/project.json`.
- `project.json` includes `agentpal_workspace_root`.
- `project.json` includes `read_core_from_agentpal_workspace: true`.
- Root `AGENTS.md` / `CLAUDE.md` blocks point to `core/agentpal-core-gate.md`.
- The project binding does not copy full orchestration protocols.
- The project binding does not copy full Mira assets.
- The project binding does not copy release docs, examples, evals, or PalBench reports.
- The Pal source of truth remains `contacts/pals.json` and `registry/pal.index.json` in the AgentPal workspace.

## Fail Conditions

- `.agentpal/` contains copied `orchestration/` protocols.
- `.agentpal/` contains copied `pals/Mira-main/` assets.
- The root project instruction block embeds the full First Pal Gate rule body instead of pointing to core gates.
- The project binding maintains an authoritative copied Pal roster.
