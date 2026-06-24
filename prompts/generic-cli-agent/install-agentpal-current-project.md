# Generic CLI Agent Install AgentPal In Current Project

Use this with a Markdown/JSON-capable CLI Agent while your shell is inside an external user project.

This is a thin binding prompt. It does not copy AgentPal rules, Pals, protocols, docs, examples, evals, or release files into the project.

```text
Connect the current project to AgentPal for a generic CLI Agent.

Inputs:
- current project root: the current working directory
- AgentPal workspace root: ask me if it is not already known

Hard boundaries:
- Do not scan the whole disk.
- Do not create Claude-specific files.
- Do not copy AgentPal Pal Packs, docs, protocols, examples, evals, or release notes into this project.
- Do not create runtime code, scripts, services, daemons, installers, or UI.
- Do not activate Deep Conductor, Subagent Mode, external Agent orchestration, or multi-runtime automation.

Create or update only the thin binding:
1. `.agentpal/project.json`
2. `.agentpal/AGENTPAL.md`
3. root `AGENTS.md` protected block

The binding must say that AgentPal rules are read from the AgentPal workspace root.

Before responding as AgentPal in this project, the runtime must read from the AgentPal workspace root:
1. core/agentpal-core-gate.md
2. core/first-pal-gate.md
3. core/simple-pal-mode-runtime-contract.md
4. core/deliverable-aware-task-judgement-gate.md
5. core/main-pal-conductor-gate.md
6. core/runtime-adapter-shared-contract.md
7. core/project-binding-thin-contract.md
8. core/runtime-response-gate.md
9. contacts/pals.json
10. registry/pal.index.json
11. pals/Mira-main/PAL.md
12. pals/Mira-main/core/output-contract.md

Use `templates/project-binding/root-agents-agentpal-block-template.md` from the AgentPal workspace as the protected block shape.

Use `projects/project-workgroup-template/agentpal/` from the AgentPal workspace only as the thin `.agentpal/` template. Do not copy optional state, memory, reports, context, or index folders unless needed by a later task.

For `.agentpal/project.json`, include at least:
- schema
- binding_version
- active_project_root
- agentpal_workspace_root
- runtime_hint: generic-cli
- active_mode: simple-pal-mode-only
- read_core_from_agentpal_workspace: true
- core_gate_paths
- pal_source_of_truth

After install, reply with a short Mira welcome in my language:
- Start with `Mira：`.
- Say AgentPal is connected to this project.
- Say ordinary messages start with Mira.
- Say specialists can be called with `/pal Name`.
- Say official Pals are read from the AgentPal workspace contacts / registry.
- Say v0.1 uses Simple Pal Mode only.
```
