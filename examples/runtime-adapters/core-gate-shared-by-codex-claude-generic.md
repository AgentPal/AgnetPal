# Core Gate Shared By Codex, Claude Code, And Generic CLI

Codex, Claude Code, and generic CLI adapters should all point to the same AgentPal core gate files.

When `core/deliverable-aware-task-judgement-gate.md` changes, adapters inherit the updated rule by reading the AgentPal workspace root.

They should not each maintain a separate copy of:

- First Pal Gate
- Deliverable-aware Task Judgement
- Mira Conductor boundary
- Simple Pal Mode runtime boundary
- Pal source of truth rules

Runtime-specific differences should stay small:

- Codex: workspace initialization prompt.
- Claude Code: `CLAUDE.md` block and `.claude/settings.local.json`.
- Generic CLI: root `AGENTS.md` block only.
