# Use With Codex

Codex is the verified first host for AgentPal v0.5.

Use this guide when you are opening the AgentPal workspace itself in Codex.

## Initialize

1. Open the AgentPal workspace directory in Codex.
2. Start a fresh thread.
3. Paste the full contents of [`prompts/codex/initialize-agentpal-workspace.md`](../../prompts/codex/initialize-agentpal-workspace.md).
4. Check that the first AgentPal answer starts with `Mira：`.
5. Confirm the official roster has 10 Pals and includes Faye.

## What To Expect

- Mira is the default Main Pal, Leader, and Conductor.
- Ordinary messages go to Mira first.
- `/pal Name` calls a registered Pal directly.
- Pal discovery comes from central contacts.
- Bounded context loading is expected.
- Deep Conductor can be used as a no-code collaboration and mode-decision protocol.

## What Not To Claim

Do not claim Codex performed an action unless the current Codex thread has evidence.

Do not claim:

- a background AgentPal service is running
- AgentPal scanned the runtime
- AgentPal installed a connector
- AgentPal started subagents automatically
- AgentPal copied all Pal Packs into a project

## External Project Use

For an external project, create a project-bound Codex thread or use the relevant project binding. The external project remains `active_project_root`; AgentPal remains `agentpal_workspace_root`.

The project-side `.agentpal/` directory should stay thin.

## Next Links

- [Open in Codex](../02-getting-started/02-open-in-codex.md)
- [Initialize AgentPal](../02-getting-started/04-initialize-agentpal.md)
- [Project-first connection](04-project-first-connection.md)
