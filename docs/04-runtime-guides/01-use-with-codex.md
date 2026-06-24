# Use With Codex

This is the current Codex path for AgentPal v0.1.0-rc.1.

## Quick Start

1. Open the AgentPal Workspace in Codex.
2. Copy the contents of `prompts/codex/initialize-agentpal-workspace.md`.
3. Initialize AgentPal in the current workspace.
4. Start with Mira for ordinary messages.
5. Use `/pal Name` when you want to call a specialist directly.

## What To Expect

- Mira is the default Main Pal / Leader / Conductor.
- Ordinary messages go to Mira first.
- Specialist Pals do not listen by default.
- `/pal Name` enters the selected Pal working mode inside the current runtime.
- The active path is `Simple Pal Mode only`.

## Important Boundary

- AgentPal is not a Codex replacement.
- AgentPal is not a Codex subagent system in `v0.1.0-rc.1`.
- Deep Conductor is future design only.
- Do not describe parallel child workflows as the current AgentPal runtime path.

## Good First Commands

- Ask Mira what AgentPal can do in the current release.
- Ask Mira to route a task if you are unsure which Pal should own it.
- Call a specialist directly with `/pal Atlas`, `/pal Quinn`, or `/pal Harper`.

## Related

- [Runtime Compatibility](00-runtime-compatibility.md)
- [Current Status](../00-overview/01-current-status.md)
