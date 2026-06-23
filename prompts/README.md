# Prompts

`prompts/` contains copy-and-paste prompts for AgentPal setup, project binding, and maintenance.

These files are Markdown instructions, not programs. They do not install dependencies, run scripts, scan the disk, create UI, or activate Deep Conductor, Subagent Mode, or external Agent orchestration.

## Quick Start Prompts

| User path | Prompt | Use when |
| --- | --- | --- |
| Codex | `codex/initialize-agentpal-workspace.md` | You opened the AgentPal Workspace directly in Codex and want to initialize Mira. |
| Claude Code | `claude-code/install-agentpal-current-project.md` | You are already inside `<your-project>` in Claude Code and want project-first AgentPal binding. |
| Generic CLI Agent | `cli-agent/install-agentpal-current-project.md` | Your CLI agent can read directories, follow Markdown / JSON instructions, and maintain context. |

## Project Workgroup Prompts

- `join-external-project-workgroup.md`: AgentPal-led external project binding from an AgentPal Workspace session.
- `remove-agentpal-workgroup.md`: AgentPal-led external project binding removal.
- `claude-code/remove-agentpal-current-project.md`: Claude Code project-local removal.
- `cli-agent/remove-agentpal-current-project.md`: generic CLI project-local removal.

For Claude Code, prefer the project-first path:

```text
cd <your-project>
claude
```

Then paste `claude-code/install-agentpal-current-project.md`.

## Maintenance Prompts

- `refresh-pal-index.md`: refresh contacts / registry after Pal Pack changes.
- `add-pal-to-agentpal.md`: add newly copied valid Pal Pack directories.
- `initialize-agentpal.md`: legacy-compatible workspace initialization prompt.
- `rebuild-mira-main-pal.md`: repair Mira public files only when damaged.
- `test-ai-routing-judgement.md`: manual routing judgement regression prompt.

## Future / Deprecated-For-Current-Use

- `test-codex-subagent-mode.md` is future-design diagnostic material. Do not use it as normal AgentPal v0.1.0-rc.1 task handling.

## Public-Safe Rules

- Use placeholders such as `<your-project>` and `<path-to-AgentPal>`.
- Do not include local absolute paths, credentials, tokens, customer data, or private project facts in prompt examples.
- Do not ask users to commit `.claude/settings.local.json`; it is local machine configuration.
- Do not copy all Pal Packs into an external project.
- Do not import the whole AgentPal Workspace into a project instruction file.

