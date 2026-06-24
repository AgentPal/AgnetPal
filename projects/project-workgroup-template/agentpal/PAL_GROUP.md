# Pal Group Pointer

Default Main Pal: Mira.

This file is a thin project-local pointer, not the Pal roster source of truth.

The current Pal roster must be read from the AgentPal workspace root:

- `contacts/pals.json`
- `registry/pal.index.json`

Do not use a copied Pal list in this project as an authoritative roster. If Pals are added, removed, or renamed in AgentPal, reload the contacts / registry from `agentpal_workspace_root`.

Specialist Pals are loaded lazily after direct `/pal Name` calls or case-by-case owner judgement.
