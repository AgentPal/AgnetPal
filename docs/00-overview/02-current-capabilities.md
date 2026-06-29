# Current Capabilities

This page describes what AgentPal v0.5 can do today without treating host-runtime-dependent behavior as AgentPal execution.

## Workspace Capabilities

- Provide runtime-readable Markdown / JSON / protocol assets.
- Keep the AgentPal workspace separate from external user projects.
- Organize Pal Packs under approved Pal asset areas.
- Expose Pal discovery through `workspace/organization/contacts/`.
- Provide root initialization assets such as `AGENTS.md`, `PAL.md`, `SKILL.md`, `agentpal.json`, and `prompts/codex/initialize-agentpal-workspace.md`.

## Pal Interaction Capabilities

- Start ordinary messages with Mira.
- Support `/pal Name` and `@Name` for explicit Pal calls.
- Support same-response owner handoff.
- Keep specialist Pals inactive until Mira routes or the user calls them directly.
- Use the current 10-Pal official roster, including Faye.

## Context And Coordination Capabilities

- Fast Route for clear owner selection.
- Task Package for bounded task handoff.
- Context Slicing so runtimes load only relevant files.
- Asset Loading Budget so a Pal does not preload the whole workspace by default.
- Runtime Response Gate for answer validity and routing boundary.
- Deep Conductor as no-code collaboration and mode-decision protocol.
- Capability Inventory from visible evidence, manual profile, or runtime-reported profile.
- Verification Result Records and Routing Decision Records.

## Runtime Use Capabilities

- Codex-first initialization path from the AgentPal workspace.
- Claude Code project-first guidance with limited/minimal handoff evidence.
- Generic CLI Agent compatibility prompt path.
- Thin external project binding that avoids copying Pal Packs, docs, evals, release files, memory, reports, or internal assets into the external project.

## Validation And Release Capabilities

- Public docs, runtime guides, examples, and evaluation assets.
- PalBench documentation and release-readiness evidence under `evals/` and `release/`.
- Honest statuses such as `pass`, `partial`, `blocked`, `not-run`, `unknown`, and `unavailable`.

## Related

- [Current Status](01-current-status.md)
- [What AgentPal Is Not](04-what-agentpal-is-not.md)
- [Runtime Compatibility](../04-runtime-guides/00-runtime-compatibility.md)
