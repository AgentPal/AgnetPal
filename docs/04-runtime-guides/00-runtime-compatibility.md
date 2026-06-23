# Runtime Compatibility

AgentPal v0.1.0-rc.1 is a Pal layer, not an execution layer.

It is designed for runtimes that can read Markdown and JSON workspace files, respect project instructions, and report execution evidence.

## Primary Runtime Targets

- Codex.
- Claude Code.
- CodeWhale.
- Gemini CLI.

## Other Possible Runtimes

Other Markdown/JSON-capable runtimes may be able to use AgentPal files, but compatibility should be verified case by case.

## Boundary

Tools, models, plugins, MCP servers, and execution systems are not Pal contacts. They may provide evidence or perform actions only when the user request and safety boundary allow it.

Future runtime adapters are not active in v0.1.0-rc.1.

Claude Code can use `CLAUDE.md` and `.claude/settings.local.json` for project-local binding. Generic CLI Agents primarily use `AGENTS.md` and `.agentpal/`.

## Related

- [Use with Codex](../02-getting-started/02-open-in-codex.md)
- [Use with Claude Code](../02-getting-started/03-open-in-claude-code.md)
- [Future runtime adapters](99-future-runtime-adapters.md)
