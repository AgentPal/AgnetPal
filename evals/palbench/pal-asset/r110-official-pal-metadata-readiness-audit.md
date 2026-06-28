# R110 Official Pal Metadata Readiness Audit

Date: 2026-06-28

## Purpose

Audit the 9 official Pals for future `pal.json` v0.5 metadata and `asset-manifest.json` readiness without modifying any official Pal `pal.json` and without generating any real official `asset-manifest.json`.

Decision vocabulary:

- `ready`: enough evidence for a future execution round with low residual review.
- `partial`: legacy Pal is loadable, but v0.5 metadata or manifest source evidence still needs mapping or review.
- `blocked`: required root entry, parseability, or safety evidence is missing.

## Summary

| Metric | Result |
| --- | --- |
| Official Pal dirs | 9 |
| Central roster registered / active | 9 / 9 |
| All official Pal `pal.json` parse | pass |
| Root entries complete | 9 / 9 |
| Current real `asset-manifest.json` files | 0 |
| Ready | 0 |
| Partial | 9 |
| Blocked | 0 |

All official Pals are legacy-loadable and suitable for future planned migration. None should be changed in R110.

## Per-Pal Readiness Table

| pal_id | pack_path | root_entries_complete | pal_json_parse | pal_json_current_schema | v0.5_required_field_status | v0.5_optional_field_status | collaboration_fields_status | asset_dirs_status | policy_fields_status | external_project_write_policy_status | keyword_routing_policy_status | credential_policy_status | readiness | safe_auto_fill_fields | human_review_fields | blockers | recommended_batch |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `mira-main` | `official/pals/Mira-main` | yes | pass | `agentpal.pal.v0.1` | missing `name`; can infer from `display_name` | missing v0.5 navigation and policy groups | present | partial: 13 dirs present | missing v0.5 policy groups | default false candidate | default false candidate | default false candidate | partial | `name`, `schema`, `entry`, `asset_dirs`, `discovery`, policy defaults | role wording, capability pruning, collaboration modes, not-applicable dirs, migration notes | none | R111 pilot candidate |
| `palsmith-pal-governor` | `official/pals/PalSmith-pal-governor` | yes | pass | `agentpal.pal-pack.v0.1` | complete from legacy fields | missing v0.5 navigation and policy groups | present | partial: 12 dirs present | missing v0.5 policy groups | default false candidate | default false candidate | default false candidate | partial | `schema`, `entry`, `asset_dirs`, `discovery`, policy defaults | role wording, capability pruning, collaboration modes, not-applicable dirs, migration notes | none | R111 pilot candidate |
| `atlas-developer` | `official/pals/Atlas-developer` | yes | pass | `agentpal.pal-pack.v0.1` | complete from legacy fields | missing most v0.5 policy groups | present | partial: 13 dirs present | missing v0.5 policy groups | default false candidate | default false candidate | default false candidate | partial | `schema`, `entry`, `asset_dirs`, `discovery`, policy defaults | role wording, capability pruning, collaboration modes, not-applicable dirs, migration notes | none | later small batch |
| `quinn-quality` | `official/pals/Quinn-quality` | yes | pass | `agentpal.pal-pack.v0.1` | complete from legacy fields | missing v0.5 navigation and policy groups | present | partial: 13 dirs present | missing v0.5 policy groups | default false candidate | default false candidate | default false candidate | partial | `schema`, `entry`, `asset_dirs`, `discovery`, policy defaults | role wording, capability pruning, collaboration modes, not-applicable dirs, migration notes | none | later small batch |
| `morgan-document` | `official/pals/Morgan-document` | yes | pass | `agentpal.pal-pack.v0.1` | complete from legacy fields | missing v0.5 navigation and policy groups | present | partial: 13 dirs present | missing v0.5 policy groups | default false candidate | default false candidate | default false candidate | partial | `schema`, `entry`, `asset_dirs`, `discovery`, policy defaults | role wording, capability pruning, collaboration modes, not-applicable dirs, migration notes | none | later small batch |
| `nova-product` | `official/pals/Nova-product` | yes | pass | `agentpal.pal-pack.v0.1` | complete from legacy fields | missing v0.5 navigation and policy groups | present | partial: 13 dirs present | missing v0.5 policy groups | default false candidate | default false candidate | default false candidate | partial | `schema`, `entry`, `asset_dirs`, `discovery`, policy defaults | role wording, capability pruning, collaboration modes, not-applicable dirs, migration notes | none | later small batch |
| `vega-research` | `official/pals/Vega-research` | yes | pass | `agentpal.pal-pack.v0.1` | complete from legacy fields | missing most v0.5 policy groups | present | partial: 13 dirs present | missing v0.5 policy groups | default false candidate | default false candidate | default false candidate | partial | `schema`, `entry`, `asset_dirs`, `discovery`, policy defaults | role wording, capability pruning, collaboration modes, not-applicable dirs, migration notes | none | later small batch |
| `harper-writing` | `official/pals/Harper-writing` | yes | pass | `agentpal.pal-pack.v0.1` | complete from legacy fields | missing v0.5 navigation and policy groups | present | partial: 13 dirs present | missing v0.5 policy groups | default false candidate | default false candidate | default false candidate | partial | `schema`, `entry`, `asset_dirs`, `discovery`, policy defaults | role wording, capability pruning, collaboration modes, not-applicable dirs, migration notes | none | later small batch |
| `rhea-system` | `official/pals/Rhea-system` | yes | pass | `agentpal.pal-pack.v0.1` | complete from legacy fields | missing most v0.5 policy groups | present | partial: 13 dirs present | missing v0.5 policy groups | default false candidate | default false candidate | default false candidate | partial | `schema`, `entry`, `asset_dirs`, `discovery`, policy defaults | role wording, capability pruning, collaboration modes, not-applicable dirs, migration notes | none | later small batch |

## Shared Findings

- All 9 official Pals remain legacy-loadable by `pal.json` plus root entries.
- No official Pal currently has a real `asset-manifest.json`.
- v0.5 policy fields are mostly absent and should be added only in a later execution round.
- `entry` and `asset_dirs` can be inferred from current root entries and existing directories, but not written in R110.
- `discovery` can be inferred from central roster aliases and direct-call fields, but central roster remains the source of truth.
- external project write policy, no-keyword-routing policy, credential policy, and Agent Skill refs policy can use safe defaults in a future migration, but must not be silently written in R110.

## R111 Pilot Recommendation

Recommended first metadata-only pilot candidates:

- `mira-main`
- `palsmith-pal-governor`

Reason: both have recent memory / research / skills index work and the clearest public-safe boundary notes. Mira needs one special review for `name` inference and Main Pal role wording. PalSmith needs review for governance-specific capability wording.

## R110 Boundary

This audit does not authorize or perform any `pal.json` rewrite or real `asset-manifest.json` generation.
