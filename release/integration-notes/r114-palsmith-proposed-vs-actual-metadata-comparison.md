# R114 PalSmith Proposed vs Actual Metadata Comparison

Date: 2026-06-28

## Purpose

Compare the R112 PalSmith v0.5 dry-run proposal with the R113 real PalSmith metadata update.

## Summary

Most R112 v0.5 metadata fields were adopted. R113 adjusted proposal-only or dry-run-only fields to preserve the existing real `pal.json` structure and avoid claiming a Pal product version change or generating a real asset manifest.

## Comparison

| Field | Proposed value summary | Actual value summary | Match / adjusted / skipped | Reason | Risk | Follow-up needed |
| --- | --- | --- | --- | --- | --- | --- |
| `schema` | `agentpal.pal.v0.5` | `agentpal.pal.v0.5` | match | intended metadata target | low | no |
| `id` | preserve `palsmith-pal-governor` | preserved | match | stable identity | low | no |
| `name` | preserve `PalSmith` | preserved | match | stable display identity | low | no |
| `display_name` | preserve | preserved | match | stable human label | low | no |
| `directory_name` | preserve | preserved | match | central roster path identity | low | no |
| `role` | preserve | preserved | match | Pal ownership boundary | low | no |
| `version` | dry-run value | real value preserved as `0.1.0` | adjusted | avoid implying a Pal product version release | low | no |
| `asset_standard` | add v0.5 asset standard | added | match | v0.5 metadata requirement | low | no |
| dry-run marker | proposal-only marker | not written | skipped | not appropriate for real metadata | low | no |
| `entry` | root entries plus future manifest reference | added while preserving existing entry order | adjusted | non-breaking overlay | low | no |
| `asset_dirs` | actual existing dirs only | actual existing dirs only | match | current directory evidence | low | no |
| `core_capabilities` | pruned public-safe labels | existing detailed labels preserved | adjusted | R113 avoided capability rewrite | medium | yes, future pruning review optional |
| `collaboration` | compact standard fields | existing fields preserved plus central roster flag | adjusted | conservative compatibility | low | no |
| `discovery` | direct call, aliases, central roster ref | added | match | central roster remains source of truth | low | no |
| `runtime_awareness` | evidence required; no Pal execution/probing | added | match | no-code boundary | low | no |
| `capability_inventory_refs` | judgement input only | added | match | avoids automatic discovery behavior | low | no |
| `pal_skill_boundary` | Pal Skills vs Agent Skill refs | added | match | preserves skill boundary | low | no |
| `agent_skill_refs_policy` | reference-only | added | match | avoids storing runtime skills as Pal Skills | low | no |
| `memory_policy` | no private memory or report bodies | added | match | public safety | low | no |
| `external_project_write_policy` | false by default | added | match | thin binding boundary | low | no |
| no fixed-route policy | all false | added | match | AI judgement only | low | no |
| private access material flag | false | added | match | public safety | low | no |
| PalSmith governance boundary | no-code governance only | added | match | Pal-specific boundary | low | no |
| `compatibility` | legacy readable; manifest not required; fallback true | added | match | backward compatibility | low | no |
| human-review array | explicit proposal review list | not written as a separate array | skipped | R113 uses field plan and migration notes instead | low | no |
| forbidden defaults array | proposal-only summary | not written as a separate array | skipped | represented by explicit false-default fields | low | no |
| `migration_notes` | dry-run notes | real-update notes | adjusted | remove dry-run-only wording | low | no |
| real asset manifest content | not proposed | not written | match | R114 still forbids real manifest generation | low | no |
| central roster edits | not proposed | not written | match | central roster unchanged | low | no |

## Adopted R112 Proposal Fields

Adopted:

- v0.5 schema
- `asset_standard`
- root `entry` completion
- actual `asset_dirs`
- discovery metadata
- runtime awareness metadata
- Pal Skill / Agent Skill boundary
- reference-only Agent Skill policy
- memory and external project write policies
- no fixed-route policy
- private access material false-default
- PalSmith governance boundary
- compatibility metadata

## Adjusted Fields

Adjusted:

- `version` preserved as `0.1.0`.
- `core_capabilities` preserved rather than pruned.
- `collaboration` preserved with an added central roster flag.
- `migration_notes` rewritten for real update context.

## Skipped Fields

Skipped:

- dry-run metadata marker
- separate human-review array
- separate forbidden-defaults array
- real asset manifest content
- central roster edits
- external project local Pal asset copies

## Follow-up

No blocking follow-up is required. A future PalSmith manifest dry-run can review whether capability labels should be summarized before any real manifest is generated.
