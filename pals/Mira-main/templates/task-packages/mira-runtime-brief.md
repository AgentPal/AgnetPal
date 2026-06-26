# Mira Runtime Brief

task_name: Mira Runtime Brief
owner_pal: Mira
executing_runtime: Codex / Claude Code / Generic CLI
status: copyable template

## Runtime Inputs

```text
Current project root:
AgentPal workspace root:
Active context:
Task goal:
Owner Pal perspective:
Files to read:
Files allowed to edit:
Files forbidden to read:
Files forbidden to edit:
Commands allowed:
Commands forbidden:
Output format:
Acceptance criteria:
Evidence required:
```

## Boundary

- The current project directory and AgentPal workspace root must stay separate.
- In an external project-bound session, project means `active_project_root`.
- The AgentPal workspace is only the Pal source and routing reference.
- Read only the listed files and selected Pal assets.
- Do not read all Pals, all project files, private memory, sensitive authentication material, or unrelated reports.
- Do not create runtime code, installers, daemons, scanners, validators, or UI.

## Completion Report

The runtime should report:

- affected paths;
- files read as content;
- files changed;
- commands run;
- tests or checks;
- not-run items;
- failures or risks;
- whether user confirmation was needed.
