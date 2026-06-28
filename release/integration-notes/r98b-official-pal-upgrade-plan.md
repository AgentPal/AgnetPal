# R98-B Official Pal Upgrade Plan

Date: 2026-06-28

Scope: integration note for upgrading the 9 official Pal Packs toward a v0.5 Pal Asset Standard. This is a plan only. It does not edit `official/pals/**`, central contacts, shared entry files, or release metadata.

## Current Audit Inputs

- audit report: `evals/palbench/pal-asset/r98b-official-pal-asset-audit.md`
- gap table: `evals/palbench/pal-asset/r98b-official-pal-upgrade-gap-table.md`
- validation: `release/fresh-clone-checks/r98b-local-official-pal-asset-audit-validation.md`

## Preconditions

Before applying any official Pal asset changes:

1. Integrate or confirm the R98-A v0.5 Pal Asset Standard under `standards/pal-asset/`.
2. Decide the exact required / recommended / optional / not-applicable directory classes.
3. Decide the `pal.json` v0.5 fields, including `asset_standard`, `asset_dirs`, and manifest references.
4. Decide whether PalSmith requires `memory/` and `learning/` directories or explicit not-applicable metadata.
5. Reconcile old `.agentpal/` project-memory wording with the v0.4 central `agentpal_project_record` boundary.

## R99: Minimal Safe Index / README Additions

Goal: improve navigability without changing Pal behavior.

Allowed changes in a future R99 thread:

- add minimal public-safe `memory/README.md` or `memory/index.md` for:
  - Atlas
  - Nova
  - Vega
  - Quinn
  - Morgan
  - Harper
  - Rhea
- add `runbooks/README.md` or `runbooks/index.md` for PalSmith.
- if approved, add PalSmith `memory/` and `learning/` placeholders, or document them as not-applicable in a standard-compliant way.

Do not in R99:

- generate asset manifests
- change central roster
- change direct calls
- move files between asset directories
- modify external projects

Suggested validation:

- official Pal dirs still 9
- root entries still 45/45
- all `pal.json` parse
- no private memory / credentials / keyword routes
- `git diff official/pals` shows only approved index/README additions

## R100: `pal.json` v0.5 Metadata Update

Goal: make each official Pal self-describing under the v0.5 asset standard.

Recommended fields after standard approval:

- `asset_standard`
- `asset_standard_version`
- `asset_dirs`
- `root_entries`
- `index_policy`
- `manifest_policy`
- `skill_boundary`
- `runtime_boundary`
- `public_safety_policy`
- `not_applicable_asset_dirs`
- `known_asset_gaps`

Do not in R100:

- generate full manifests if the manifest schema is not approved
- infer missing content capability from directory existence
- add ordinary Skills, tools, models, plugins, MCP servers, raw repos, or knowledge packs to contacts

Suggested validation:

- all 9 `pal.json` parse
- central roster unchanged unless a separate user-approved registration task explicitly allows it
- `asset_dirs` entries match actual directories or explicit not-applicable notes

## R101: Asset Manifest Generation

Goal: generate `asset-manifest.json` for each official Pal after the schema is stable.

Recommended manifest sections:

- `schema`
- `pal_id`
- `display_name`
- `asset_standard_version`
- `generated_at`
- `asset_root`
- `root_entries`
- `asset_dirs`
- `indexes`
- `manifest_sources`
- `public_safety`
- `skill_boundary`
- `runtime_boundary`
- `known_gaps`
- `not_run_checks`
- `requires_human_review`

Manifest rules:

- manifests are evidence indexes, not validators.
- manifests do not prove job fitness by themselves.
- manifests must preserve `missing`, `not-run`, and `requires_human_review`.
- manifests must not include private memory, runtime state, private reports, credentials, or external project data.

## R102: PalSmith-Driven Audit Integration

Goal: integrate PalSmith audit methods into future official Pal maintenance without creating a runtime scanner.

Recommended work:

- add a PalSmith audit task-package template for official Pal asset review.
- document how to run a bounded, evidence-first official Pal audit.
- add PalBench cases for:
  - v0.5 root entry compliance
  - index completeness
  - manifest completeness
  - Pal Skill vs Runtime Skill boundary
  - stale `.agentpal/` boundary wording
  - public safety

Non-goals:

- no marketplace / hub program
- no scanner / validator / daemon
- no automatic Runtime / Skill / plugin / MCP / business-system probe
- no keyword router
- no central roster auto-modification

## Priority Queue

High:

- integrate / settle `standards/pal-asset/`
- reconcile stale `.agentpal/` boundary wording in Mira and PalSmith assets
- add v0.5 `pal.json` metadata after standard approval
- define and generate `asset-manifest.json` only after schema approval

Medium:

- add minimal memory index files for 7 specialist Pals with `memory/` directories
- add PalSmith runbooks index
- classify PalSmith `memory/` and `learning/` as required or not-applicable

Low:

- polish examples and eval index wording after the structural and schema work is done

## Boundary

This plan intentionally does not execute repairs. Any official Pal asset changes should happen in a later single-thread repair with explicit allowed paths and validation.
