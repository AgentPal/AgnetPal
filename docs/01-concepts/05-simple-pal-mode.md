# Simple Pal Mode

Simple Pal Mode is the only active task-handling path in AgentPal v0.1.0-rc.1.

## How It Works

1. Mira receives ordinary messages.
2. Mira judges substantive tasks case-by-case.
3. If a registered Pal should own the work, Mira gives a short handoff and stops.
4. The owner Pal answers immediately in the same response.
5. The owner Pal uses its own identity, assets, Output Contract, and fallback rules.

## Direct Pal Calls

`/pal Name` and `@Name` select a registered Pal by display name or alias.

The call enters that Pal's working mode. It does not start an independent agent process.

## What Simple Pal Mode Does Not Do

- It does not spawn child workflows.
- It does not run a multi-agent runtime.
- It does not call external agent services.
- It does not make tools, plugins, models, or MCP servers into Pals.
- It does not show runtime-mode metadata in normal answers.

## Why This Mode Exists

Simple Pal Mode keeps v0.1.0-rc.1 usable as a plain Markdown/JSON workspace. It also keeps context loading small: Mira reads routing context, and the selected owner Pal reads only the relevant slice of its own assets.

## Related

- [Call your first Pal](../02-getting-started/05-call-your-first-pal.md)
- [Official Pals](../99-reference/official-pals.md)
- [Context Packet](../06-collaboration/03-context-packet.md)
