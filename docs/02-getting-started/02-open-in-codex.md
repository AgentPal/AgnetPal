# Use With Codex

## Purpose

This document explains the basic Codex path for AgentPal v0.1.0-rc.1.

## Steps

1. Add the AgentPal directory as a Codex workspace or project.
2. Open the AgentPal Workspace.
3. Paste or run `prompts/codex/initialize-agentpal-workspace.md`.
4. Let Codex read the short initialization path.
5. Start with Mira.

Do not add each official Pal as a separate Codex project for normal use. Add the AgentPal Workspace once; Mira can route to currently registered Pals from contacts and registry.

## Expected Behavior

- Ordinary messages go to Mira.
- Specialist Pals do not listen by default.
- Direct specialist replies start with the resolved Pal name from contacts and registry.
- No Python, Node.js, Rust, or Go dependency is required for initialization.
- Simple Pal Mode is the only active v0.1.0-rc.1 task-handling path.

## Related

- [Quick start](00-quick-start.md)
- [Initialize AgentPal](04-initialize-agentpal.md)
- [Call your first Pal](05-call-your-first-pal.md)
