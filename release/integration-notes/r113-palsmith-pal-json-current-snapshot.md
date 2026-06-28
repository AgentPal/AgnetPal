# R113 PalSmith pal.json Current Snapshot

Date: 2026-06-28

## Current Path

Resolved from central roster:

`official/pals/PalSmith-pal-governor/pal.json`

## Current Key Summary

| Field | Current value summary |
| --- | --- |
| `schema` | `agentpal.pal-pack.v0.1` |
| `id` | `palsmith-pal-governor` |
| `name` | `PalSmith` |
| `display_name` | `PalSmith / Pal Asset Governor` |
| `directory_name` | `PalSmith-pal-governor` |
| `role` | `pal-asset-governor` |
| `official` / `system_pal` / `no_runtime_code` | `true / true / true` |
| `direct_call` | `/pal PalSmith` |
| `version` | `0.1.0` |
| `type` | `pal-pack` |
| `formal_skill_count` | `15` |
| `entry` | `SKILL.md`, `PAL.md`, `AGENTS.md` |
| `core_capabilities` | present |
| `collaboration` | present |
| `resource_policy` | present |
| `compatible_runtimes` | present |

## Actual Asset Directories

Existing PalSmith directories used for v0.5 `asset_dirs`:

- `checklists/`
- `core/`
- `evals/`
- `examples/`
- `governance/`
- `identity/`
- `knowledge/`
- `memory/`
- `reports/`
- `research/`
- `runbooks/`
- `skills/`
- `state/`
- `templates/`
- `workflows/`

Optional recommended directory not present:

- `learning/`

## Current Missing v0.5 Fields

- `asset_standard`
- `entry.readme`
- future `entry.asset_manifest` reference
- `asset_dirs`
- `discovery`
- `runtime_awareness`
- `capability_inventory_refs`
- `pal_skill_boundary`
- `agent_skill_refs_policy`
- `memory_policy`
- `external_project_write_policy`
- `no_keyword_routing_policy`
- `credentials_allowed`
- `palsmith_governance_boundary`
- `compatibility`
- `migration_notes`

## Existing Fields To Preserve

R113 must preserve existing identity and compatibility fields:

- `id`
- `name`
- `display_name`
- `directory_name`
- `role`
- `official`
- `system_pal`
- `no_runtime_code`
- `direct_call`
- `aliases`
- `version`
- `type`
- `description`
- `formal_skill_count`
- `formal_skills`
- `license`
- `core_capabilities`
- `collaboration`
- `resource_policy`
- `compatible_runtimes`

## Update Scope

R113 may update `schema` to the v0.5 schema id and add v0.5 metadata / policy / compatibility fields as a conservative overlay.

## No Deletion Policy

No existing PalSmith `pal.json` field is deleted in this round. No central roster file, other official Pal `pal.json`, official `asset-manifest.json`, or PalSmith asset directory is modified.
