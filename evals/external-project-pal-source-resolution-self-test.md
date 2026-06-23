# External Project Pal Source Resolution Self-Test

## Purpose

Verify that an external project-bound session resolves Pals from the bound AgentPal workspace, not from the external project's lightweight `.agentpal/` folder.

## Test Setup

- External project has `.agentpal/project.json`.
- `.agentpal/project.json` contains `agentpal_workspace_root`.
- The bound AgentPal workspace contains `contacts/pals.json` and `registry/pal.index.json`.

## Test Input

```text
帮我做一下调研，有没有与 AgentPal 类似的程序。
```

## Expected Behavior

- Mira reads the external project binding files.
- Mira keeps `active_project_root` as the only current project.
- Mira reads only the bounded Pal discovery files from `agentpal_workspace_root`:
  - `contacts/pals.json`
  - `registry/pal.index.json`
- Mira does not scan all Pals.
- Mira does not treat external `.agentpal/` as the Pal asset store.
- Mira judges owner by AI routing judgement and hands off when a registered Pal can own the work.
- The selected owner Pal then reads its own Level 0 assets and relevant indexes / assets.

## Fail Signs

- Mira says the external project binding has no Pal portraits or output templates and therefore answers the specialist task herself.
- Mira performs web research, product planning, engineering advice, quality review, document work, or system diagnosis as Mira after skipping `agentpal_workspace_root/contacts` and `agentpal_workspace_root/registry`.
- Mira treats the AgentPal workspace as a second current project root.
- Mira reads all Pal Packs just to choose an owner.

