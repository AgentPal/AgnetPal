# R113 PalSmith pal.json v0.5 Field Update Plan

Date: 2026-06-28

## Decision

Plan status: `ready_to_apply`

This plan applies a conservative overlay to `official/pals/PalSmith-pal-governor/pal.json`. It is based on the R112 PalSmith dry-run proposal, v0.5 metadata standard, current PalSmith root files, and actual directory evidence.

## Field Plan

| Field | Current value summary | Proposed value summary | Source | Action | Reason | Risk | Human review required | Applied in this round |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `schema` | `agentpal.pal-pack.v0.1` | `agentpal.pal.v0.5` | v0.5 standard, R112 proposal | update | mark target metadata shape | low; intentional upgrade marker | yes | yes |
| `id` | `palsmith-pal-governor` | preserve | current `pal.json`, central roster | preserve | stable identity | low | no | yes |
| `name` | `PalSmith` | preserve | current `pal.json` | preserve | stable human-short name | low | no | yes |
| `display_name` | `PalSmith / Pal Asset Governor` | preserve | current `pal.json` | preserve | stable display identity | low | no | yes |
| `directory_name` | `PalSmith-pal-governor` | preserve | current `pal.json`, central roster | preserve | stable path identity | low | no | yes |
| `role` | `pal-asset-governor` | preserve | current `pal.json`, central roster | preserve | stable role | low | no | yes |
| `version` | `0.1.0` | preserve | current `pal.json` | preserve | avoid claiming Pal product version change | low | yes | yes |
| `type` | `pal-pack` | preserve | current `pal.json` | preserve | compatibility | low | no | yes |
| `official`, `system_pal`, `no_runtime_code` | present | preserve | current `pal.json` | preserve | identity and boundary | low | no | yes |
| `direct_call`, `aliases` | present | preserve | current `pal.json`, central roster | preserve | direct mention compatibility | low | no | yes |
| `description` | present | preserve | current `pal.json` | preserve | no capability rewrite in R113 | low | yes | yes |
| `formal_skill_count`, `formal_skills` | present | preserve | current `pal.json`, skills index | preserve | no Pal Skill inventory change | low | no | yes |
| `license` | `MIT` | preserve | current `pal.json` | preserve | no license change | low | no | yes |
| `asset_standard` | missing | `agentpal-pal-asset-standard.v0.5` | v0.5 standard | add | identify asset metadata target | low | no | yes |
| `entry` | root entries missing README and manifest reference | preserve existing entries; add `readme`, `asset_manifest` reference | actual root files, standard | update | complete root metadata without generating manifest | medium; manifest file remains absent by design | yes | yes |
| `asset_dirs` | missing | actual existing PalSmith directories only | directory listing | add | navigation metadata | low | yes | yes |
| `core_capabilities` | present | preserve | current `pal.json` | preserve | capability pruning out of scope | medium | yes | yes |
| `collaboration` | present | preserve and add `central_roster_required` | current `pal.json`, standard | update | align with central roster source of truth | low | no | yes |
| `discovery` | missing | direct call, aliases, central roster ref | central roster, R112 proposal | add | discovery hint, not route map | low | no | yes |
| `runtime_awareness` | missing | requires evidence; Pal does not execute or auto-probe | PAL.md, AGENTS.md, SKILL.md | add | no-code runtime boundary | low | no | yes |
| `capability_inventory_refs` | missing | central capability inventory as judgement input only | v0.5 standard | add | prevent scanner behavior | low | no | yes |
| `pal_skill_boundary` | missing | Pal Skills role-level, Agent Skills runtime-level references | skills index | add | preserve skill boundary | low | no | yes |
| `agent_skill_refs_policy` | missing | reference-only, no storage by default | skills index, standard | add | avoid copying runtime skills into Pal assets | low | no | yes |
| `memory_policy` | missing | no private memory or report bodies in manifest | memory README, standard | add | public safety | low | no | yes |
| `external_project_write_policy` | missing | false by default, thin binding required | PAL.md, R100-D | add | preserve external project boundary | low | no | yes |
| `no_keyword_routing_policy` | missing | false defaults for keyword / domain / role / route maps | central roster, standard | add | avoid deterministic routing | low | no | yes |
| `credentials_allowed` | missing | `false` | standard | add | public safety | low | no | yes |
| `palsmith_governance_boundary` | missing | no-code governance; no automatic roster modification or runtime programs | PAL.md, AGENTS.md, SKILL.md | add | PalSmith-specific safe boundary | medium; wording must not overpromise | yes | yes |
| `compatibility` | missing | legacy readable; manifest not required; directory fallback true; missing optional `learning/` | R100-D, manifest cases | add | legacy loadability | low | yes | yes |
| `migration_notes` | missing | real-update notes without dry-run-only wording | standard, R112 proposal | add | human-readable upgrade context | low | yes | yes |
| real asset manifest content | absent | keep absent | task boundary | skip | R113 forbids manifest generation | low | no | no |
| central roster edits | none | none | task boundary | skip | R113 forbids roster edits | low | no | no |
| other official Pal `pal.json` files | unchanged | unchanged | task boundary | skip | single-Pal pilot only | low | no | no |

## Explicit Non-Actions

- Do not create `official/pals/PalSmith-pal-governor/asset-manifest.json`.
- Do not modify Mira or any other official Pal `pal.json`.
- Do not modify central contacts.
- Do not add connector, scanner, marketplace, hub, installer, daemon, auto-execution, or external project write behavior.
- Do not add route maps or deterministic Pal assignment tables.
