# Claude Code One-Prompt Install Self-Test

## Input

```text
cd <your-project>
claude
```

Then paste `prompts/claude-code/install-agentpal-current-project.md` with `AGENTPAL_HOME = <path-to-AgentPal>`.

## Pass

- Current project root is confirmed and is not AgentPal itself.
- AgentPal path is verified before writes.
- `.agentpal/` is created or updated.
- `CLAUDE.md` block is created or updated.
- `AGENTS.md` block is created or updated.
- Both blocks tell a fresh session to read `.agentpal/project.json`, `.agentpal/AGENTPAL.md`, `.agentpal/PAL_GROUP.md`, and `.agentpal/INIT_AGENTPAL_PROJECT_PROMPT.md` if AgentPal project-bound rules are not loaded yet.
- `.claude/settings.local.json` is created or updated.
- `permissions.additionalDirectories` contains the AgentPal path.
- Existing project instructions and Claude settings are preserved.
- The prompt does not require manual `--add-dir` as the default path.
- Restart / `/add-dir` is presented only as fallback.
- Final install output includes a first welcome message that starts with `Mira：`.
- Welcome identifies Mira as AgentPal's default Main Pal / Leader Pal / Conductor.
- Welcome lists the 8 official bundled Pals.
- Welcome explains ordinary tasks start with Mira and `/pal Name` can explicitly call a specialist Pal.
- Welcome says v0.1 uses Simple Pal Mode only and Deep Conductor is future design, not automatic current execution.
- No all-AgentPal import, Subagent Mode, external Agent orchestration, or runtime dependency is introduced.

## Fail

- The user must start with `claude --add-dir` as the default required path.
- The prompt overwrites existing `CLAUDE.md` or `AGENTS.md`.
- The prompt copies all Pal Packs into the project.
- The prompt imports the whole AgentPal workspace into project context.
- The final response only lists installed files and does not include a `Mira：` welcome.
- Mira introduces herself primarily as a secretary instead of Main Pal / Leader Pal / Conductor.
