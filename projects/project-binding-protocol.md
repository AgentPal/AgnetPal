# Project Binding Protocol

Use this protocol when the user asks to add AgentPal to a project.

For Claude Code, the preferred user workflow is:

```text
cd <your-project>
claude
```

Then paste `prompts/claude-code/install-agentpal-current-project.md` with the AgentPal path. The prompt writes `.claude/settings.local.json` so the user does not need to remember `claude --add-dir <path-to-AgentPal>` as the default entry.

For generic Markdown/JSON CLI Agents, use `prompts/generic-cli-agent/install-agentpal-current-project.md`.

## Core rule

Project means external user project by default, not the AgentPal workspace itself.

Codex project list first. list_projects first if the current environment provides it. If tool discovery is needed to expose list_projects, use tool discovery before saying the list is unavailable. Workspace roots first.

When the user asks Mira to add AgentPal to a named project, the first step must be checking the Codex current project list / `list_projects` / current visible workspace project list.

If the current environment provides a Codex `list_projects` tool, Mira must call or inspect it first. Do not skip it.

If no `list_projects` interface is available, Mira must say:

```text
Mira：我这里没有可用的 Codex 项目列表接口，所以我只能根据当前可见工作区和已登记项目查找。你也可以直接给我项目路径。
```

Only then inspect Codex-known projects, current-session visible projects, or workspace roots before asking the user for a path.

当用户说“把 AgentPal 工作组加入某某项目”时，Mira 必须先查 Codex 当前项目列表或工作区根目录。只有无法确定目标项目时，才向用户索要路径。

## Flow

1. Identify the requested external project.
2. Check Codex `list_projects` if the current environment provides it.
3. Use tool discovery if needed before saying `list_projects` is unavailable.
4. Inspect current Codex-known projects / current Codex project list / current-session visible projects / workspace roots.
5. Inspect AgentPal registered external project records.
6. Inspect recent project records.
7. Use a user-provided path if the user explicitly provided one.
8. If no target can be resolved, ask for the project path.
9. If one candidate is found, confirm the exact path with the user or proceed if the user already gave permission.
10. If multiple candidates are found, list candidates and ask the user to choose.
11. Use `projects/project-workgroup-template/agentpal/` as the template.
12. In the external project, create or update `.agentpal/`.
13. Write `project.json`, `AGENTPAL.md`, `PAL_GROUP.md`, and `INIT_AGENTPAL_PROJECT_PROMPT.md`.
14. Create or update the external project root `AGENTS.md` with a protected AgentPal workgroup block.
14a. For Claude Code, create or update `CLAUDE.md` with the same protected AgentPal workgroup block.
14b. For Claude Code, create or update `.claude/settings.local.json` and merge `permissions.additionalDirectories`.
15. Create context, memory, state, and index folders.
16. Ensure the root `AGENTS.md` block tells Codex to read `.agentpal/INIT_AGENTPAL_PROJECT_PROMPT.md` if this session has not loaded AgentPal rules yet.
17. Explain the next step prompt for entering the external project Codex session.
18. Explain that ordinary messages go to Mira and specialist Pals do not listen by default.

Do not bind AgentPal to the AgentPal workspace itself unless the user explicitly says they are developing AgentPal itself.

## Project root roles

Every external binding must distinguish the two roots:

- `active_project_root`: the external user project directory.
- `agentpal_workspace_root`: the AgentPal workspace directory, used only as a Pal source and routing reference.
- `active_project_role`: `user_project`.
- `agentpal_workspace_role`: `pal_workspace_reference`.
- `current_project_semantics`: `active_project_root_only`.
- `runtime_hint`: `claude-code`, `codex`, `generic-cli`, `codewhale`, `gemini-cli`, or `unknown`.
- `mode`: `simple-pal-mode-only`.

Current project means `active_project_root`. Do not list AgentPal workspace as project root. Do not treat the AgentPal workspace as part of this project. Only read or discuss AgentPal workspace files when the user explicitly asks about AgentPal itself, Mira files, Pal configuration, or the AgentPal workspace.

Exception: Pal discovery, direct Pal calls, owner routing, and selected Pal asset loading may read bounded contacts / registry and selected Pal files from `agentpal_workspace_root`. The external project's `.agentpal/` folder is not the Pal asset store.

Even if Codex exposes multiple workspace roots, AgentPal must choose one active context. Do not answer project questions by listing both the external project and the AgentPal workspace.

即使 Codex 暴露多个 workspace roots，AgentPal 也必须选择一个当前上下文。回答“项目”问题时不能把外部项目和 AgentPal 工作区同时列出来。

## External project root AGENTS.md / CLAUDE.md

project workgroup auto-load.

Creating `.agentpal/` alone is not enough because runtimes may not automatically read `.agentpal/AGENTPAL.md`.

When binding an external project, create or update the external project root `AGENTS.md`.

read root AGENTS.md.

If the file exists, append or replace only the protected block:

```text
<!-- BEGIN AGENTPAL WORKGROUP -->
...
<!-- END AGENTPAL WORKGROUP -->
```

If the file does not exist, create it with the protected block.

If the file does not exist, include a short project-native placeholder above the AgentPal block, then the protected block. Do not pretend to know project-specific rules.

For Claude Code, also create or update `CLAUDE.md` with the same marker pair. Preserve user-authored content and replace only the AgentPal block.

The block must say:

- This project is connected to AgentPal.
- The current external project directory is the active user project.
- The AgentPal workspace is only a Pal source and routing reference.
- Runtime hint is recorded in `.agentpal/project.json`.
- Current mode is Simple Pal Mode only.
- Do not treat the AgentPal workspace as part of this project.
- For routing and direct Pal calls, read contacts / registry from `agentpal_workspace_root`.
- Do not look only inside the external project's `.agentpal/` folder for Pal portraits or output templates.
- Ordinary messages in this project should be handled as if addressed to Mira.
- Mira is the default Main Pal, Leader Pal, and Conductor.
- Specialist Pals do not listen by default.
- Use `/pal Name` to call a specialist Pal.
- Read `.agentpal/project.json`.
- Read `.agentpal/AGENTPAL.md`.
- Read `.agentpal/PAL_GROUP.md`.
- AgentPal project-bound mode is active whenever the protected AgentPal block exists in the project root `AGENTS.md`.
- Before the first AgentPal-mode answer in a new session, read `.agentpal/INIT_AGENTPAL_PROJECT_PROMPT.md`.
- Every user-facing answer must start with a speaking Pal prefix such as `Mira：`, unless the user explicitly requests Codex generic / no Pal mode.
- If the user asks project questions, current project means `active_project_root`.
- Do not list AgentPal workspace as project root.
- Do not confuse this external project with the AgentPal workspace directory.
- Do not involve owner Pals unless Mira delegates after case-by-case AI routing judgement or the user directly calls them.
- Replies should include the speaking Pal prefix, such as `Mira：`.
- Owned tasks may be delegated through Context Packet after AI routing judgement.
- No hard-coded semantic routing.
- Pal capability reference is not a route map.
- Owner judgement gate: Mira may answer directly only for ordinary chat, clarification, routing explanation, project/context coordination, initialization guidance, result summarization, or explicit Mira-only / Codex-generic requests. Owned work goes to the selected owner Pal by AI judgement.
- This block is managed by AgentPal. When removing the workgroup, delete only this block and do not delete user-authored `AGENTS.md` content.
- Do not import or paste the whole AgentPal workspace, AgentPal `AGENTS.md`, or AgentPal `README.md`.
- Distinguish index-known paths from content-read files.

## Claude Code local settings

For Claude Code, create or update:

```text
.claude/settings.local.json
```

Rules:

- This file is local machine configuration and should not be committed.
- If it exists, parse JSON and preserve all existing settings.
- Merge only `permissions.additionalDirectories`.
- Append `agentpal_workspace_root` if missing.
- Preserve existing allow / deny / ask rules.
- Do not write local absolute AgentPal paths into `.claude/settings.json`.
- If JSON is invalid, stop and ask the user whether to fix or back it up. Do not overwrite.
- Ensure `.gitignore` contains `.claude/settings.local.json`.

`--add-dir` and `/add-dir` are fallback / advanced options for the current session, not the default install path.

## Post-bind user message

After successful binding, Mira says:

```text
Mira：
已经接好了。以后你在这个项目里说普通问题，会先到我这里；需要专业 Pal 的时候，我会逐案判断是否交给合适的人。

下一步你进入这个项目的 Codex 会话后，如果它没有自动进入 Mira 模式，就复制执行：

请读取当前项目根 AGENTS.md，以及 .agentpal/INIT_AGENTPAL_PROJECT_PROMPT.md，进入 AgentPal project-bound mode。普通消息默认交给 Mira，回答必须以当前 speaking Pal 前缀开头，例如 Mira：。当前项目只以本项目目录为准。

如果当前 Codex 能自动读取根 AGENTS.md，则用户无需手动执行这段提示。
```

## External project content boundary

The external project directory may act as shared project knowledge, but only by task need.

Do not share by default:

- credentials
- tokens
- secrets
- private user files
- private customer data
- unrelated source files
- full project trees

Do not copy all Pal Packs into the external project. AgentPal remains the Pal workspace; the external project receives `.agentpal/` binding files and an AgentPal block in the external project root `AGENTS.md`.

