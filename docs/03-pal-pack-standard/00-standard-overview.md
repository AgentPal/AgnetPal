# Standard Overview

## Status

Current for AgentPal `v0.1.0-rc.1`.

AgentPal is a Pal Workspace and Pal Pack standard practice for agent runtimes. A Pal Pack is one directory that packages a Pal's identity, output contract, knowledge, Skills, runbooks, workflows, examples, evals, and public-safe placeholders.

## What This Standard Does

- Gives external users a concrete directory shape for creating a Pal.
- Keeps Pal Packs readable by Codex, Claude Code, and generic Markdown / JSON capable CLI agents.
- Separates Pal identity from ordinary Skills, plugins, models, MCP servers, runtimes, and raw repositories.
- Defines public/private boundaries for memory, state, reports, examples, and evals.

## Current v0.1 Boundary

`v0.1.0-rc.1` is file-driven. It does not provide an automatic scanner, validator, installer, desktop app, web app, marketplace, or active multi-agent runtime.

## Standard Levels

- Minimal: enough files for a runtime to load one Pal and produce valid Pal-mode answers.
- Standard: enough structure to maintain the Pal over time.
- Official: the richer pattern used by bundled Pals such as Mira, Atlas, and Nova.

## Next

Use [Pal Pack structure](01-pal-pack-structure.md), then follow the authoring guide in [docs/07-authoring-pals](../07-authoring-pals/00-authoring-overview.md).
