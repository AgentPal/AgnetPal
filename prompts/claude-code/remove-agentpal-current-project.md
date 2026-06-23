# Claude Code One-Prompt AgentPal Project Removal

Copy this prompt into Claude Code while your shell is inside the target project directory.

```text
Please remove AgentPal from the current project.

This removes only the AgentPal project binding. It must not delete:
- project source files
- project docs
- .git
- package files
- user-authored CLAUDE.md content outside the AgentPal block
- user-authored AGENTS.md content outside the AgentPal block
- the AgentPal workspace itself
- any Pal Pack files

Before changing files, confirm the current project root and ask me to confirm removal.

After confirmation:
1. Delete this project's .agentpal/ directory.
2. Remove only the block between <!-- BEGIN AGENTPAL WORKGROUP --> and <!-- END AGENTPAL WORKGROUP --> from CLAUDE.md.
3. Remove only the block between <!-- BEGIN AGENTPAL WORKGROUP --> and <!-- END AGENTPAL WORKGROUP --> from AGENTS.md.
4. Read .claude/settings.local.json if it exists.
5. Remove the AgentPal path from permissions.additionalDirectories.
6. Preserve all other Claude Code settings, including allow / deny / ask rules.
7. If settings.local.json becomes empty or only contains empty permissions, ask whether to delete it. Do not delete it automatically.
8. Do not modify .claude/settings.json unless I explicitly ask.

If .claude/settings.local.json is invalid JSON, stop and ask me how to proceed. Do not overwrite it.

Report briefly:
- .agentpal/ removed or was absent
- CLAUDE.md AgentPal block removed or was absent
- AGENTS.md AgentPal block removed or was absent
- settings.local.json additionalDirectories updated or was absent
- no project source files were deleted
- AgentPal workspace was not deleted

Note: an already-open Claude Code session may still have old instructions in memory. The cleanest verification is to restart Claude Code in this project.
```
