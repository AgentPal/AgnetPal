# Pal Loading Order Standard

Date: 2026-06-28

## Purpose

This standard defines the logical loading order for a selected Pal Pack in AgentPal. It helps a Runtime, Brain, Mira, or owner Pal read enough Pal assets for the current task without loading every Pal file by default.

This is a no-code standard. It is not a resolver program, scanner, validator, daemon, installer, keyword router, or automatic execution engine.

## Scope

Use this standard after a Pal candidate has been selected or is being evaluated through AI judgement.

It applies to Pal assets stored in the AgentPal Workspace, especially under:

```text
official/pals/<Pal-Directory>/
```

It also applies to valid user-added Pal Packs stored in an approved central AgentPal location.

External projects do not provide local Pal bodies by default. A project-local `.agentpal/` folder provides thin binding and project context only. It must not be treated as the source of Pal identity, skills, workflows, memory, evals, or output contracts unless the user explicitly approved a separate public-safe example or private central record.

## Standard Loading Order

Read the smallest useful slice in this order:

1. `pal.json`
2. `PAL.md`
3. `AGENTS.md`
4. `SKILL.md`
5. `README.md`
6. `core/index.md` or the core protocols required by the task
7. `identity/`
8. `asset-manifest.json`
9. task-relevant assets under `knowledge/`, `skills/`, `workflows/`, `runbooks/`, `memory/`, and `evals/`

The order is a default logical order, not a requirement to read every file. Stop once the current task has enough identity, boundary, output-contract, and task-specific evidence.

## Required Interpretation

### `pal.json`

Read first when available. Use it to identify:

- Pal id
- display name
- role
- directory name
- aliases
- no-code or runtime boundary flags
- formal skill list when present

`pal.json` is not a routing map. Formal skills are capability claims and asset references, not automatic task triggers.

### `PAL.md`

Read for the Pal's identity, role, responsibilities, collaboration boundary, and what the Pal is not allowed to claim.

### `AGENTS.md`

Read for runtime-facing instructions, required entry files, context boundaries, allowed assets, and execution boundary.

### `SKILL.md`

Read for host-runtime skill entry metadata and the Pal's supported use cases. This file can help a Runtime understand when a Pal-owned method may be relevant, but it must not become keyword routing.

### `README.md`

Read as public orientation when available. It may summarize the Pal Pack shape, examples, or usage path. Missing `README.md` is a warning, not a blocker, unless a release, publish, or onboarding task requires it.

### `core/index.md` Or Required Core Protocols

If `core/index.md` exists, use it to select the smallest relevant protocol.

If no core index exists, read only the task-relevant core file named by `AGENTS.md`, `SKILL.md`, `PAL.md`, an asset manifest, or the current task package.

### `identity/`

Read identity files such as persona, voice, and boundaries when the task depends on voice, behavior, collaboration style, or publish readiness.

For pure path validation, identity files can remain index-known without content read.

### `asset-manifest.json`

If present, use it as an asset navigation aid. It can list Pal-owned skills, workflows, runbooks, knowledge, memory policy, evals, examples, source coverage, and verification assets.

The manifest is not a route table and must not include `keyword_map`, `domain_map`, or `role_map`.

### Task-Relevant Assets

After the entry and navigation files, read only the assets needed for the task:

- `knowledge/` for domain or method knowledge
- `skills/` for Pal-owned work methods
- `workflows/` for repeatable staged work
- `runbooks/` for operational review paths
- `memory/` for approved public-safe or project-approved memory summaries
- `evals/` for self-tests, acceptance, regression, or release checks

## Asset Manifest Fallback

If `asset-manifest.json` is missing, use directory convention fallback:

1. List the Pal root files.
2. List top-level asset directories.
3. Read index files such as `skills/index.md`, `knowledge/index.md`, `workflows/index.md`, or `runbooks/index.md` when present.
4. Select one to three relevant assets for ordinary tasks.
5. Expand only when the task requires deeper evidence.

Missing asset directories should produce a warning, not an automatic blocked result. Block only when the missing directory or asset is required for the task's acceptance criteria.

## Do Not Load By Default

Do not read by default:

- all official Pals
- all assets of one Pal
- all knowledge directories
- all memory
- all evals
- all examples
- all imported resources
- all private project records
- all Org Pack assets
- all Capability Inventory profiles

Directory listings, registry entries, indexes, and manifests expose paths for navigation. They are `index_known` evidence, not `content_read` evidence.

## Relationship To Central Roster

The current Pal source of truth is the central roster:

```text
workspace/organization/contacts/pals.json
workspace/organization/contacts/PAL_CONTACTS.md
official/pals/
```

The central roster identifies Pal candidates and Pack paths. It must not be modified by the loading process.

## Relationship To Org Packs

Org Packs may recommend Pals, workflows, governance patterns, or verification checklists. These recommendations are AI judgement inputs only.

An Org Pack recommendation can help decide which Pal asset slice to inspect, but it must not force a Pal selection or bypass the central roster.

## Relationship To Capability Inventory

Capability Inventory records may describe runtime, model, Skill, plugin, MCP, Pal, or business-system capabilities. They can inform risk, availability, evidence needs, and fallback selection.

Capability Inventory records must not become automatic Runtime selection, plugin selection, external system invocation, or deterministic Pal routing.

## Relationship To Thin Binding

External project binding files may provide:

- `active_project_root`
- `agentpal_workspace_root`
- `agentpal_project_record`
- runtime hint
- project context policy
- central contacts references

They do not provide:

- copied Pal Packs
- copied central roster
- copied Org Pack assets
- project-local Pal memory
- project-local Pal workflows
- project-local evals
- project-local Capability Inventory by default

## Required Report Fields

When reporting Pal asset loading, distinguish:

- `index_known_paths`
- `content_read_paths`
- `required_assets_read`
- `optional_assets_read`
- `missing_assets`
- `warnings`
- `not_run`
- `fallback_used`
- `verification_needed`

## Forbidden

The loading process must not:

- keyword route
- domain route
- use a hardcoded role map
- execute files
- call external APIs
- copy Pal assets into an external project
- modify central roster files
- store credentials
- load private memory without explicit approval
- turn missing evidence into pass
- claim host Runtime availability without current evidence

## Completion Bar

A Pal loading result is acceptable when it identifies the selected or candidate Pal, reads the minimum required identity and boundary files, selects only task-relevant assets, keeps missing assets visible, and preserves verification needs without pretending that loading equals execution.
