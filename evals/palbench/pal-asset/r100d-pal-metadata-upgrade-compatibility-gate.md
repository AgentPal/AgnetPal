# R100-D Pal Metadata Upgrade Compatibility Gate

Date: 2026-06-28

## Purpose

This PalBench gate defines the compatibility checks that must pass before any future official Pal v0.5 metadata or `asset-manifest.json` upgrade.

R100-D does not modify `official/pals/**`, does not generate real manifests, and does not change the central roster. It creates the gate that later upgrade threads must run before and after small batches of official Pal metadata work.

## Scope

Use this gate for future official Pal metadata / asset-manifest upgrades that may touch:

- `official/pals/<Pal-Directory>/pal.json`
- optional `official/pals/<Pal-Directory>/asset-manifest.json`
- optional root README or index compatibility work, only when separately allowed

This gate protects the v0.4 behavior proven by R95:

- central roster remains stable
- official Pal loading still works
- external projects remain thin-bound
- no keyword routing is introduced
- no Pal assets are copied into external projects
- no connector, scanner, or auto execution behavior appears

## Preconditions

Before running this gate, read:

- `release/current/v0.4-local-completion-report.md`
- `evals/palbench/v0.4/r95-v0.4-real-usage-regression-results.md`
- `workspace/organization/contacts/pals.json`
- `standards/pal-asset/`
- `release/integration-notes/r98b-official-pal-upgrade-plan.md`
- `release/fresh-clone-checks/r98d-local-pal-asset-resolver-validation.md`

R100-A or other Pal asset standard outputs should be read when available. If no file explicitly named R100-A exists, use the current integrated `standards/pal-asset/` files as the available standard source and record the direct R100-A evidence as `missing`.

## Gate 1: Central Roster Unchanged

### Checks

| Check | Required Result |
| --- | --- |
| `workspace/organization/contacts/pals.json` parses | pass |
| registered Pal count | 9 |
| active Pal count | 9 |
| every `pack_path` exists | pass |
| `routing_policy` | `ai_judgement_only` |
| `keyword_routing_allowed` | `false` |
| route-map keys | no active keyword / domain / role route map |
| central roster diff | no unexpected change |

### Failure Conditions

Fail the gate if:

- registered or active Pal count changes without a separate approved registration task;
- any `pack_path` points to a missing directory;
- central roster adds a keyword, domain, role, or deterministic routing map;
- `workspace/organization/contacts/pals.json` changes during a metadata-only upgrade thread.

## Gate 2: Official Pal Loadability

### Checks

For each official Pal under `official/pals/`:

| Check | Required Result |
| --- | --- |
| Pal directory exists | pass |
| `pal.json` exists and parses | pass |
| `PAL.md` exists | pass |
| `AGENTS.md` exists | pass |
| `SKILL.md` exists | pass |
| `README.md` exists or prior accepted compatibility is documented | pass / warning |
| current loading-order fallback works without `asset-manifest.json` | pass |
| presence of `asset-manifest.json` is optional | pass |

### Compatibility Rule

The absence of `asset-manifest.json` must not break official Pal loading. Existing v0.4 official Pals must remain loadable through directory convention and root entry files.

If a future upgrade adds `asset-manifest.json`, the manifest may improve navigation, but it must not become the only path to load the Pal.

### Failure Conditions

Fail the Pal-specific upgrade if:

- that Pal's `pal.json` does not parse;
- a required root entry is missing after the upgrade;
- loading requires a manifest that is absent;
- manifest presence causes root entries or directory convention fallback to be ignored;
- an upgrade claims loadability without current file evidence.

Block only the affected Pal upgrade, not the whole workspace, when the failure is isolated to one Pal's new metadata.

## Gate 3: Asset-Manifest Compatibility

### Checks

| Situation | Required Behavior |
| --- | --- |
| manifest exists | use it as an asset index |
| manifest missing | fall back to directory convention |
| recommended directory missing | warning, not blocker |
| required root entry missing | block only affected Pal upgrade |
| manifest lists a missing optional asset | warning |
| manifest lists a missing required asset | block affected Pal upgrade until repaired |
| manifest mentions Agent Skill refs | treat as references, not copied Pal Skills |
| manifest references external project assets | fail unless explicitly approved public-safe example outside default binding |

### Required Manifest Boundaries

An `asset-manifest.json`, when introduced later, must not:

- execute checks;
- scan directories automatically;
- validate a Pal by itself;
- store credentials or private memory;
- copy Pal assets into external projects;
- create project-local `.agentpal/pals`;
- create project-local `.agentpal/skills`;
- modify central roster files;
- define keyword, domain, role, or deterministic routing maps.

## Gate 4: Thin Binding Preserved

### Checks

| Check | Required Result |
| --- | --- |
| project binding templates still exist | pass |
| JSON project binding templates parse | pass |
| external project receives Pal assets by default | no |
| external project receives manifest by default | no |
| external project creates `.agentpal/pals` by default | no |
| external project creates `.agentpal/skills` by default | no |
| central project record remains central | pass |

### Failure Conditions

Fail the gate if a metadata / manifest upgrade:

- changes `templates/project-binding/` without explicit scope;
- changes thin binding semantics;
- requires external projects to copy Pal Packs, manifests, skills, workflows, memory, evals, reports, or capability inventory;
- writes into an external project `.agentpal/` directory;
- treats an external project as the Pal asset source of truth.

## Gate 5: No Behavior Expansion

### Checks

The upgrade must not introduce:

- connector
- external business system API client
- scanner
- validator
- installer
- daemon
- database
- marketplace or hub program
- auto sync
- auto execution
- automatic Runtime / Skill / plugin / MCP / business system probing
- keyword routing
- domain routing
- hardcoded role map
- credential storage
- private token storage
- cookie storage
- password storage
- secret storage

### Failure Conditions

Fail the gate if any future metadata or manifest file claims active runtime behavior without current Runtime evidence, or if it stores private operational data.

## Gate 6: v0.4 Regression Unaffected

### Required Reference

The gate must reference the R95 v0.4 regression result:

- `evals/palbench/v0.4/r95-v0.4-real-usage-regression-results.md`

R95 baseline:

- 10 test groups executed
- 10 pass
- 0 fail
- 0 not-run
- 0 blocked
- result: `ready_for_v0.4_completion_report`

### Rerun Requirement

If official Pal metadata changes later, rerun selected R95 groups at minimum:

| R95 Group | Why rerun |
| --- | --- |
| Group 2: External project thin binding | ensures manifests do not thicken binding |
| Group 3: Central Pal roster | ensures roster count and policy remain stable |
| Group 4: No keyword routing | ensures metadata does not introduce route maps |
| Group 5: Official Pal integrity | ensures official Pals still load |
| Group 10: Public safety / internal leak | ensures no credentials or private data enter manifests |

If an upgrade changes docs or public navigation, also rerun Group 9.

## Required Evidence Record

Every future run of this gate should record:

- commit or working tree baseline before upgrade;
- files changed;
- central roster count and parse result;
- official Pal count;
- per-Pal root entry and `pal.json` parse result;
- manifest presence / absence handling;
- thin binding check result;
- exact route-map declaration check;
- connector / scanner / credential scan result;
- selected R95 rerun result or `not-run` with reason;
- decision: `pass`, `fail`, `blocked`, or `needs-more-evidence`.

## Decision Rules

| Evidence | Decision |
| --- | --- |
| all gates pass and selected R95 reruns pass | pass |
| only optional dirs missing, all fallback behavior works | pass with warnings |
| one Pal metadata breaks loadability | fail affected Pal upgrade |
| central roster or thin binding changes unexpectedly | fail |
| keyword routing, connector, scanner, credential, or external project asset copy appears | fail |
| required evidence cannot be collected | blocked or needs-more-evidence |

## Non-Goals

This gate does not:

- upgrade any official Pal;
- generate real `asset-manifest.json` files;
- edit `pal.json`;
- modify central contacts;
- modify project binding templates;
- run the full R95 suite by itself;
- publish, tag, push, or create a release.

## Expected Use

Future official Pal upgrade threads should:

1. run this gate before changes;
2. apply one Pal or small batch;
3. rerun this gate;
4. rerun selected R95 groups;
5. commit only after evidence passes;
6. avoid push, tag, release, or remote sync in ordinary development rounds.
