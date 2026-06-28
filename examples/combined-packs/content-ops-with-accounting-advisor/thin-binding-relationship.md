# Thin Binding Relationship

## Default Rule

External projects remain thin-bound. The combined Org/FDE example belongs in
the AgentPal Workspace public example area and is referenced from project
records or task packages when relevant.

## Allowed Project-local Binding Files

An external project binding may include only thin pointers and protected blocks
such as:

- `.agentpal/project.json`
- `.agentpal/AGENTPAL.md`
- `AGENTS.md` protected block
- `CLAUDE.md` protected block
- `.claude/settings.local.json`
- `.gitignore` entry

These files may identify the active external project, the AgentPal Workspace,
the central project record, and runtime-adapter guidance. They must not become
the storage place for public reusable packs or customer-private evidence by
default.

## Forbidden Default Project-local Directories

Do not create or copy these directories into an external project by default:

- `.agentpal/org-pack/`
- `.agentpal/fde-pack/`
- `.agentpal/pals/`
- `.agentpal/workflows/`
- `.agentpal/memory/`
- `.agentpal/reports/`
- `.agentpal/capability-inventory/`
- `.agentpal/business-systems/`

## Why This Boundary Exists

Thin binding keeps project identity and runtime bootstrapping local while
preserving reusable Org Pack, FDE Pack, Pal, memory, report, capability, and
governance assets in the AgentPal Workspace or approved private project
records. It prevents accidental public reusable asset drift, private customer
data leakage, and copied central Pal assets in external projects.
