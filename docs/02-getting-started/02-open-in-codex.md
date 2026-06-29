# Open In Codex

Codex is the verified first host for AgentPal v0.5.

Use this path when you want to initialize AgentPal itself, inspect the official Pal roster, or ask Mira to help with AgentPal workspace tasks.

## Steps

1. Open the AgentPal workspace directory as a Codex project.
2. Open [`prompts/codex/initialize-agentpal-workspace.md`](../../prompts/codex/initialize-agentpal-workspace.md).
3. Paste the whole initialization prompt into a fresh Codex thread.
4. Let Codex read the short initialization path.
5. Start ordinary messages with Mira.

## Expected First Result

The first AgentPal reply should:

- start with `Mira：`
- explain that AgentPal is a no-code Pal organization layer
- list the current official Pal roster from central contacts
- include 10 official Pals, including Faye
- avoid claiming a runtime scan, connector, installer, app runtime, or automatic multi-agent execution

## First Prompts To Try

```text
Mira, what can AgentPal v0.5 help me do today?
```

```text
/pal Quinn Review whether this plan has enough evidence to call it tested.
```

```text
/pal Faye Turn this business goal into a delivery package outline.
```

## External Projects

If you want to use AgentPal inside another project, do not treat the AgentPal workspace as that project. Use thin binding:

- [Bind an external project](../01-getting-started/bind-external-project.md)
- [Project-first connection](../04-runtime-guides/04-project-first-connection.md)

## Current Limits

- Codex real host evidence exists for v0.5.
- Host tools, models, plugins, and Skills must still be reported from visible current evidence.
- AgentPal does not create Codex subagents, background workers, or a runtime scanner.

## Next Links

- [Initialize AgentPal](04-initialize-agentpal.md)
- [Call your first Pal](05-call-your-first-pal.md)
- [Use with Codex runtime guide](../04-runtime-guides/01-use-with-codex.md)
