# Simple Pal Mode

Simple Pal Mode is the lightweight day-to-day task path in AgentPal v0.5.

Deep Conductor may help with no-code collaboration and mode decisions when work is complex, but Simple Pal Mode remains the normal path for ordinary and clear single-owner tasks.

## How It Works

1. Mira receives ordinary messages.
2. Mira judges substantive tasks case by case.
3. If a registered Pal should own the work, Mira gives a short handoff and stops.
4. The owner Pal answers immediately in the same response.
5. The owner Pal uses its identity, assets, Output Contract, and fallback rules.

## Direct Pal Calls

`/pal Name` and `@Name` select a registered Pal by display name or alias.

The call enters that Pal's working mode. It does not start an independent Agent process.

## What It Does Not Do

- It does not spawn child workflows by itself.
- It does not run a multi-Agent runtime.
- It does not call external Agent services.
- It does not make tools, plugins, models, or MCP servers into Pals.
- It does not show runtime-mode metadata in normal answers.

## Why This Mode Exists

Simple Pal Mode keeps AgentPal usable as a plain Markdown / JSON workspace. It also keeps context loading small: Mira reads routing context, and the selected owner Pal reads only the relevant slice of its own assets.

## Next Links

- [Call your first Pal](../02-getting-started/05-call-your-first-pal.md)
- [Official Pals](../99-reference/official-pals.md)
- [Pal Teams and Deep Conductor](08-pal-teams-collaboration-and-deep-conductor.md)
