# AgentPal

AgentPal is a no-code AI team organization layer for agent runtimes.

It does not replace Codex, Claude Code, OpenCode, OpenHands, OpenClaw, Hermes, workbuddy, Gemini CLI, DeepSeek-TUI, or other execution environments. It gives those environments a readable Pal workspace: identities, responsibilities, knowledge, skills, workflows, memory boundaries, task packages, verification habits, and collaboration rules.

In one sentence:

> AgentPal adds a Pal team organization layer to existing agent runtimes.

## What AgentPal Is

AgentPal v0.5 is a Markdown / JSON / protocol workspace. It is designed for runtimes that can read local files and follow structured instructions.

AgentPal is:

- a no-code Pal organization layer
- a Pal Pack and AI team workspace
- a way to organize role-based AI working partners
- a thin-binding system for connecting an external user project to the central AgentPal Workspace
- a public-safe set of docs, templates, examples, standards, and evaluation records

AgentPal is not:

- an Agent runtime
- a multi-agent runtime
- an app runtime
- a desktop app or web app
- an installer, CLI, daemon, scanner, connector layer, or marketplace
- an external-system executor
- a replacement for the host runtime that actually reads files, edits files, runs commands, or publishes releases

## Pal / Skill / Agent

AgentPal keeps three layers separate:

```text
Skill  -> capability package
Pal    -> working partner that uses Skills and Agents
Agent  -> execution runtime
```

The core positioning is:

- A Skill is a capability package; a Pal is a working partner that knows how to use Skills.
- An Agent is the execution runtime; a Pal is a working partner that knows how to use Agents.
- Multi-Pal and multi-Agent teams share the same goal, but AgentPal uses a lighter organization layer to reduce complexity and cost.

A Skill usually helps an AI do one kind of work. A Pal owns a role: identity, responsibility, knowledge, workflows, memory rules, output contracts, collaboration boundaries, and verification habits. An Agent runtime performs the actual execution.

## Multi-Pal Vs Multi-Agent

Multi-agent systems often create several executing agents. That can be powerful, but it can also add configuration, context, cost, permission, and result-merging overhead.

AgentPal starts lighter:

- Pals organize work, context, responsibility, and verification.
- The host runtime performs execution when real file, command, tool, or publishing actions are needed.
- A Pal team can still prepare work for subagents or external agents when the current runtime proves that capability and the user authorizes it.

Not every AI role needs to become an independent running Agent. Many roles work better as stable Pals that shape tasks, choose context, and verify results.

## Verified Runtime Support

Current v0.5 public claims are intentionally conservative.

| Runtime / mode | Status | Public claim |
| --- | --- | --- |
| Codex | verified | Codex-first AgentPal workspace initialization and Pal collaboration evidence exists. |
| Codex child/background thread and subagent usage | limited / evidence-backed | Supported only where current Codex host evidence and user authorization exist. |
| Claude Code | limited | Minimal handoff evidence exists; full AgentPal host acceptance is not claimed. |
| Generic CLI agents | compatibility path | Prompt-based path exists, but broad host acceptance is not claimed. |
| DeepSeek / DeepSeek-TUI | experimental / version-help only | Do not treat as complete runtime support. |
| Plan Mode | unavailable in current UI evidence | Do not claim real UI-verified support. |
| Goal Mode | limited | Active-goal evidence exists with UI capture limitations. |
| OpenCode / Gemini | unavailable in current evidence | Do not claim current support. |
| External systems such as GitHub, Notion, Lark, Cloudflare | not generally validated | AgentPal can prepare task packages, but does not claim direct writeback integration. |

Host capability must come from visible evidence, a manual profile, or a runtime-reported profile. AgentPal does not automatically scan the user's system.

## Built-In Pals

The current official Pal roster has 10 Pals. The source of truth is [`workspace/organization/contacts/pals.json`](workspace/organization/contacts/pals.json).

| Pal | Role | Use for | Direct call |
| --- | --- | --- | --- |
| Mira | Main Pal / Leader / Conductor | first contact, routing, project context, handoff, summaries | `/pal Mira` |
| Atlas | Developer / Implementation Lead | engineering plans, code work packages, implementation review | `/pal Atlas` |
| Nova | Product / Strategy Lead | product framing, PRD shape, user flows, priorities, roadmap | `/pal Nova` |
| Faye | AI Delivery Pal | business scenarios, user flows, data/interface lists, risks, Delivery Packs, `FAYE_BUILD_REQUEST` | `/pal Faye` |
| Vega | Research / Intelligence Lead | research plans, source synthesis, evidence matrices, uncertainty | `/pal Vega` |
| Quinn | Quality / Verification Lead | acceptance criteria, regression checks, evidence review, release gates | `/pal Quinn` |
| Morgan | Document / File Workflow Lead | documentation structure, file workflows, Office/PDF task packages | `/pal Morgan` |
| Harper | Writing / Content Craft Lead | writing, copy, narrative, voice, editing, claim safety | `/pal Harper` |
| Rhea | System / Runtime Safety Lead | runtime boundaries, permissions, no-code safety, release safety | `/pal Rhea` |
| PalSmith | Pal Asset Governor | create, inspect, upgrade, and govern Pals and Pal teams | `/pal PalSmith` |

Mira is the default entry Pal. Specialist Pals do not listen by default. Mira can route to them, or you can call them directly with `/pal Name`.

## Install And Initialize With Codex

AgentPal currently installs as a local workspace, not as a package manager dependency.

1. Clone or download this repository.
2. Keep the AgentPal directory as its own local workspace.
3. Open the AgentPal directory as a Codex project.
4. Open [`prompts/codex/initialize-agentpal-workspace.md`](prompts/codex/initialize-agentpal-workspace.md).
5. Copy the whole prompt into the fresh Codex conversation.
6. Confirm that Mira welcomes you and lists the current 10 Pals.
7. Use ordinary messages with Mira, or call a specialist with `/pal Name`.

Quick start:

- [`START_HERE.md`](START_HERE.md)
- [`prompts/codex/README.md`](prompts/codex/README.md)
- [`docs/04-runtime-guides/01-use-with-codex.md`](docs/04-runtime-guides/01-use-with-codex.md)

## Bind AgentPal To An External Project

Daily work usually happens inside your own project, not inside the AgentPal Workspace.

AgentPal uses thin binding for external projects:

- the external project stays the active project
- the AgentPal Workspace remains the Pal source and organization layer
- `.agentpal/` stores small binding files only
- Pal Packs, docs, evals, release files, memory, reports, and internal AgentPal assets are not copied into the external project

For current project binding, use the prompt path for your host runtime:

- Claude Code: [`prompts/claude-code/install-agentpal-current-project.md`](prompts/claude-code/install-agentpal-current-project.md)
- Generic CLI Agent: [`prompts/generic-cli-agent/install-agentpal-current-project.md`](prompts/generic-cli-agent/install-agentpal-current-project.md)

Codex-first support is the verified release path. Other host paths must remain honest about their current evidence limits.

## Create Your Own Pal Team

AgentPal includes PalSmith and Faye for moving from "use built-in Pals" to "design my own AI team."

Use Faye when you need to turn a real business idea into a delivery-shaped package:

- business scenario
- user flow
- data list
- interface list
- risks and missing information
- acceptance handoff
- `FAYE_BUILD_REQUEST`

Use PalSmith when you need to design or improve the Pal team:

- new Pal or team blueprint
- Pal responsibilities and boundaries
- Pal Pack structure
- knowledge / skill / workflow / runbook classification
- health check and governance notes

Useful entry points:

- [`docs/PalSmith.md`](docs/PalSmith.md)
- [`docs/03-user-guides/palsmith-v0.5-pal-creation-and-upgrade.md`](docs/03-user-guides/palsmith-v0.5-pal-creation-and-upgrade.md)
- [`docs/07-authoring-pals/README.md`](docs/07-authoring-pals/README.md)
- [`docs/03-pal-pack-standard/README.md`](docs/03-pal-pack-standard/README.md)

## Project Structure

| Path | Purpose |
| --- | --- |
| `AGENTS.md` | runtime instructions for AgentPal mode |
| `PAL.md` | workspace identity |
| `SKILL.md` | Skill-aware entry for the AgentPal Workspace |
| `agentpal.json` | structured workspace metadata |
| `prompts/` | copyable runtime prompts |
| `official/pals/` | official Pal Packs |
| `workspace/organization/contacts/` | central Pal roster and contact cards |
| `workspace/projects/` | central records for bound external projects |
| `docs/` | user docs, concepts, runtime guides, authoring guides |
| `standards/` | no-code standards and protocols |
| `templates/` | public-safe templates |
| `examples/` | public-safe examples |
| `evals/` and `release/` | validation and release evidence archive |

## Documentation

Start here:

- [`docs/README.md`](docs/README.md)
- [`docs/00-overview/00-what-is-agentpal.md`](docs/00-overview/00-what-is-agentpal.md)
- [`docs/01-concepts/07-why-pal.md`](docs/01-concepts/07-why-pal.md)
- [`docs/04-runtime-guides/00-runtime-compatibility.md`](docs/04-runtime-guides/00-runtime-compatibility.md)
- [`RESOURCE_INDEX.md`](RESOURCE_INDEX.md)

Evidence and validation records are available, but they are not the main onboarding path.

## Current Limitations

- AgentPal does not execute tasks by itself.
- AgentPal does not include a scanner, daemon, connector system, marketplace, installer, or app runtime.
- AgentPal does not claim full non-Codex host acceptance in v0.5.
- AgentPal does not write to GitHub, Notion, Lark, Cloudflare, CRM, or customer systems unless the current host runtime performs an explicitly authorized action with evidence.
- Customer data and private project facts must not be copied into public examples, Pal Packs, or global knowledge.
- Deep Conductor is a no-code collaboration and mode-decision protocol. It is not an automatic background executor.

## License

MIT. See [`LICENSE`](LICENSE).
