# Claude Code Project-First Check

## Scope

Verify the Claude Code path from README and `docs/04-runtime-guides/02-use-with-claude-code.md`.

## Input

```text
cd <your-project>
claude
```

Then paste:

```text
prompts/claude-code/install-agentpal-current-project.md
```

## Pass

- current directory is confirmed as the user project
- install stops if the current directory is the AgentPal Workspace itself
- AgentPal path is verified before writing binding files
- `.agentpal/` is created or updated
- `CLAUDE.md` and `AGENTS.md` preserve user-authored content outside the AgentPal block
- `.claude/settings.local.json` is local machine configuration and is not meant for commit
- `permissions.additionalDirectories` is merged without overwriting other settings
- restart or `/add-dir <path-to-AgentPal>` is described only as fallback
- final response includes a `Mira：` welcome

## Fail

- `claude --add-dir` is the default required path
- existing `CLAUDE.md` is overwritten
- all Pal Packs are copied into the project
- the whole AgentPal Workspace is imported into project instructions

