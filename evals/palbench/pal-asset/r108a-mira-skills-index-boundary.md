# R108-A Mira Skills Index Boundary

Date: 2026-06-28

## Purpose

This eval checks that R108-A backfills Mira `skills/index.md` without changing
Mira behavior, central contacts, official Pal metadata, manifests, or external
project thin-binding boundaries.

## Pass Criteria

- Mira is resolved from `workspace/organization/contacts/pals.json`.
- Mira `pack_path` is `official/pals/Mira-main`.
- Mira root entries are present: `README.md`, `PAL.md`, `AGENTS.md`,
  `SKILL.md`, and `pal.json`.
- Mira `pal.json` parses and remains unchanged.
- `official/pals/Mira-main/skills/index.md` exists.
- Mira skills index states:
  - Mira Pal Skills are default-entry, task clarification, project-binding
    understanding, Context Packet / Task Package organization, Pal
    collaboration coordination, and lightweight secretary-style reporting
    capabilities;
  - Mira Pal Skills are not Runtime Agent Skills;
  - Mira does not directly edit files, run commands, or call external APIs;
  - Mira does not hard-route tasks to specialist Pals by keyword;
  - Mira may use AI judgement with central roster, Capability Inventory,
    project context, and relevant Pal / Org assets to propose candidate Pals,
    workflows, Runtime capabilities, and verification paths;
  - Agent Skill / Runtime Tool references remain references and are not copied
    into Mira `skills/`;
  - credentials, tokens, cookies, passwords, API keys, and secrets are
    forbidden;
  - external project `.agentpal/skills/` is not a default target.
- Central roster parses and remains 9 registered / 9 active Pals.
- Official Pal directory count remains 9.
- All official Pal `pal.json` files parse.
- No central contacts file changes.
- No official Pal `pal.json` file changes.
- No official `asset-manifest.json` is generated.
- No keyword, fixed topic, or deterministic semantic route is introduced.
- No direct execution, connector, scanner, validator program, daemon,
  installer, marketplace, hub, auto-sync, or auto-execution behavior is
  introduced.
- No credential, token, cookie, password, API key, secret, private project data,
  private user memory, or customer data is introduced.
- No external project `.agentpal/` thick-binding directory is created or
  modified.
- Clean-copy validation passes.

## Fail Conditions

- Mira cannot be resolved from the central roster.
- Mira skills index is missing.
- Any official Pal `pal.json` changes.
- Central contacts change.
- A real `asset-manifest.json` appears under `official/pals/**`.
- The skills index claims runtime execution, automatic routing, connector
  behavior, scanning, validation, or external system behavior.
- The skills index requires copying Mira assets into external project
  `.agentpal/` directories by default.
- The skills index contains private data, credentials, or deterministic Pal
  routes.
- R108-A moves, deletes, renames, or reclassifies existing Mira assets.

## Required Evidence

Record evidence in:

- `release/integration-notes/r108a-mira-skills-index-summary.md`
- `release/fresh-clone-checks/r108a-local-mira-skills-index-validation.md`
