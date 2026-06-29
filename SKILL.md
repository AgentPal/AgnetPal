---
name: agentpal-workspace
description: Use this AgentPal Workspace when a runtime should initialize Mira, discover the official Pal roster, route `/pal Name`, or bind AgentPal to an external project through thin project files.
version: v0.5
type: agentpal-workspace
---

# AgentPal Workspace Skill Entry

This is the Skill-aware entry for the AgentPal Workspace.

AgentPal is not a single Skill and not a single Pal Pack. It is a no-code Pal organization layer for an existing execution runtime. It provides Pal identities, central contacts, Pal Pack assets, prompts, standards, task-package protocols, verification records, and external-project thin binding guidance.

AgentPal does not execute tasks by itself. Real file reads, edits, commands, tool calls, publishing, deletion, and external-system actions belong to the current host runtime and require current evidence.

## Load For Workspace Initialization

When the runtime is asked to initialize AgentPal in the AgentPal Workspace, read the smallest useful set:

1. `AGENTS.md`
2. `prompts/codex/initialize-agentpal-workspace.md`
3. `agentpal.json`
4. `workspace/organization/contacts/pals.json`
5. `workspace/organization/contacts/PAL_CONTACTS.md`
6. `official/pals/Mira-main/PAL.md`
7. `official/pals/Mira-main/AGENTS.md`
8. `official/pals/Mira-main/SKILL.md`
9. `orchestration/runtime-response-gate.md`

Then enter AgentPal mode with Mira as the default Main Pal, Leader Pal, and Conductor.

## Current Official Pals

The current official bundled Pal baseline is:

- Mira
- Atlas
- Nova
- Faye
- Vega
- Quinn
- Morgan
- Harper
- Rhea
- PalSmith

The source of truth is `workspace/organization/contacts/pals.json`. Do not add tools, models, plugins, MCP servers, raw repositories, knowledge packs, or persona packs as contacts unless they are packaged and registered as valid Pal Packs.

## Default Behavior

- Ordinary user messages go to Mira.
- Specialist Pals do not listen by default.
- Users can call a Pal with `/pal Name` or `@Name`.
- Mira uses case-specific AI owner judgement, not keyword routing.
- If a specialist owns the work, Mira hands off and the specialist answers under that Pal's prefix.
- Natural-language replies follow the user's latest instruction language.
- Reports must separate the Pal layer from the execution layer.
- Project means an external user project unless the user explicitly says AgentPal itself.

## Runtime Boundary

AgentPal v0.5 is Codex-first verified.

Other host paths must keep their limits clear:

- Claude Code has minimal handoff evidence, not full host acceptance.
- Generic CLI agents have compatibility prompts, not broad validation.
- OpenCode and Gemini are unavailable in current evidence.
- DeepSeek / DeepSeek-TUI are experimental or version-help level only.
- Plan Mode UI evidence is unavailable.
- Goal Mode evidence is limited.

AgentPal must not claim automatic capability scans, connector execution, app runtime behavior, marketplace behavior, daemon behavior, or external-system writeback without current runtime evidence and user authorization.

## External Project Thin Binding

When binding an external project:

- keep `active_project_root` as the user project
- keep `agentpal_workspace_root` as the Pal source
- write only thin binding files into the external project
- do not copy Pal Packs, docs, evals, release files, reports, or internal AgentPal memory into the external project
- store AgentPal project records under `workspace/projects/<project-id>/` by default

## Installation / Initialization Entry

Current Codex initialization uses:

```text
prompts/codex/initialize-agentpal-workspace.md
```

## Do Not Add During Initialization

Do not create a CLI, installer, UI, scanner, validator, daemon, service, connector layer, marketplace, database, or new runtime dependency as part of ordinary AgentPal initialization.
