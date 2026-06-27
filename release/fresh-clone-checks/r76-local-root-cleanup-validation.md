# R76 Local Root Cleanup Validation

Date: 2026-06-28

This is a local root-structure cleanup validation for the AgentPal workspace.

This is not a GitHub fresh clone check. No `git push`, `git pull`, `git fetch`, `git tag`, `gh release`, GitHub Release action, or release/tag migration was performed for this validation.

## Scope

R76 validates that local root legacy noise was reduced without breaking the v0.4/v0.5 target structure, central Pal roster, thin binding templates, or no-keyword-routing boundary.

## Root Cleanup Result

Moved out of the root:

- `pals/` -> `archive/migration-from-v0.3/root-legacy/pals/`
- `contacts/` -> `archive/migration-from-v0.3/root-legacy/contacts/`
- `registry/` -> `workspace/resources/registry/`

The ignored local file `contacts/collaboration-memory.md` was moved to ignored local `.agentpal/` storage and was not included in public source.

Remaining legacy or current-reference root directories:

- `projects/`
- `prompts/`
- `capabilities/`
- `orchestration/`
- `runtime/`
- `models/`
- `plugins/`
- `imports/`
- `memory/`
- `state/`
- `reports/`
- `response-fingerprints/`

Those remaining directories are classified in:

- `archive/migration-from-v0.3/root-legacy/root-directory-classification.md`

## Target Structure Check

The target visible root directories still exist:

- `standards/`
- `official/`
- `workspace/`
- `templates/`
- `examples/`
- `evals/`
- `release/`
- `archive/`
- `docs/`

## Official Pal And Central Roster Check

- `official/pals/` exists: pass
- official Pal directories: 9
- `workspace/organization/contacts/pals.json` parse: pass
- registered Pals: 9
- `source_of_truth`: `true`
- `routing_policy`: `ai_judgement_only`
- `keyword_routing_allowed`: `false`

## Thin Binding Check

Required project-binding files remain present:

- `templates/project-binding/generic-codex/.agentpal/project.json`
- `templates/project-binding/generic-codex/.agentpal/AGENTPAL.md`
- `templates/project-binding/generic-codex/AGENTS.agentpal-block.md`
- `templates/project-binding/claude-code/CLAUDE.agentpal-block.md`
- `templates/project-binding/claude-code/settings.local.example.json`

Forbidden default thick-binding template directories were not created:

- `.agentpal/memory/`
- `.agentpal/state/`
- `.agentpal/reports/`
- `.agentpal/context/`
- `.agentpal/index/`
- `.agentpal/pals/`
- `.agentpal/workflows/`
- `.agentpal/evals/`

Active thick-binding bug count: 0.

## JSON And Routing Checks

- JSON files checked in local clean copy: 49
- JSON parse failures: 0
- active JSON `keyword_map` / `domain_map` / `role_map` route keys: 0

Text hits for `keyword_map`, `domain_map`, and `role_map` are limited to forbidden, boundary, template-check, archive, or regression-test contexts.

## Local Clean-Copy Result

Local clean-copy validation copied Git-visible files plus visible untracked public assets into a temporary local copy and checked the resulting tree.

- copied file count: 2750
- required paths missing: 0
- JSON files checked: 49
- JSON failures: 0
- private/runtime leak count: 0
- active thick binding bug: 0
- active keyword routing bug: 0
- target root dirs exist: true
- removed old root dirs: `pals/`, `contacts/`, `registry/`
- official Pal dirs: 9
- registered Pals: 9

Result: pass.

## Non-Actions

The following actions were intentionally not performed in R76:

- no `git push`
- no `git pull`
- no `git fetch`
- no tag creation or modification
- no GitHub Release creation or modification
- no release/tag migration
- no CLI, App, scanner, validator, installer, daemon, database, auto-sync, or auto-execution engine creation
- no keyword router or deterministic semantic router
