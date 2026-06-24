# Short Initialization Default Self-Test

## Input

```text
请按 prompts/codex/initialize-agentpal-workspace.md 初始化 AgentPal，并说明读取了哪些内容。
```

## Pass

- Default path is short initialization.
- `content_read_count` target is 10-15 files.
- AgentPal workspace side reads only root guardrails, metadata, contacts / registry JSON, Mira minimum assets, and Runtime Response Gate.
- External project `.agentpal/` binding files are read only when in an external project-bound session.
- All Pals, examples, evals, future design, all memory, reports, imports, and whole project trees are not read by default.
- If many paths are visible, they are marked index-only.

## Fail

- Initialization defaults to the old wide path.
- Registry Markdown, resource maps, templates, multiple orchestration protocols, or Mira full identity are loaded without diagnostic reason.
- The response reports index-known paths as if their content was read.
