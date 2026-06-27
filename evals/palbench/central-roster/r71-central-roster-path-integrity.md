# R71 Central Roster Path Integrity

## Case ID

R71-CENTRAL-ROSTER-PATH-INTEGRITY

## Goal

Verify that current root entries, docs, templates, and clean-copy checks use the central roster paths and official Pal Pack paths.

## Setup

- Use the R71 dirty worktree after R68/R69/R70 migrations.
- Do not rely on old root `pals/`, `contacts/`, or `registry/` as current source of truth.

## Evidence Paths

- `workspace/organization/contacts/pals.json`
- `workspace/organization/contacts/PAL_CONTACTS.md`
- `workspace/organization/contacts/aliases.json`
- `official/pals/`
- `README.md`
- `AGENTS.md`
- `PAL.md`
- `SKILL.md`
- `RESOURCE_INDEX.md`
- `release/fresh-clone-checks/r71-clean-copy-validation.md`

## Expected Result

- Root entries point to `workspace/organization/contacts/` as the roster source of truth.
- Pal Pack paths point to `official/pals/`.
- Legacy `contacts/` and `registry/` references are explicitly compatibility or historical references.
- `pals.json` includes `routing_policy: ai_judgement_only` and `keyword_routing_allowed: false`.

## Forbidden Result

- Current root entries instruct users to use old `contacts/` or `registry/` as active source of truth.
- Current docs instruct users to use old root `pals/` as the active Pal asset path.
- A clean copy lacks central contacts or official Pal Pack paths.

## R71 Verification Notes

Use `rg "official/pals|workspace/organization/contacts|templates/project-binding|standards/project-binding"` and JSON parse checks as evidence.

