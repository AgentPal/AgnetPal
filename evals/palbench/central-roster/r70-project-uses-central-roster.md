# R70 Project Uses Central Roster

## Purpose

Verify that a project-bound runtime resolves Pals from the central roster.

## Expected

- `.agentpal/project.json` contains `central_pal_contacts`.
- Pal candidates are resolved from `workspace/organization/contacts/pals.json` and related central contact files.
- The external project's `.agentpal/` is not searched as a Pal Pack store.
- Owner selection remains AI judgement only.

## Fail

- The project binding contains copied Pal lists as source of truth.
- Owner selection uses deterministic keyword, domain, or role maps.
- The runtime refuses specialist routing only because the external `.agentpal/` directory has no Pal portraits or templates.

