# Project Binding Thin Contract

External project binding should be thin.

The external project is the active user project. The AgentPal workspace is only a Pal source and routing reference.

## Required Files

Required in an external project:

- `.agentpal/project.json`
- `.agentpal/AGENTPAL.md`
- root `AGENTS.md` protected AgentPal block

Required for Claude Code projects:

- root `CLAUDE.md` protected AgentPal block
- `.claude/settings.local.json` with `permissions.additionalDirectories` including the AgentPal workspace root

## Optional / Lazy-Created

Create only when needed:

- `.agentpal/state/`
- `.agentpal/memory/`
- `.agentpal/reports/`
- `.agentpal/context/`
- `.agentpal/index/`

## Do Not Copy Into Project Binding

- full Pal list as source of truth
- full Mira assets
- full orchestration protocols
- full docs
- full examples
- full evals
- release notes
- PalBench reports

## Read From AgentPal Workspace

Before responding as AgentPal, the runtime should use `.agentpal/project.json` to locate `agentpal_workspace_root`, then read:

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

The project binding is a pointer and state holder, not a copy of AgentPal.
