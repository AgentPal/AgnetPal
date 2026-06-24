# Root AGENTS.md / CLAUDE.md AgentPal Block Template

Use this protected block in an external project root `AGENTS.md`. The same thin block may be used in `CLAUDE.md` for Claude Code.

Replace `<runtime-hint>` with `codex`, `claude-code`, `generic-cli`, `codewhale`, `gemini-cli`, or `unknown`.

```text
<!-- BEGIN AGENTPAL WORKGROUP -->
This project is connected to AgentPal.

This block is managed by AgentPal.
When removing the AgentPal workgroup, delete only this block.
Do not delete user-authored AGENTS.md or CLAUDE.md content outside this block.

Runtime hint: <runtime-hint>

AgentPal workspace root is recorded in `.agentpal/project.json`.
AgentPal rules, Pals, contacts, registry, protocols, examples, evals, and release docs are not copied into this project.

Before responding as AgentPal, read the current core gates from the AgentPal workspace:

1. `core/agentpal-core-gate.md`
2. `core/first-pal-gate.md`
3. `core/simple-pal-mode-runtime-contract.md`
4. `core/deliverable-aware-task-judgement-gate.md`
5. `core/main-pal-conductor-gate.md`
6. `core/runtime-adapter-shared-contract.md`
7. `core/project-binding-thin-contract.md`
8. `core/runtime-response-gate.md`

Pal source of truth:
- `contacts/pals.json`
- `registry/pal.index.json`

Default Main Pal:
- `pals/Mira-main/PAL.md`
- `pals/Mira-main/core/output-contract.md`

Do not use stale Pal lists copied into this project.
Do not preload all AgentPal files.
Load selected Pal assets on demand.
AgentPal v0.1 active mode is Simple Pal Mode only.
Deep Conductor, Subagent Mode, and external Agent orchestration are future design only.
Project questions mean this external project, not the AgentPal workspace.

Claude Code access to the AgentPal workspace is configured in `.claude/settings.local.json` when Claude Code is used.
<!-- END AGENTPAL WORKGROUP -->
```

Use this block as a lightweight binding only. Do not copy AgentPal Pal Packs into the external project.
