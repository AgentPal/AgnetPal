# R110 pal.json v0.5 Field Mapping Table

Date: 2026-06-28

## Purpose

Map v0.5 `pal.json` fields to current evidence sources and classify whether future values can be inferred automatically, defaulted safely, or require human review.

This mapping is a readiness plan only. It does not modify any official Pal `pal.json`.

## Field Mapping

| v0.5 field | current source | can infer from existing `pal.json` | can infer from directory | can infer from central roster | requires human review | default allowed | forbidden default | notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `schema` | standard | partial | no | no | yes | `agentpal.pal.v0.5` in future batch | no silent write in R110 | Upgrade target must be explicit. |
| `id` | existing `pal.json` | yes | no | yes | no | no | no | Must match central roster. |
| `name` | `display_name`, roster display name | partial | no | yes | yes for display simplification | no | no | Mira currently lacks `name`; others have enough source but should be reviewed. |
| `display_name` | existing `pal.json`, roster | yes | no | yes | no | no | no | Preserve existing display text unless batch says otherwise. |
| `directory_name` | existing `pal.json`, directory | yes | yes | yes | no | no | no | Must match current pack path. |
| `role` | existing `pal.json`, roster role | yes | no | yes | yes | no | no | Human review should keep role concise and non-routing. |
| `type` | existing `pal.json` | yes | no | no | no | `pal-pack` if missing | no | Existing values are legacy-compatible. |
| `version` | existing `pal.json` | yes | no | no | yes | no | no | Future metadata version wording should be reviewed. |
| `asset_standard` | standard | no | no | no | no | `agentpal-pal-asset-standard.v0.5` | no | Safe once user approves migration batch. |
| `entry` | root entries | no | yes | no | no | root entry map from actual files | no | Include `PAL.md`, `README.md`, `AGENTS.md`, `SKILL.md`, `pal.json`, future manifest ref. |
| `asset_dirs` | existing directories | no | yes | no | yes for not-applicable dirs | actual existing dirs only | no invented dirs | Missing optional dirs must stay warnings. |
| `core_capabilities` | existing `pal.json` | yes | no | no | yes | no | no | Prune for public-safe non-route labels. |
| `collaboration` | existing `pal.json` | yes | no | yes | yes | no | no | Modes and approval fields need review. |
| `discovery` | aliases/direct_call, roster | yes | no | yes | no | central roster ref | no | Must state central roster is source of truth. |
| `runtime_awareness` | existing `pal.json`, standards | partial | no | no | yes | no-code defaults | no auto-probe | Must not claim Pal executes runtime actions. |
| `capability_inventory_refs` | standards / org records | no | no | possible | yes | empty or judgement-only refs | no scanner refs | References are judgement inputs only. |
| `pal_skill_boundary` | standards and skills indexes | no | yes | no | no | role-level true flags | no | Pal Skills are not Agent Skills. |
| `agent_skill_refs_policy` | standard | no | no | no | no | reference-only defaults | copying Agent Skills into Pal `skills/` | Must say refs require runtime evidence. |
| `memory_policy` | memory README / standard | no | yes | no | yes | safe privacy defaults | report bodies / private memory | Do not store task logs or full reports in `pal.json`. |
| `external_project_write_policy` | thin-binding docs / standard | no | no | no | no | `external_project_write_allowed_by_default: false`; `copy_pal_assets_to_external_project_by_default: false`; `thin_binding_required: true` | true by default | External projects remain thin-bound. |
| `no_keyword_routing_policy` | standard / roster | no | no | yes | no | all false | any true route-map default | `keyword_routing_allowed`, `domain_routing_allowed`, `role_routing_allowed`, `route_maps_allowed` default false. |
| `compatibility` | standards | no | no | no | yes | legacy-readable notes | no | Must preserve old Pal fallback. |
| `migration_notes` | audit findings | no | no | no | yes | concise public-safe notes | private report bodies | Should name gaps without copying internal reports. |
| `credentials_allowed` | standard | no | no | no | no | `false` | `true` | If top-level field is retained, it must remain false. |

## Auto-Fill Candidates For Future Batch

Safe candidates if a later execution round is approved:

- `entry` from actual root entry files.
- `asset_dirs` from existing directory names only.
- `discovery.direct_call` and aliases from current roster / existing `pal.json`.
- `asset_standard` from accepted standard.
- policy defaults that keep keyword routing, external project writes, credential storage, and Agent Skill copying disabled.

## Human Review Fields

Require review before writing:

- `name`
- `role`
- `version`
- `core_capabilities`
- `collaboration.allowed_modes`
- `runtime_awareness`
- `capability_inventory_refs`
- `compatibility`
- `migration_notes`
- not-applicable asset directory decisions

## Explicit Defaults

- `keyword_routing_allowed`: default false.
- `external_project_write_allowed_by_default`: default false.
- `credentials_allowed`: default false.
- `asset_standard`: can be set only if the current standard is accepted for the target batch.
- `asset_dirs`: infer only from real directories, not desired future directories.
- `collaboration`: review if missing or ambiguous.
- `agent_skill_refs_policy`: reference-only; Agent Skills are not copied into Pal `skills/`.
