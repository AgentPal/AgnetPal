# Project Binding Walkthrough

## Purpose

This walkthrough shows how an external project can be connected to AgentPal
while using the combined pack as a central AgentPal Workspace reference.

It does not create a real binding, write to an external project, install tools,
call APIs, scan systems, or copy pack assets into project-local `.agentpal/`.

## Default Rule

External projects remain thin-bound. The external project contains only binding
metadata and protected instruction blocks. The AgentPal Workspace remains the
source for Pals, Org Packs, FDE Packs, combined packs, review notes, and central
project records.

## Allowed Project-local Binding Files

Allowed files are:

```text
.agentpal/project.json
.agentpal/AGENTPAL.md
AGENTS.md protected block
CLAUDE.md protected block
.claude/settings.local.json
.gitignore entry
```

These files may identify:

- `active_project_root`
- `agentpal_workspace_root`
- `agentpal_project_record`
- active runtime hint
- central Pal contact source
- core gate paths
- thin binding policy

## Forbidden Default Directories

Do not create these directories in an external project by default:

```text
.agentpal/org-pack/
.agentpal/fde-pack/
.agentpal/pals/
.agentpal/workflows/
.agentpal/memory/
.agentpal/reports/
.agentpal/capability-inventory/
.agentpal/business-systems/
```

Also keep project-local `.agentpal/` free of copied central contacts, Pal
bodies, reusable pack bodies, private evidence, customer data, and credentials.

## How The Combined Pack Is Referenced

The project binding points to the AgentPal Workspace. The combined pack remains
at:

```text
examples/combined-packs/content-ops-with-accounting-advisor/
```

The central project record can record that the project used this combined pack,
but the external project should not receive a copied `.agentpal/org-pack/` or
`.agentpal/fde-pack/` directory by default.

## What Mira May Explain

Mira may explain that the external project is the active project, while the
AgentPal Workspace is the Pal and reusable asset reference. Mira may prepare a
context packet that says the combined pack is relevant.

Mira must not claim that AgentPal has installed a connector, scanned the
project, copied reusable pack assets, or created a marketplace workflow.

## What PalSmith May Review

PalSmith may review whether the binding remains thin:

- allowed files only;
- no copied Org/FDE/Pal directories;
- no project-private records inside `.agentpal/`;
- no credentials;
- no keyword route map;
- central project record used for private facts.

## Completion Evidence

A public-safe binding walkthrough can be considered valid when:

- allowed files are listed;
- forbidden directories are listed;
- external project facts are pointed to central project records;
- reusable pack assets remain in the AgentPal Workspace;
- no real project path or customer-private data is included.
