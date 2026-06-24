# Generic CLI Agent One-Prompt AgentPal Project Install

Copy this prompt into a Markdown/JSON-capable CLI Agent while your shell is already inside the target project directory.

Before pasting, replace `AGENTPAL_HOME = <replace-with-your-AgentPal-path>` with your real AgentPal Workspace path, for example `AGENTPAL_HOME = D:/Tools/AgentPal` or `AGENTPAL_HOME = /Users/you/AgentPal`.

```text
Please connect AgentPal to the current project.

AGENTPAL_HOME = <replace-with-your-AgentPal-path>

This is a generic CLI Agent install path for runtimes such as CodeWhale, Gemini CLI, or another Markdown/JSON-capable Agent Runtime.

AgentPal is a Pal layer, not an Agent layer, not a multi-agent runtime, and not an execution layer.
Current mode: Simple Pal Mode only.

Do not call Subagent Mode.
Do not call external agents.
Do not create scripts, installers, CLIs, daemons, scanners, validators, or runtime dependencies.

Step 1 - Confirm current project root:
- Treat the current working directory as the target user project.
- If the current directory appears to be the AgentPal workspace itself, stop and tell me to cd into my target project first.
- AgentPal workspace indicators: agentpal.json, prompts/codex/initialize-agentpal-workspace.md, pals/Mira-main/, contacts/pals.json.

Step 2 - Resolve and verify AgentPal path:
Use AGENTPAL_HOME above if it is not a placeholder.
If missing, try only:
1. current project .agentpal/project.json -> agentpal_workspace_root
2. environment variable AGENTPAL_HOME
3. current project parent or sibling directory named AgentPal or agentpal
4. common examples only as examples, not a full disk scan

Verify the AgentPal path contains:
- README.md
- prompts/codex/initialize-agentpal-workspace.md
- agentpal.json
- RESOURCE_INDEX.md
- contacts/pals.json
- registry/pal.index.json
- pals/Mira-main/PAL.md

If verification fails, stop and ask me for the AgentPal path.

Step 3 - Create or update .agentpal/:
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
- runtime: generic-cli
- runtime_hint: generic-cli
- mode: simple-pal-mode-only
- agentpal_is_pal_layer: true
- created_by: agentpal-one-prompt-install
- version: v0.1.0-rc.1

Step 4 - Create or update AGENTS.md:
If AGENTS.md does not exist, create it.
If it exists, preserve user-authored content and replace only the block between:
<!-- BEGIN AGENTPAL WORKGROUP -->
<!-- END AGENTPAL WORKGROUP -->

Use this lightweight block:

<!-- BEGIN AGENTPAL WORKGROUP -->
This project is connected to AgentPal.

This block is managed by AgentPal.
When removing the AgentPal workgroup, delete only this block.
Do not delete user-authored AGENTS.md content outside this block.

Runtime hint: generic-cli

AgentPal is a Pal layer, not an Agent runtime, not a multi-agent runtime, and not an execution layer.
Current mode: Simple Pal Mode only.

Active project root: this current project directory.
AgentPal workspace root: <path-to-AgentPal>

Mira is the default Main Pal, Leader Pal, and Conductor. Ordinary messages should be treated as going to Mira first.
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
<!-- END AGENTPAL WORKGROUP -->

Step 5 - Optional runtime-specific notes:
Do not create CLAUDE.md unless Claude Code is detected or I explicitly ask.
Do not create GEMINI.md, CODEWHALE.md, or other runtime-specific files unless the project already uses that standard or I ask for it.

Step 6 - Verify:
Report briefly:
- current project root
- AgentPal workspace root
- .agentpal/ created or updated
- AGENTS.md block created or updated
- default Pal count from contacts / registry
- current mode: Simple Pal Mode only
- no Subagent Mode or external Agent orchestration activated
```
