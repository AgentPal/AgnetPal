# What Is AgentPal

AgentPal v0.5 is a lightweight Pal team organization layer for existing agent runtimes.

It packages Pal identity, responsibilities, knowledge, Skills, memory boundaries, workflows, context rules, output contracts, verification habits, and collaboration protocols into runtime-readable Markdown / JSON assets.

AgentPal is not an Agent runtime, multi-Agent runtime, execution layer, desktop app, connector, scanner, installer, daemon, marketplace, or app runtime.

## The Short Version

AgentPal gives an existing host runtime a structured Pal workspace.

The host runtime still performs execution: reading files, writing files, calling tools, running commands, publishing, deleting, or modifying systems. AgentPal provides the Pal layer that helps the runtime decide who should answer, which assets to read, what boundaries apply, and what evidence is required.

## Workspace, Not One Pal Pack

The AgentPal root is the AgentPal workspace. It contains central contacts, core gates, orchestration methodology, templates, prompts, examples, evals, release files, and public-safe placeholders.

Single Pal Packs live under `official/pals/<Pal-Directory>/`. Each Pal owns its identity, output contract, professional knowledge, Skills, runbooks, workflows, examples, evals, and learning rules.

## Current Runtime Path

Mira receives ordinary messages. When a substantive task belongs to a registered Pal, Mira gives a short owner judgement and hands off. The owner Pal answers immediately in the same response using its own assets and Output Contract.

Direct calls such as `/pal Faye` enter that Pal's working mode inside the current host runtime. They do not start an independent Agent process.

Deep Conductor is available as a no-code collaboration and mode-decision protocol. It is not automatic multi-Agent execution.

## Official Pal Roster

AgentPal v0.5 bundles 10 official Pals:

Mira, Atlas, Vega, Rhea, PalSmith, Quinn, Morgan, Harper, Nova, and Faye.

## Continue Reading

- [Current status](01-current-status.md)
- [Current capabilities](02-current-capabilities.md)
- [What is a Pal?](../01-concepts/01-what-is-a-pal.md)
- [Pal vs Agent vs Skill](../01-concepts/03-pal-vs-agent-vs-skill.md)
- [Runtime compatibility](../04-runtime-guides/00-runtime-compatibility.md)
