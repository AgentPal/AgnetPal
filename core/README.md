# AgentPal Core Gates

This directory is the shared rule surface for AgentPal runtime adapters and external project bindings.

Runtime adapters such as Codex, Claude Code, and generic CLI agents should read these files from the AgentPal workspace root instead of copying full AgentPal rules into each adapter prompt or external project.

Start here:

1. `agentpal-core-gate.md`
2. `first-pal-gate.md`
3. `simple-pal-mode-runtime-contract.md`
4. `deliverable-aware-task-judgement-gate.md`
5. `main-pal-conductor-gate.md`
6. `runtime-adapter-shared-contract.md`
7. `project-binding-thin-contract.md`
8. `runtime-response-gate.md`

The detailed orchestration protocols remain under `orchestration/`. Core gates are the thin, shared entry rules that point runtimes to the current source of truth.
