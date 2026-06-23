# Use With Claude Code

## Purpose

This document is the runtime guide for Claude Code.

## Recommended Project-First Workflow

Use Claude Code from the target project:

```text
cd <your-project>
claude
```

Then paste `prompts/claude-code/install-agentpal-current-project.md`.

The one-prompt install writes lightweight project binding files and updates `.claude/settings.local.json` `permissions.additionalDirectories`. It does not copy all Pal Packs, does not import the whole AgentPal workspace, and does not activate Subagent Mode.

If the current session cannot access AgentPal immediately after the settings update, restart Claude Code or use temporary `/add-dir <path-to-AgentPal>`.

## Related

- [Quick start](../02-getting-started/00-quick-start.md)
- [Runtime compatibility](00-runtime-compatibility.md)
- [AgentPal vs agent runtime](../00-overview/03-agentpal-vs-agent-runtime.md)
- [Claude Code project install](../10-using-agentpal-with-claude-code.md)
