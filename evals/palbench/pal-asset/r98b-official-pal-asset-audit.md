# R98-B Official Pal Asset Audit

Date: 2026-06-28

Owner Pal: PalSmith

Scope: audit the 9 official Pal Packs under `official/pals/` against the requested v0.5 Pal Asset Standard direction. This is an audit and upgrade-planning artifact only. It does not upgrade or edit any official Pal.

## Summary

Result: `upgrade_plan_required`.

The 9 official Pal Packs are structurally valid for the current v0.4 baseline: all root entry files exist, every `pal.json` parses, central roster count is 9, and every roster `pack_path` resolves under `official/pals/`.

The main v0.5 readiness gaps are standardization gaps, not immediate blockers:

- R98-A Pal Asset Standard files are present in the current worktree and were read as the v0.5 audit reference. R98-B does not stage or commit those R98-A files.
- none of the 9 official Pals has `asset-manifest.json`.
- none of the 9 `pal.json` files declares v0.5-style `asset_standard` or `asset_dirs`.
- 8 official Pals have `memory/` directories but no directory-level `memory/index.md` or `memory/README.md`.
- PalSmith lacks `learning/` and `memory/` directories and lacks `runbooks/index.md` or `runbooks/README.md`.
- legacy `.agentpal/` wording exists in Mira project-workgroup assets and PalSmith import-staging examples; it should be reviewed against the v0.4 central project-record boundary before v0.5.

Public safety result: `pass_with_notes`.

- no credential-assignment-shaped leak was found by the focused search.
- no active `keyword_map`, `domain_map`, or `role_map` was found in `official/pals/`.
- `.agentpal/` text hits are documentation / workflow references, not created external project directories. Some are stale-boundary review candidates.
- `git diff -- official/pals` returned no diff during validation.

## Baseline Counts

| Check | Result |
| --- | --- |
| Official Pal directories | 9 |
| Central registered Pals | 9 |
| Central active Pals | 9 |
| Official `pal.json` files parsed | 9 |
| Official `pal.json` parse failures | 0 |
| Root entry files expected | 45 |
| Root entry files present | 45 |
| Root entry files missing | 0 |
| `asset-manifest.json` files present | 0 |
| `asset_standard` in `pal.json` | 0 / 9 |
| `asset_dirs` in `pal.json` | 0 / 9 |
| `collaboration` in `pal.json` | 9 / 9 |
| `standards/pal-asset/` present | true |

## Audit Criteria

Root entry files checked:

- `README.md`
- `PAL.md`
- `pal.json`
- `AGENTS.md`
- `SKILL.md`

Asset directories checked:

- `identity/`
- `core/`
- `knowledge/`
- `research/`
- `skills/`
- `workflows/`
- `runbooks/`
- `learning/`
- `memory/`
- `state/`
- `reports/`
- `evals/`
- `examples/`

Index or README checked for:

- `skills/`
- `workflows/`
- `runbooks/`
- `knowledge/`
- `memory/`
- `learning/`
- `evals/`

## Per-Pal Audit Table

| Pal | Root entry status | Asset dirs status | Index status | Manifest status | Misplaced risk | Public safety result | Upgrade priority |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Mira | complete | complete | complete | missing `asset-manifest.json` | stale project-boundary assets mention external `.agentpal/` project facts / memory and should be reconciled with central `agentpal_project_record` policy | pass_with_notes | high |
| Atlas | complete | complete | missing `memory/index.md` or `memory/README.md` | missing `asset-manifest.json` | imported Skill cards under knowledge and security-hardening Skills should be reviewed to keep Pal Skill vs Runtime Skill boundary explicit | pass | medium |
| Nova | complete | complete | missing `memory/index.md` or `memory/README.md` | missing `asset-manifest.json` | no clear misplaced asset found from structural audit; v0.5 should still classify product examples vs memory templates | pass | medium |
| Vega | complete | complete | missing `memory/index.md` or `memory/README.md` | missing `asset-manifest.json` | research examples and source inventories should remain research/evidence, not promoted to stable knowledge without review | pass | medium |
| Quinn | complete | complete | missing `memory/index.md` or `memory/README.md` | missing `asset-manifest.json` | no clear misplaced asset found from structural audit; v0.5 should classify evals vs reports carefully | pass | medium |
| Morgan | complete | complete | missing `memory/index.md` or `memory/README.md` | missing `asset-manifest.json` | document privacy knowledge and examples appear correctly placed; v0.5 should verify reports are not used as memory | pass | medium |
| Harper | complete | complete | missing `memory/index.md` or `memory/README.md` | missing `asset-manifest.json` | no clear misplaced asset found from structural audit; v0.5 should separate style examples from durable user memory | pass | medium |
| Rhea | complete | complete | missing `memory/index.md` or `memory/README.md` | missing `asset-manifest.json` | runtime-capability examples and runbooks appear correctly separated; v0.5 should keep state out of memory | pass | medium |
| PalSmith | complete | missing `learning/`, `memory/` | missing `runbooks/index.md` or `runbooks/README.md`; missing `memory/`; missing `learning/` | missing `asset-manifest.json` | import-staging examples mention `.agentpal/import-staging/`; review against v0.5 staging / public export policy | pass_with_notes | high |

## Root Entry Findings

All 9 official Pals have:

- `README.md`
- `PAL.md`
- `pal.json`
- `AGENTS.md`
- `SKILL.md`

Content signal checks:

- all `SKILL.md` files mention Pal / Pal Pack orientation.
- all `AGENTS.md` files mention read/load behavior for runtime asset access.
- all `PAL.md` files contain boundary language.
- all `pal.json` files contain `id`, `role`, and `collaboration`.

v0.5 root-entry upgrade need:

- add explicit `asset_standard` metadata to `pal.json` after the R98-A standard is integrated into the target branch.
- add explicit `asset_dirs` inventory to `pal.json` using the R98-A directory standard.
- clarify in every `SKILL.md` that Pal Skills are Pal job-level capabilities, not host Runtime Agent Skills, if not already explicit enough.

## Asset Directory Findings

Classification used in this audit:

- required for minimal Pal: root files, `core/`, `skills/`, `knowledge/`, `memory/` placeholder or explicit not-applicable note, `evals/` or explicit test-plan note.
- recommended for standard Pal: `identity/`, `research/`, `workflows/`, `runbooks/`, `learning/`, `examples/`, directory indexes.
- optional: `reports/`, `state/` public-safe placeholders when the Pal has current use for them.
- not applicable: directories that the future v0.5 standard explicitly exempts.

Observed:

- 8 official Pals have the full audited directory set.
- PalSmith has no `learning/` or `memory/` directory. This is not a current blocker, but it is inconsistent with the other official Pals and should be resolved or explicitly marked not-applicable in v0.5 metadata.

## Index / README Findings

Index coverage is mostly present, but `memory/` is the main repeated gap.

Missing index/README items:

- Atlas: `memory/index.md` or `memory/README.md`
- Nova: `memory/index.md` or `memory/README.md`
- Vega: `memory/index.md` or `memory/README.md`
- Quinn: `memory/index.md` or `memory/README.md`
- Morgan: `memory/index.md` or `memory/README.md`
- Harper: `memory/index.md` or `memory/README.md`
- Rhea: `memory/index.md` or `memory/README.md`
- PalSmith: `runbooks/index.md` or `runbooks/README.md`, plus missing `memory/` and `learning/`

Mira has complete index coverage for the audited index directories.

## Manifest Findings

No official Pal currently has:

- `asset-manifest.json`

Recommended future manifest fields:

- `schema`
- `pal_id`
- `display_name`
- `asset_standard_version`
- `generated_at`
- `generated_by`
- `asset_root`
- `root_entries`
- `asset_dirs`
- `indexes`
- `public_safety`
- `collaboration`
- `skill_boundary`
- `runtime_boundary`
- `known_gaps`
- `not_run_checks`
- `requires_human_review`

R98-B does not generate real manifests.

## Misplaced Asset Risk Notes

This audit only records possible risks; it does not move files.

| Risk Type | Evidence / Note | Recommended Review |
| --- | --- | --- |
| Agent Skill vs Pal Skill | Some skill directories contain implementation-shaped or imported Skill references, especially in Atlas. | R99/R100 should require Pal job-level Skill wording and mark imported Runtime Skill references as knowledge or runtime candidates. |
| Workflow vs runbook | PalSmith has `runbooks/` but lacks a runbook index. | R99 should add index/README or explicitly classify runbooks. |
| Report vs memory | Official Pals include memory placeholders and reports directories. | R99/R100 should ensure reports are not treated as long-term memory and private reports remain excluded from public packs. |
| Research vs knowledge | Vega has substantial research examples. | R100/R101 should preserve distinction between source evidence, research notes, and durable knowledge. |
| State vs memory | State directories exist as public placeholders. | R100 should keep `state/` as runtime-private or placeholder only, never long-term memory. |
| External `.agentpal/` boundary | Mira project-workgroup assets contain old external `.agentpal/` memory/project-facts wording; PalSmith examples mention `.agentpal/import-staging/`. | R99/R100 should reconcile wording with v0.4 central `agentpal_project_record` and v0.5 staging policy. |

## Public Safety Findings

Focused checks requested by R98-B:

| Check | Result | Notes |
| --- | --- | --- |
| Credential assignment search | pass | Focused regex found no assignment-shaped live credential/token/password/api_key/secret values. |
| Broad credential terms | pass_with_notes | Broad hits are boundary text such as "do not store credentials/tokens" and examples of forbidden content. |
| `.agentpal/` search | pass_with_notes | Hits are workflow/docs/staging references; no external project `.agentpal/` data directory was found under official Pals. Some wording needs v0.5 boundary review. |
| `keyword_map|domain_map|role_map` search | pass | No hits under `official/pals/`. |
| `git diff -- official/pals` | pass | No diff. |

## Recommended Upgrade Priority

High:

- Mira: reconcile old external `.agentpal/` project-memory wording with central project record boundary.
- PalSmith: decide whether `memory/` and `learning/` are required for PalSmith under v0.5, add index coverage, and clarify import staging path policy.
- all Pals: add v0.5 `asset_standard` / `asset_dirs` metadata after R98-A standard integration.

Medium:

- add or normalize `memory/README.md` / `memory/index.md` for the 8 Pals with memory directories but no top-level memory index.
- add `asset-manifest.json` in R101 after metadata format is approved.
- audit Skill wording for Pal job-level capabilities vs Runtime Agent Skills.

Low:

- improve examples / evals index consistency after high and medium issues are resolved.

## Non-Goals / Not Run

Not run:

- no official Pal upgrades
- no manifest generation
- no automatic scanner or validator
- no Runtime / Skill / plugin / MCP discovery
- no external project `.agentpal/` writes
- no central roster modification
- no remote Git operations
