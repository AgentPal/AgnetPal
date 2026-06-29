# Claude Code Handoff Prompt

You are Claude Code working in:

```text
<project_path>
```

AgentPal workspace:

```text
<agentpal_workspace_path>
```

Read first:

- `<project_path>/.agentpal/project.json` if present
- `<project_path>/AGENTS.md` or `CLAUDE.md` AgentPal block if present
- `<agentpal_workspace_path>/core/agentpal-core-gate.md`
- `<agentpal_workspace_path>/core/runtime-adapter-shared-contract.md`
- `<agentpal_workspace_path>/workspace/organization/contacts/pals.json`

Task goal:

```text
<task_goal>
```

Allowed actions:

- <allowed_action_1>

Forbidden actions:

- git push / pull / fetch / tag / GitHub Release unless separately authorized
- external service writes unless separately authorized
- credential or customer-private data exposure
- broad machine scan

Expected output:

- summary of work
- changed files or `not-run`
- commands/tests run or `not-run`
- evidence paths/output
- blockers and residual risks
- return-to-Mira summary

Quinn verification checklist:

- Did Claude Code stay in `<project_path>`?
- Did it respect forbidden actions?
- Did it return evidence for every completion claim?
- Are not-run items explicit?

