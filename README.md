# AgentPal

AgentPal is a Pal layer for coding agents.

It is not an Agent layer, not a multi-agent runtime, and not an execution layer. AgentPal gives an existing runtime a structured Pal workspace: identity, knowledge, skills, context, memory, output contracts, coordination rules, review habits, summaries, and learning storage.

AgentPal v0.1.0-rc.1 is a Markdown / JSON / protocol workspace. It has no desktop UI, web UI, daemon, scanner, installer, service, or required runtime dependency.

## Current Runtime

AgentPal v0.1.0-rc.1 uses Simple Pal Mode only.

In Simple Pal Mode:

- Mira is the default Main Pal, Leader Pal, and Conductor. Ordinary messages start with Mira.
- Mira judges substantive requests case-by-case.
- If a registered Pal can own the work, Mira gives a short handoff and stops.
- The owner Pal answers immediately in the same response.
- The owner Pal uses its own `PAL.md`, `SKILL.md`, `pal.json`, relevant assets, Output Contract, and honest fallback when assets are missing.
- AgentPal does not print runtime-mode metadata in normal answers.

AgentPal can be used from Codex, Claude Code, CodeWhale, Gemini CLI, DeepSeek-TUI, or another Markdown/JSON-capable agent runtime, because the Pal layer is plain files and protocols.

## Orchestration Methodology

AgentPal does not position itself against foundation models. It studies orchestration methodology: how a transparent Pal layer can help users apply existing Agent runtimes, models, reasoning levels, Skills, plugins, context, verification, and memory more effectively.

AgentPal does not compete with foundation models. It studies how to use existing Agent runtimes better.

Inspired by orchestration methods such as Fugu, AgentPal separates:

- Fast Route: use one suitable Pal / runtime / Skill for clear tasks.
- Deep Conductor: future orchestration for complex tasks using workflow topology, Context Access Lists, isolation, verification, and routing memory.

The v0.1 release provides the foundation: Mira as the default Main Pal / Leader Pal / Conductor, official Pal Packs, Simple Pal Mode, AI Judgement routing, Context Slicing, Task Packages, and one-prompt project install for Claude Code / generic CLI Agents. Future design work covers Capability Inventory, Context Access Lists, Routing Reward Memory, workflow topology, Deep Conductor, and PalBench evaluation.

See `docs/research/agentpal-orchestration-methodology.md`, `docs/research/fugu-inspired-agentpal-methodology.md`, and `docs/research/palbench-design.md`.

R33 adds a small-sample PalBench smoke validation in `docs/research/palbench-r33-small-sample-report.md`. It shows initial evidence for clearer task packages, stronger verification awareness, lower file-scope context risk, and lower user routing burden. It is not a statistically significant benchmark and does not compare foundation model capability.

## Single Entry Via Mira

Most users can start with Mira. They do not need to constantly decide whether a task should go to Atlas, Nova, Quinn, Codex, Claude Code, a Skill, a plugin, or a future Deep Conductor workflow.

Mira receives the goal, checks contacts / registry, judges ownership, prepares bounded context when needed, and hands off to the owner Pal. Explicit `/pal Name` calls still work.

## Context Slicing And Token Strategy

AgentPal's context advantage comes from loading the right slice, not from loading everything.

In normal task handling:

- Mira reads the user goal, task state, guardrails, and contacts / registry summary.
- Mira does not read every Pal's professional knowledge before routing.
- The owner Pal reads its own minimum required files and one to three relevant assets.
- Project files, memory, examples, evals, reports, imports, and future design docs are loaded only when the task needs them.
- `RESOURCE_INDEX.md` and Pal `index.md` files are navigation aids, not default context bundles.

AgentPal v0.1.0-rc.1 does not provide exact token metering, but it defines context budgets, file loading levels, and asset loading reports for auditability.

Initialization uses a short path by default. It reads only root guardrails, workspace metadata, contacts / registry JSON, Mira minimum assets, and the Runtime Response Gate. Deep initialization is reserved for diagnostics, release checks, registry repair, failed initialization, or explicit user request.

File names discovered through a directory listing, registry, or index are reported as `index_known_*`. They are not content reads. Files actually opened and read are reported as `content_read_*`.

Mira has her own secretary Output Contract at `pals/Mira-main/core/output-contract.md`. It allows reception, clarification, summaries, handoffs, Task Package compression, and Asset Loading Reports, but forbids Mira from writing specialist professional bodies owned by another Pal.

## What A Pal Is

A Pal is not an independent runtime process. A Pal is a task-facing package of:

- identity and role
- knowledge and skills
- context and memory boundaries
- output contract
- review and summary habits
- learning and Skill storage rules

The runtime still performs actual file reads, writes, commands, tool calls, publishing, and other execution actions. AgentPal helps the runtime decide who should answer, what assets to use, and how to report honestly.

## Bundled Pals

The bundled Pals are:

- Mira: Main Pal, Leader Pal, Conductor, and secretary-style coordinator
- Atlas: development perspective
- Vega: research and evidence perspective
- Rhea: local system and environment perspective
- Quinn: quality, risk, evidence, and acceptance perspective
- Morgan: document and file workflow perspective
- Harper: writing and communication perspective
- Nova: product and decision perspective

Capability notes are examples only. They are not a route map. Owner selection is AI judgement case-by-case from the current request, context, constraints, risk, requested output, and available Pal assets.

## Quick Start

1. Open this workspace in your agent runtime.
2. Run or paste `INIT_PROMPT.md`.
3. Talk to Mira normally.
4. Use `/pal Name` to call a Pal directly.
5. Put additional Pal Packs under `pals/` and refresh contacts / registry when needed.

## Using With Claude Code

For a real project, the recommended Claude Code workflow is project first:

```text
cd <your-project>
claude
```

Then paste `prompts/claude-code/install-agentpal-current-project.md` and provide your AgentPal path:

```text
Please connect AgentPal to the current project.
AGENTPAL_HOME = <path-to-AgentPal>
```

The one-prompt install creates or updates `.agentpal/`, `CLAUDE.md`, `AGENTS.md`, and `.claude/settings.local.json`. It merges `permissions.additionalDirectories` so Claude Code can access the AgentPal workspace path.

`.claude/settings.local.json` is local machine configuration and should not be committed. The install prompt adds it to `.gitignore` if needed.

You do not need to remember `claude --add-dir <path-to-AgentPal>` as the default path. If the current Claude Code session does not immediately pick up the new additional directory, restart Claude Code or temporarily use `/add-dir <path-to-AgentPal>`.

## Using With Generic CLI Agents

For CodeWhale, Gemini CLI, or another Markdown/JSON-capable Agent Runtime:

```text
cd <your-project>
<your-cli-agent>
```

Then paste `prompts/cli-agent/install-agentpal-current-project.md` and provide your AgentPal path. The generic prompt creates `.agentpal/` and updates `AGENTS.md`; it does not depend on Claude Code settings.

## External Project Workgroup

AgentPal can be added to an external project as a workgroup reference. In an external project-bound session:

- the external project is the active project
- AgentPal is only the Pal source and routing reference
- "this project" means the external project, not the AgentPal workspace

Use the Claude Code or generic CLI one-prompt install prompts for project-local setup. `prompts/join-external-project-workgroup.md` remains available for AgentPal-led project binding from inside an AgentPal workspace session.

## Skill Storage

If the user explicitly asks to save a method as a Skill, or similar operations happen more than 3 times, the owner Pal stores the formal Skill under its own directory:

```text
pals/<Owner-Pal-Directory>/skills/<skill-id>/SKILL.md
```

Do not store AgentPal Pal-owned Skills in global runtime skill folders unless the user explicitly asks for a global runtime Skill.

## Future Runtime Orchestration

Future designs for child workflows, non-Pal runtimes, MCP-hosted agents, or remote agent services are documented separately in `docs/99-reference/future-agent-orchestration.md`. They are not active in AgentPal v0.1.0-rc.1 runtime behavior.


