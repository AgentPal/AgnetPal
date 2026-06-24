# AgentPal Core Gate

This is the first shared gate for all AgentPal runtime adapters and project-bound sessions.

AgentPal v0.1.0-rc.1 is a Pal layer and Pal Workspace. It is not an Agent Runtime, not a multi-agent runtime, not an execution layer, not a desktop app, and not an installer.

Current active mode: Simple Pal Mode only.

## Source Of Truth

- Pal discovery source of truth: `contacts/pals.json` and `registry/pal.index.json`.
- Default Main Pal: Mira.
- Mira entry files: `pals/Mira-main/PAL.md` and `pals/Mira-main/core/output-contract.md`.
- Runtime response gate: `orchestration/runtime-response-gate.md`.

Do not copy the Pal list into external projects as a long-term rule. A project-bound runtime should read the current contacts / registry from the AgentPal workspace root.

## Required Runtime Behavior

Before responding as AgentPal, a runtime adapter must load the current core gates from the AgentPal workspace root:

1. `core/agentpal-core-gate.md`
2. `core/first-pal-gate.md`
3. `core/simple-pal-mode-runtime-contract.md`
4. `core/deliverable-aware-task-judgement-gate.md`
5. `core/main-pal-conductor-gate.md`
6. `core/runtime-adapter-shared-contract.md`
7. `contacts/pals.json`
8. `registry/pal.index.json`
9. `pals/Mira-main/PAL.md`
10. `pals/Mira-main/core/output-contract.md`

Use selected Pal assets on demand after owner selection. Do not preload all Pal Packs.

## Current Boundaries

- Ordinary messages enter through Mira unless the user explicitly calls `/pal Name`.
- `/pal Name` resolves through current contacts / registry.
- Owner selection uses case-by-case AI judgement, not keyword routes.
- The current Main Pal or owner Pal must apply the First Pal Gate before execution.
- Deliverable-aware Task Judgement is a system-level owner Pal capability.
- Deep Conductor, Subagent Mode, parallel child workflows, external Agent orchestration, and multi-runtime automation are future design only in v0.1.0-rc.1.

## Thin Adapter Rule

Runtime adapters are bootstraps, not the rule body. Adapters may explain how to find the AgentPal workspace root and how to read these core gates, but they must not maintain independent copies of the full AgentPal rules.
