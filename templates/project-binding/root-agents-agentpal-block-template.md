# Root AGENTS.md / CLAUDE.md AgentPal Block Template

Use this protected block in an external project root `AGENTS.md`. The same lightweight shape may be used in `CLAUDE.md` for Claude Code.

Replace `<path-to-AgentPal>` with the user's AgentPal workspace path and `<runtime-hint>` with `claude-code`, `codex`, `generic-cli`, `codewhale`, `gemini-cli`, or `unknown`.

```text
<!-- BEGIN AGENTPAL WORKGROUP -->
This project is connected to AgentPal.

This block is managed by AgentPal.
When removing the AgentPal workgroup, delete only this block.
Do not delete user-authored AGENTS.md or CLAUDE.md content outside this block.

Runtime hint: <runtime-hint>

AgentPal is a Pal layer, not an Agent runtime, not a multi-agent runtime, and not an execution layer.
Current mode: Simple Pal Mode only.

Active project root: this current project directory.
AgentPal workspace root: <path-to-AgentPal>

Mira is the default Main Pal. Ordinary messages should be treated as going to Mira first.
Use /pal Name for explicit Pal calls.
Pal discovery source: AgentPal contacts / registry under agentpal_workspace_root.

Use RESOURCE_INDEX.md and selected Pal assets on demand.
Do not preload all Pals.
Do not import or paste AgentPal AGENTS.md, README.md, or the whole AgentPal workspace into this project context.
Do not call Subagent Mode in AgentPal v0.1.
Do not call external agents from AgentPal v0.1.

When reporting asset use, distinguish index-known paths from content-read files.
Project questions mean this active project root, not the AgentPal workspace.

For owner Pal selection, use case-by-case AI judgement from current contacts / registry. Do not use hard-coded semantic routing, keyword triggers, or fixed Pal sets.

If this session has not loaded AgentPal project-bound rules, read:
1. .agentpal/project.json
2. .agentpal/AGENTPAL.md
3. .agentpal/PAL_GROUP.md
4. .agentpal/INIT_AGENTPAL_PROJECT_PROMPT.md

Claude Code note:
- .claude/settings.local.json may contain permissions.additionalDirectories with the AgentPal workspace path.
- settings.local.json is local machine configuration and should not be committed.
- If the current Claude Code session cannot read the AgentPal path yet, restart Claude Code or temporarily use /add-dir <path-to-AgentPal>.
<!-- END AGENTPAL WORKGROUP -->
```

Use this block as a lightweight binding only. Do not copy AgentPal Pal Packs into the external project.
