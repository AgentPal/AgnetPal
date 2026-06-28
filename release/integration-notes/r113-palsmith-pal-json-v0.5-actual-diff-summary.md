# R113 PalSmith pal.json v0.5 Actual Diff Summary

Date: 2026-06-28

## Updated File

`official/pals/PalSmith-pal-governor/pal.json`

## Changed Fields

| Field | Before | After |
| --- | --- | --- |
| `schema` | `agentpal.pal-pack.v0.1` | `agentpal.pal.v0.5` |
| `asset_standard` | missing | `agentpal-pal-asset-standard.v0.5` |
| `entry` | `skill`, `pal`, `agent` | preserved existing entries and added `readme`, `asset_manifest` reference |
| `asset_dirs` | missing | actual existing PalSmith asset directories |
| `collaboration.central_roster_required` | missing | `true` |
| `discovery` | missing | direct call, aliases, central roster source |
| `runtime_awareness` | missing | requires runtime evidence; Pal does not execute or auto-probe |
| `capability_inventory_refs` | missing | capability inventory path as judgement input only |
| `pal_skill_boundary` | missing | Pal Skills are role-level; Agent Skills are runtime-level references |
| `agent_skill_refs_policy` | missing | reference-only Agent Skill policy |
| `memory_policy` | missing | no private memory, task logs, or report bodies in public manifest metadata |
| `external_project_write_policy` | missing | false by default; thin binding required |
| `no_keyword_routing_policy` | missing | false defaults for deterministic routing classes |
| `credentials_allowed` | missing | `false` |
| `palsmith_governance_boundary` | missing | no-code governance boundary and no automatic roster / project / runtime-program behavior |
| `compatibility` | missing | legacy readable, manifest not required, directory fallback true, optional `learning/` gap |
| `migration_notes` | missing | real-update notes for R113 |

## Preserved Fields

The update preserves:

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
- existing collaboration booleans and allowed modes
- `resource_policy`
- `compatible_runtimes`

## Skipped Fields / Non-Actions

- No real `asset-manifest.json` generated.
- No central roster edit.
- No other official Pal `pal.json` edit.
- No Pal asset move, delete, rename, or directory creation.
- No connector, scanner, marketplace, hub, installer, daemon, or auto-execution program.
- No external project `.agentpal/` write.

## Before / After Summary

Before R113, PalSmith had a v0.1-era manifest with strong identity and capability fields but lacked v0.5 metadata, explicit false-default policies, and compatibility metadata.

After R113, PalSmith keeps the same identity, version, no-code role, formal skills, collaboration surface, resource policy, and compatible runtime list while adding v0.5 metadata and safety boundaries.

## No Behavior Change Statement

This is a metadata overlay only. It does not make PalSmith execute actions, route by keywords, scan local systems, write external projects, modify the central roster, or publish releases.

## Rollback Note

Rollback, if required, should restore only `official/pals/PalSmith-pal-governor/pal.json` from the parent commit of the R113 checkpoint. No generated manifest or central roster rollback is expected because neither is changed in this round.
