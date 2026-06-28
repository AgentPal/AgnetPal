# R93-D Central Asset Integrity And Path Navigation Audit

## Audit Summary

Decision: pass with fix suggestions.

Method: Quinn evidence review + release quality gate. Codex execution layer ran read-only local checks, JSON parsing, path existence checks, and text searches. No shared entry files were modified.

Scope: central asset integrity after R68-R92 path migrations.

Hard boundary observed:

- No `git push`, `git pull`, `git fetch`, tag work, or GitHub Release work.
- No CLI, app, daemon, scanner, validator, installer, database, connector, or runtime dependency was added.
- `README.md`, `RESOURCE_INDEX.md`, `agentpal.json`, `AGENTS.md`, `PAL.md`, `SKILL.md`, and `workspace/organization/contacts/pals.json` were not modified.

Overall result:

- Core entry files: pass.
- Central roster: pass.
- Official Pals: pass.
- Capability Inventory four-source paths: pass.
- Business System governance chain: pass.
- Thin binding templates: pass.
- Forbidden active behavior: pass with tracked-file text hits classified as boundary/example/eval language; one ignored local `.agentpal/` runtime/smoke area is suspicious-local but not tracked.
- Path fix suggestions: required for stale path references in `RELEASE_MANIFEST.md` and `RELEASE_CHECKLIST.md`.

## Evidence Commands

Executed by current Codex execution layer:

- `git status --short --branch`
- parse all visible `.json` files with PowerShell `ConvertFrom-Json`
- path existence checks for required root files, directories, templates, examples, and governance-chain files
- official Pal directory count and required entry-file checks
- central roster count and routing flag checks
- `rg` searches for stale root paths, thick binding patterns, keyword routing maps, auto scanner/connector claims, and credential-like strings
- tracked runtime-code/manifest check through `git ls-files`

## Root Entry Path Status

| Path | Status |
| --- | --- |
| `README.md` | exists |
| `AGENTS.md` | exists |
| `PAL.md` | exists |
| `SKILL.md` | exists |
| `agentpal.json` | exists and parses |
| `RESOURCE_INDEX.md` | exists |

Key required directories referenced by the current root/navigation surfaces all exist:

| Path | Status |
| --- | --- |
| `official/pals/` | exists |
| `standards/capability-inventory/` | exists |
| `templates/capability-inventory/` | exists |
| `examples/capability-inventory/` | exists |
| `workspace/organization/capability-inventory/` | exists |
| `templates/project-binding/` | exists |
| `workspace/projects/_template/` | exists |

Stale path samples were found in release support files, not the protected shared entry files:

- `RELEASE_MANIFEST.md` still references old `pals/`, `contacts/`, and `registry/` root paths.
- `RELEASE_CHECKLIST.md` still references old `pals/*`, `contacts/pals.json`, and `registry/pal.index.json` paths.

These are recorded in `release/integration-notes/r93d-path-fix-suggestions.md` for the integration thread.

## Central Roster Status

Source: `workspace/organization/contacts/pals.json`

| Check | Result |
| --- | --- |
| JSON parse | pass |
| registered Pals | 9 |
| active Pals | 9 |
| `routing_policy` | `ai_judgement_only` |
| `keyword_routing_allowed` | `false` |
| top-level `keyword_map` / `domain_map` / `role_map` | absent |
| missing `pack_path` targets | 0 |

Registered active Pal pack paths all exist:

- `official/pals/Mira-main`
- `official/pals/Atlas-developer`
- `official/pals/Nova-product`
- `official/pals/Vega-research`
- `official/pals/Quinn-quality`
- `official/pals/Morgan-document`
- `official/pals/Harper-writing`
- `official/pals/Rhea-system`
- `official/pals/PalSmith-pal-governor`

## Official Pals Status Table

| Official Pal | `PAL.md` | `pal.json` parses | `AGENTS.md` | `SKILL.md` | copied `.agentpal/` dirs |
| --- | --- | --- | --- | --- | --- |
| `Atlas-developer` | pass | pass | pass | pass | 0 |
| `Harper-writing` | pass | pass | pass | pass | 0 |
| `Mira-main` | pass | pass | pass | pass | 0 |
| `Morgan-document` | pass | pass | pass | pass | 0 |
| `Nova-product` | pass | pass | pass | pass | 0 |
| `PalSmith-pal-governor` | pass | pass | pass | pass | 0 |
| `Quinn-quality` | pass | pass | pass | pass | 0 |
| `Rhea-system` | pass | pass | pass | pass | 0 |
| `Vega-research` | pass | pass | pass | pass | 0 |

Official Pal count: 9.

## Capability Inventory Status

Four-source integrity:

| Source | Status |
| --- | --- |
| standards: `standards/capability-inventory/` | pass |
| templates: `templates/capability-inventory/` | pass |
| examples: `examples/capability-inventory/` | pass |
| organization records: `workspace/organization/capability-inventory/` | pass |

README / navigation files:

| Path | Status |
| --- | --- |
| `standards/capability-inventory/README.md` | exists |
| `templates/capability-inventory/README.md` | exists |
| `examples/capability-inventory/README.md` | exists |
| `workspace/organization/capability-inventory/README.md` | exists |
| `workspace/projects/_template/capability-inventory/README.md` | exists |

## Business System Governance Chain Status

| Chain Item | Path | Status |
| --- | --- | --- |
| profile standard | `standards/capability-inventory/business-system-profile-standard.md` | pass |
| profile template | `templates/capability-inventory/business-system-profile-template.json` | pass |
| public examples | `examples/capability-inventory/business-system-profiles/` | pass |
| manual profile guide | `docs/03-user-guides/manual-capability-profile.md` | pass |
| review flow standard | `standards/capability-inventory/business-system-profile-review-flow.md` | pass |
| review packet template | `templates/capability-inventory/business-system-profile-review-packet.md` | pass |
| evidence pack standard | `standards/capability-inventory/business-system-profile-manual-update-evidence-pack.md` | pass |
| evidence pack template | `templates/capability-inventory/business-system-profile-manual-update-evidence-pack.md` | pass |
| evidence pack example | `examples/capability-inventory/business-system-profile-reviews/notion-read-access-manual-update-evidence.example.md` | pass |
| replay record standard | `standards/capability-inventory/business-system-profile-manual-writeback-replay-record.md` | pass |
| replay record template | `templates/capability-inventory/business-system-profile-manual-writeback-replay-record.md` | pass |
| replay record example | `examples/capability-inventory/business-system-profile-reviews/notion-read-access-manual-writeback-replay.example.md` | pass |
| audit trail standard | `standards/capability-inventory/business-system-profile-audit-trail-index.md` | pass |
| audit trail template | `templates/capability-inventory/business-system-profile-audit-trail-index.md` | pass |
| audit trail example | `examples/capability-inventory/business-system-profile-reviews/notion-read-access-audit-trail-index.example.md` | pass |
| governance decision standard | `standards/capability-inventory/business-system-profile-governance-decision-record.md` | pass |
| governance decision template | `templates/capability-inventory/business-system-profile-governance-decision-record.md` | pass |
| governance decision example | `examples/capability-inventory/business-system-profile-reviews/notion-read-access-governance-decision.example.md` | pass |
| change ledger standard | `standards/capability-inventory/business-system-profile-change-ledger.md` | pass |
| change ledger template | `templates/capability-inventory/business-system-profile-change-ledger.md` | pass |
| change ledger example | `examples/capability-inventory/business-system-profile-reviews/notion-read-access-change-ledger.example.md` | pass |

Governance chain count: 21 / 21 present.

## Thin Binding Status

| Check | Result |
| --- | --- |
| generic Codex binding templates | pass |
| Claude Code binding templates | pass |
| project JSON templates parse | pass |
| template file count under `templates/project-binding/` | 18 |
| forbidden default directories inside binding templates | none found |

Parsed project JSON files:

- `templates/project-binding/generic-codex/.agentpal/project.json`
- `templates/project-binding/claude-code/.agentpal/project.json`
- `workspace/projects/_template/project.json`

Local note: the AgentPal Workspace root contains an ignored `.agentpal/` local runtime/smoke area, including `.agentpal/reports`. `git ls-files -- '.agentpal/*'` returned no tracked files. This is not an external project binding template and not a public tracked asset, but it should remain ignored and should not be copied into external projects.

## JSON Parse Status

Visible `.json` files parsed: 82.

Failures: 0.

This includes tracked workspace JSON and visible ignored local JSON under the working tree.

## Forbidden Active Behavior Scan

| Search | Count / Result | Classification |
| --- | --- | --- |
| `.agentpal/(memory|state|reports|context|index|pals|workflows|evals|capability-inventory|business-systems|reviews|evidence|replay|rollback|verification|audit-trail|governance-decisions|change-ledger)` | 331 text hits | boundary docs, templates, archived examples, evals, and ignored local `.agentpal/` smoke/runtime data |
| `keyword_map|domain_map|role_map` | 92 text hits | forbidden-boundary language and release/eval evidence |
| exact JSON keys `"keyword_map"`, `"domain_map"`, `"role_map"` | 0 files | pass |
| `scanner|validator|daemon|auto scan|automatic scan|自动扫描|自动检测|自动发现|自动路由|connector|API client|background sync|auto sync` | 667 text hits | mostly negative boundary language, examples, evals, and release checklist wording |
| `credential|token|password|api_key|cookie|secret` | 951 text hits | mostly forbidden-boundary language and public-safe placeholders |
| concrete secret-like value regex | 1 hit | expected failure example: `examples/failures/business-system-profile-as-connector.md` uses `ghp_DO_NOT_USE_EXAMPLE_TOKEN` |
| tracked runtime code or dependency manifests | 0 | pass |

No tracked active scanner, validator, daemon, connector, dependency manifest, runtime code file, or keyword-route JSON configuration was found.

## Suspicious References

1. `RELEASE_MANIFEST.md` contains stale references to old root paths:
   - `pals/*`
   - `contacts/pals.json`
   - `contacts/PAL_CONTACTS.md`
   - `registry/pal.index.json`

2. `RELEASE_CHECKLIST.md` contains stale references to old root paths:
   - `pals/*`
   - `contacts/pals.json`
   - `registry/pal.index.json`

3. Ignored local `.agentpal/` runtime/smoke area exists under the AgentPal Workspace root. This is not tracked, but it contains names such as `reports`, `state`, `pals`, `scanners`, and smoke data. Classification: suspicious-local, not public tracked release content.

4. `examples/failures/business-system-profile-as-connector.md` contains `ghp_DO_NOT_USE_EXAMPLE_TOKEN`. Classification: public-safe negative example, not a real credential.

## Recommended Fixes

1. In the next single-thread integration pass, update `RELEASE_MANIFEST.md` stale root references to current paths:
   - `official/pals/*`
   - `workspace/organization/contacts/pals.json`
   - `workspace/organization/contacts/PAL_CONTACTS.md`
   - `workspace/resources/registry/pal.index.json` if that registry reference remains intended.

2. In the next single-thread integration pass, update `RELEASE_CHECKLIST.md` stale root references to current paths using the same mapping.

3. Keep local `.agentpal/` ignored. Do not copy it into public release files or external project bindings. Optional local cleanup can be handled separately, outside R93-D.

## Final Decision

R93-D audit result: pass with integration fix suggestions.

Blocking issues for central asset reachability: none found.

Blocking issues for roster integrity: none found.

Blocking issues for Capability Inventory / Business System governance-chain path reachability: none found.

Non-blocking navigation debt: stale release support references in `RELEASE_MANIFEST.md` and `RELEASE_CHECKLIST.md`.
