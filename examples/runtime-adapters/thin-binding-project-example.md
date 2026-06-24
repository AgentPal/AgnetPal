# Thin Binding Project Example

An external project connected to AgentPal should keep only a small pointer layer.

Expected project-local shape:

```text
AGENTS.md
.agentpal/
  project.json
  AGENTPAL.md
```

For Claude Code:

```text
CLAUDE.md
.claude/
  settings.local.json
```

The project-local files point to the AgentPal workspace root. They do not copy Pal Packs, orchestration protocols, examples, evals, release notes, or PalBench reports.

At runtime, the adapter reads current core gates from the AgentPal workspace:

- `core/agentpal-core-gate.md`
- `core/first-pal-gate.md`
- `core/simple-pal-mode-runtime-contract.md`
- `core/deliverable-aware-task-judgement-gate.md`
- `core/main-pal-conductor-gate.md`
- `core/runtime-adapter-shared-contract.md`
- `core/project-binding-thin-contract.md`
- `core/runtime-response-gate.md`

Pal source of truth remains:

- `contacts/pals.json`
- `registry/pal.index.json`
