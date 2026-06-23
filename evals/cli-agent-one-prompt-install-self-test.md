# Generic CLI Agent One-Prompt Install Self-Test

## Input

```text
cd <your-project>
<your-cli-agent>
```

Then paste `prompts/cli-agent/install-agentpal-current-project.md` with `AGENTPAL_HOME = <path-to-AgentPal>`.

## Pass

- Current project root is confirmed.
- AgentPal path is verified before writes.
- `.agentpal/` is created or updated.
- `AGENTS.md` AgentPal block is created or updated.
- The `AGENTS.md` block tells a fresh session to read `.agentpal/project.json`, `.agentpal/AGENTPAL.md`, `.agentpal/PAL_GROUP.md`, and `.agentpal/INIT_AGENTPAL_PROJECT_PROMPT.md` if AgentPal project-bound rules are not loaded yet.
- No Claude Code settings are required.
- `CLAUDE.md` is not created unless Claude Code is detected or user asks.
- Simple Pal Mode only remains active.
- No scripts, installer, external Agent orchestration, or Subagent Mode is introduced.

## Fail

- Generic prompt depends on `.claude/settings.local.json`.
- The prompt creates runtime-specific files without detection or user request.
- The prompt copies all Pal Packs into the project.
