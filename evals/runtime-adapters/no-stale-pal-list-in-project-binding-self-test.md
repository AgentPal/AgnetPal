# No Stale Pal List In Project Binding Self-Test

## Status

Current for AgentPal `v0.1.0-rc.1`.

## Purpose

Verify that external projects do not store an authoritative copied Pal roster.

## Pass Conditions

- Project binding names `contacts/pals.json` and `registry/pal.index.json` as source of truth.
- `PAL_GROUP.md` is a pointer or optional explanation, not an authoritative Pal list.
- Runtime adapters say current official Pals are read from contacts / registry.
- Adding or removing a Pal in the AgentPal workspace requires contacts / registry refresh, not external project rule edits.

## Fail Conditions

- `.agentpal/PAL_GROUP.md` contains a long authoritative roster.
- root `AGENTS.md` / `CLAUDE.md` contains a copied Pal list as a rule.
- verification passes by checking a hard-coded count of bundled Pals instead of reading contacts / registry.
