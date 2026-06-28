# R100-D Pal Manifest Backward Compatibility Cases

Date: 2026-06-28

## Purpose

These cases define expected backward compatibility behavior for future official Pal `asset-manifest.json` and v0.5 metadata upgrades.

They are no-code PalBench cases. They do not create or modify real official Pal manifests.

## Case Matrix

| Case | Scenario | Expected Result | Blocks |
| --- | --- | --- | --- |
| 1 | Old Pal without `asset-manifest.json` still loads by convention. | Runtime reads `pal.json`, `PAL.md`, `AGENTS.md`, `SKILL.md`, `README.md` if present, and task-relevant indexes/directories. | Block only if required root entries are missing or `pal.json` fails to parse. |
| 2 | New Pal with `asset-manifest.json` loads by manifest. | Runtime may use manifest as asset index while still preserving root-entry fallback. | Block if manifest conflicts with root entries or claims execution. |
| 3 | Manifest missing optional dir gives warning. | Missing recommended directory is reported as warning / `missing_optional`, not workspace failure. | Block only if the task requires that directory or manifest marks it required. |
| 4 | Missing required root entry blocks only that Pal upgrade, not whole workspace. | Affected Pal upgrade is `fail`; central roster and other Pals remain usable if unchanged. | Block affected Pal until repaired. |
| 5 | Agent Skill refs are references, not copied into Pal `skills/`. | Manifest or Pal Skill may list host Runtime Skill refs as candidates with availability evidence requirements. | Fail if runtime Agent Skill files are copied into Pal `skills/` as Pal-owned capabilities without rewriting and boundary. |
| 6 | External project does not receive manifest or Pal assets. | External project remains thin-bound; no default `.agentpal/pals`, `.agentpal/skills`, `.agentpal/workflows`, or copied manifest. | Fail if upgrade requires project-local Pal assets. |
| 7 | Central roster remains source of truth. | Pal discovery still reads `workspace/organization/contacts/pals.json`; manifests do not replace or modify central contacts. | Fail if manifest becomes roster, contact list, or route map. |

## Case 1: Old Pal Without Manifest

### Setup

An official Pal has:

- `pal.json`
- `PAL.md`
- `AGENTS.md`
- `SKILL.md`
- optional `README.md`
- no `asset-manifest.json`

### Expected Behavior

The Runtime / Brain uses the Pal loading order standard:

1. read root entries;
2. use indexes when present;
3. use directory convention fallback;
4. report `asset-manifest.json` as `not-present / compatible`;
5. continue normal Pal loading.

### Fail If

- loading stops only because `asset-manifest.json` is absent;
- absence of manifest becomes a workspace-level failure;
- directory convention fallback is removed.

## Case 2: New Pal With Manifest

### Setup

An upgraded Pal has a valid `asset-manifest.json` plus the standard root entries.

### Expected Behavior

The Runtime / Brain may use the manifest to navigate assets and then verify paths against the Pal directory.

The manifest is an index. It is not:

- proof of job fitness;
- runtime execution;
- scanner output;
- validator output;
- contact registry;
- route map.

### Fail If

- manifest replaces central roster;
- manifest claims execution occurred;
- manifest includes credentials or private memory;
- manifest makes root entry fallback impossible.

## Case 3: Missing Optional Directory

### Setup

The manifest or v0.5 metadata recommends a directory such as `runbooks/`, `learning/`, or `memory/`, but the directory is absent or explicitly not applicable.

### Expected Behavior

Report a warning:

```text
missing_optional: <dir>
impact: no blocker unless current task requires it
```

### Fail If

- optional missing directory blocks the whole workspace;
- warning is hidden;
- missing directory is reported as pass without explanation.

## Case 4: Missing Required Root Entry

### Setup

A future upgrade removes or breaks one of:

- `pal.json`
- `PAL.md`
- `AGENTS.md`
- `SKILL.md`

### Expected Behavior

The affected Pal upgrade fails. The gate reports:

- affected Pal id / directory;
- missing root entry;
- whether central roster still points to that Pal;
- repair required before committing the Pal upgrade.

### Fail If

- the whole workspace is declared unusable when only one upgraded Pal is broken;
- the broken Pal is accepted without evidence;
- central roster is edited to hide the failure.

## Case 5: Agent Skill Refs Are References

### Setup

An asset manifest or Pal Skill lists host Runtime capabilities such as browser control, document processing, GitHub CLI, spreadsheet handling, or MCP tools.

### Expected Behavior

These are `agent_skill_refs` or runtime capability candidates only.

They must include:

- availability status or `unknown`;
- current Runtime evidence requirement;
- fallback if unavailable;
- approval requirement if external systems or file writes are involved.

### Fail If

- Agent Skill refs are copied into Pal `skills/` as raw runtime tool files;
- Agent Skill refs become Pal contacts;
- Runtime Skill availability is claimed without current evidence;
- references trigger automatic probing, installation, connector setup, or execution.

## Case 6: External Project Does Not Receive Manifest Or Pal Assets

### Setup

An external project is bound to AgentPal through thin binding.

### Expected Behavior

The project-local binding remains limited to allowed binding files such as:

- `.agentpal/project.json`
- `.agentpal/AGENTPAL.md`
- root protected instruction blocks
- optional host-runtime local settings

Official Pal manifests and Pal assets stay in the AgentPal Workspace.

### Fail If

- upgrade writes or requires `.agentpal/pals`;
- upgrade writes or requires `.agentpal/skills`;
- upgrade writes or requires `.agentpal/workflows`;
- upgrade writes or requires `.agentpal/evals`;
- upgrade writes or requires copied `asset-manifest.json` files in the external project.

## Case 7: Central Roster Remains Source Of Truth

### Setup

Future manifests include Pal id, display name, asset paths, and capability summaries.

### Expected Behavior

The central roster remains the discovery source:

- `workspace/organization/contacts/pals.json`
- `workspace/organization/contacts/PAL_CONTACTS.md`
- `official/pals/`

Manifest metadata can describe one Pal's assets. It must not define organization-level contacts, routes, or roster membership.

### Fail If

- manifest replaces the central roster;
- manifest changes Pal availability;
- manifest introduces keyword, domain, role, or deterministic routes;
- manifest modifies `workspace/organization/contacts/pals.json`.

## Required Regression Link

These cases are tied to R95 v0.4 regression evidence:

- `evals/palbench/v0.4/r95-v0.4-real-usage-regression-results.md`

After any official Pal metadata / manifest change, rerun the relevant R95 groups listed in `r100d-pal-metadata-upgrade-compatibility-gate.md`.

## Expected Verdict

Expected verdict for R100-D itself: pass if these cases are defined without modifying official Pals and the local validation confirms central roster, official Pal loadability, thin binding, no keyword routing, and no behavior expansion remain intact.
