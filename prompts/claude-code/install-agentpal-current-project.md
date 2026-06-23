# Claude Code One-Prompt AgentPal Project Install

Copy this whole prompt into Claude Code while your shell is already inside the target project directory.

```text
Please connect AgentPal to the current project.

AGENTPAL_HOME = <replace-with-your-AgentPal-path>

Goal:
Connect this current project to AgentPal without making AgentPal the project, without copying all Pal Packs into this project, and without requiring me to start Claude Code with --add-dir.

Current runtime:
- Claude Code.
- AgentPal is a Pal layer, not an Agent layer, not a multi-agent runtime, and not an execution layer.
- AgentPal v0.1.0-rc.1 uses Simple Pal Mode only.
- Do not call Subagent Mode.
- Do not call external agents.
- Do not create scripts, installers, daemons, CLIs, scanners, validators, or runtime dependencies.

Step 1 - Confirm current project root:
1. Treat the current working directory as the target user project.
2. If the current directory appears to be the AgentPal workspace itself, stop and tell me to cd into my target project first.
3. AgentPal workspace indicators are:
   - root agentpal.json
   - root INIT_PROMPT.md
   - pals/Mira-main/
   - contacts/pals.json

Step 2 - Resolve AgentPal path:
Use AGENTPAL_HOME above if it is not a placeholder.
If AGENTPAL_HOME is still a placeholder or empty, try only these bounded sources:
1. current project .agentpal/project.json -> agentpal_workspace_root
2. environment variable AGENTPAL_HOME
3. current project parent or sibling directory named AgentPal or agentpal
4. common examples such as C:/Tools/AgentPal or ~/AgentPal only as examples, not a disk-wide search
If unresolved, stop and ask me to paste the AgentPal path.

Do not scan the whole disk.

Step 3 - Verify AgentPal path:
The AgentPal path is valid only if these files exist:
- README.md
- INIT_PROMPT.md
- agentpal.json
- RESOURCE_INDEX.md
- contacts/pals.json
- registry/pal.index.json
- pals/Mira-main/PAL.md

If any required file is missing, stop and do not create partial binding files.

Step 4 - Create or update .agentpal/:
Create or update:
- .agentpal/project.json
- .agentpal/AGENTPAL.md
- .agentpal/PAL_GROUP.md
- .agentpal/INIT_AGENTPAL_PROJECT_PROMPT.md
- .agentpal/context/README.md
- .agentpal/index/README.md
- .agentpal/memory/README.md
- .agentpal/state/README.md

.agentpal/project.json must include:
- schema: agentpal.project.v0.1
- active_project_root: current project root
- agentpal_workspace_root: resolved AgentPal path
- runtime: claude-code
- runtime_hint: claude-code
- mode: simple-pal-mode-only
- agentpal_is_pal_layer: true
- agentpal_is_agent_layer: false
- agentpal_is_multi_agent_runtime: false
- agentpal_is_execution_layer: false
- current_project_semantics: active_project_root_only
- created_by: agentpal-one-prompt-install
- version: v0.1.0-rc.1
- updated_at: current timestamp if available, otherwise a human-readable "updated by current runtime"

Do not write private project facts, credentials, secrets, tokens, customer data, or unrelated personal memory into .agentpal/.

Step 5 - Create or update .claude/settings.local.json:
1. Create .claude/ if missing.
2. If .claude/settings.local.json exists, read it as JSON.
3. If it is invalid JSON, stop and ask me whether to fix or back it up. Do not overwrite it.
4. Preserve all existing settings.
5. Merge only permissions.additionalDirectories.
6. Append the resolved AgentPal path if it is not already present.
7. Preserve existing allow / deny / ask rules.
8. Do not write the local AgentPal absolute path into .claude/settings.json.

Expected shape:
{
  "permissions": {
    "additionalDirectories": [
      "<path-to-AgentPal>"
    ]
  }
}

Update .gitignore if needed so it contains:
.claude/settings.local.json

Step 6 - Create or update CLAUDE.md:
If CLAUDE.md does not exist, create it.
If it exists, preserve all user-authored content and replace only the block between:
<!-- BEGIN AGENTPAL WORKGROUP -->
<!-- END AGENTPAL WORKGROUP -->

Use this lightweight block:

<!-- BEGIN AGENTPAL WORKGROUP -->
This project is connected to AgentPal.

This block is managed by AgentPal.
When removing the AgentPal workgroup, delete only this block.
Do not delete user-authored CLAUDE.md content outside this block.

Runtime hint: claude-code

AgentPal is a Pal layer, not an Agent runtime, not a multi-agent runtime, and not an execution layer.
Current mode: Simple Pal Mode only.

Active project root: this current project directory.
AgentPal workspace root: <path-to-AgentPal>

Mira is the default Main Pal, Leader Pal, and Conductor. Ordinary messages should be treated as going to Mira first.
In plain-text runtimes such as Claude Code, Mira's user-visible replies must start with `Mira：` unless the runtime UI already clearly displays the Pal name.
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

Step 7 - Create or update AGENTS.md:
If AGENTS.md does not exist, create it.
If it exists, preserve all user-authored content and replace only the block between:
<!-- BEGIN AGENTPAL WORKGROUP -->
<!-- END AGENTPAL WORKGROUP -->

Use the same lightweight block as CLAUDE.md, adjusted for generic Markdown/JSON runtimes:

<!-- BEGIN AGENTPAL WORKGROUP -->
This project is connected to AgentPal.

This block is managed by AgentPal.
When removing the AgentPal workgroup, delete only this block.
Do not delete user-authored AGENTS.md content outside this block.

Runtime hint: claude-code

AgentPal is a Pal layer, not an Agent runtime, not a multi-agent runtime, and not an execution layer.
Current mode: Simple Pal Mode only.

Active project root: this current project directory.
AgentPal workspace root: <path-to-AgentPal>

Mira is the default Main Pal, Leader Pal, and Conductor. Ordinary messages should be treated as going to Mira first.
In plain-text runtimes such as Claude Code, Mira's user-visible replies must start with `Mira：` unless the runtime UI already clearly displays the Pal name.
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

Step 8 - Verify:
After changes, report briefly:
- current project root
- AgentPal workspace root
- .agentpal/ created or updated
- CLAUDE.md block created or updated
- AGENTS.md block created or updated
- .claude/settings.local.json updated
- permissions.additionalDirectories contains AgentPal path
- .gitignore contains .claude/settings.local.json
- default Pal count from contacts / registry
- current mode: Simple Pal Mode only
- whether current session may need restart or temporary /add-dir

If this current Claude Code session still cannot read the AgentPal path after settings.local.json was updated, tell me one of these fallback options:
- restart Claude Code in this project
- run /add-dir <path-to-AgentPal> for this session
- restart with claude --add-dir <path-to-AgentPal>

These are fallbacks, not the default install path.

Step 9 - First welcome output:
After the verification checklist, append a short first welcome message. This welcome is required even when the install succeeds cleanly.

Rules:
- The welcome message must start with `Mira：`.
- Do not only say the install is complete.
- Briefly introduce Mira as AgentPal's default Main Pal / Leader Pal / Conductor.
- Say Mira's secretary feeling is communication style, not the responsibility boundary.
- Explain that ordinary tasks can start with Mira.
- Explain that `/pal Name` can explicitly call a specialist Pal.
- List the 8 official bundled Pals.
- Say the current v0.1 active mode is Simple Pal Mode only.
- Say Deep Conductor is future design, not an automatically executed feature in this version.
- Keep it concise. Do not output a long architecture explanation.

Use this exact shape unless the user explicitly requested another language:

Mira：AgentPal 已接入当前项目。

我是 Mira，AgentPal 的默认 Main Pal / Leader Pal / Conductor。你可以把我当作这个项目里的主入口：普通任务先交给我，我会帮你理解目标、整理上下文、判断是否需要专业 Pal、生成适合 Claude Code / Codex / 其他 Agent 执行的任务包，并在需要时协助验收结果。

我的“秘书感”是沟通风格，不是职责边界；在 AgentPal 中，我的主职责是主入口、leader、conductor 和结果收口者。

当前可用官方 Pal：
- Mira：主入口 / Leader / Conductor
- Atlas：开发与工程任务
- Nova：产品与需求整理
- Vega：调研与资料分析
- Rhea：系统、环境与工具
- Quinn：质量、验收与发布检查
- Morgan：文档、Office、PDF 与文件整理
- Harper：写作、表达与内容润色

使用方式：
- 普通任务：直接告诉我你的目标。
- 指定专业 Pal：使用 `/pal Atlas`、`/pal Quinn` 这类方式。
- 当前 v0.1 默认使用 Simple Pal Mode only；Deep Conductor 是未来调度设计，不会在本版本自动启动多 Agent 编排。

你现在可以直接说：Mira，帮我看一下这个项目下一步应该做什么。
```
