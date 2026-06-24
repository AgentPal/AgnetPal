# Current Capabilities

This page describes what AgentPal v0.1.0-rc.1 can do today without treating future design material as active runtime behavior.

## Workspace Capabilities

- Provide an AgentPal Workspace with runtime-readable Markdown / JSON / protocol assets.
- Organize official and user-added Pal Packs under `pals/`.
- Expose Pal discovery through `contacts/` and `registry/`.
- Define runtime-facing release assets such as `AGENTS.md`, `PAL.md`, `SKILL.md`, `agentpal.json`, and the Codex initialization prompt at `prompts/codex/initialize-agentpal-workspace.md`.

## Pal Interaction Capabilities

- Start ordinary messages with Mira.
- Support `/pal Name` for explicit specialist calls.
- Support same-response owner handoff in `Simple Pal Mode`.
- Keep specialist Pals inactive until Mira routes or the user calls them directly.

## Context And Coordination Capabilities

- Fast Route for clear owner selection.
- Task Package for bounded task handoff.
- Context Slicing so runtimes load only relevant files.
- Asset Loading Budget so a Pal does not preload the whole workspace by default.
- Runtime Response Gate for answer validity and routing boundary.

## Runtime Use Capabilities

- Codex quick-start path from the AgentPal Workspace.
- Claude Code project-first binding path with `.agentpal/`, `CLAUDE.md`, `AGENTS.md`, and `.claude/settings.local.json`.
- Generic CLI agent compatibility path through `.agentpal/` and `AGENTS.md`.

## Validation And Release Capabilities

- Release notes, release checklist, and GitHub release draft files.
- Small-sample PalBench validation material for cautious RC evidence.
- Public-safe prompts, examples, and evaluation assets.

## Related

- [Current Status](01-current-status.md)
- [What AgentPal Is Not](04-what-agentpal-is-not.md)
- [Runtime Compatibility](../04-runtime-guides/00-runtime-compatibility.md)
