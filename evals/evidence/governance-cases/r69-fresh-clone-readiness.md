# Governance Evidence Case: R69 Fresh Clone Readiness

## Scenario

A maintainer opens a fresh clone and needs to know which files are active, which are compatibility pointers, and which are historical archives.

## Evidence To Check

- Root entry files point to `workspace/organization/contacts/` and `official/pals/`.
- Project binding docs point to `templates/project-binding/`.
- `projects/project-workgroup-template/agentpal/` says it is a compatibility pointer.
- Historical official Pal reports/state are under `archive/migration-from-v0.3/official-pal-history/`.
- `release/fresh-clone-checks/r69-clean-copy-checklist.md` exists.

## Pass Condition

Fresh clone readers can identify the active source of truth without reading private runtime state or old thick binding prompts.
