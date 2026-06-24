# Generic CLI Agent One-Prompt AgentPal Project Removal

Copy this prompt into a Markdown/JSON-capable CLI Agent while your shell is inside the target project directory.

```text
Please remove AgentPal from the current project.

This removes only the AgentPal project binding. It must not delete project source files, project docs, .git, package files, user-authored AGENTS.md content outside the AgentPal block, or the AgentPal workspace itself.

Before changing files, confirm the current project root and ask me to confirm removal.

After confirmation:
1. Delete this project's .agentpal/ directory.
2. Remove only the block between <!-- BEGIN AGENTPAL WORKGROUP --> and <!-- END AGENTPAL WORKGROUP --> from AGENTS.md.
3. Preserve all other AGENTS.md content.
4. Do not modify Claude Code .claude/settings.local.json unless I explicitly ask.
5. Do not delete AgentPal workspace files.

Report briefly:
- .agentpal/ removed or was absent
- AGENTS.md AgentPal block removed or was absent
- no project source files were deleted
- AgentPal workspace was not deleted

Note: an already-open CLI Agent session may still have old instructions in memory. The cleanest verification is to restart the session in this project.
```
