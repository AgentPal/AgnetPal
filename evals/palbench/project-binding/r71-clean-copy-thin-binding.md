# R71 Clean-Copy Thin Binding

## Case ID

R71-CLEAN-COPY-THIN-BINDING

## Goal

Verify that a clean copy assembled from Git-visible files preserves the thin external project binding model.

## Setup

- Assemble a clean copy without `.git/`.
- Include tracked files that still exist plus Git-visible untracked public assets.
- Exclude ignored runtime/private files.

## Evidence Paths

- `templates/project-binding/generic-codex/.agentpal/project.json`
- `templates/project-binding/generic-codex/.agentpal/AGENTPAL.md`
- `templates/project-binding/generic-codex/AGENTS.agentpal-block.md`
- `templates/project-binding/claude-code/CLAUDE.agentpal-block.md`
- `templates/project-binding/project-json-template.md`
- `standards/project-binding/thin-project-binding-standard.md`
- `standards/boundaries/thin-project-binding-boundary.md`

## Expected Result

- Binding templates include `binding_mode: thin`.
- Binding templates include `agentpal_project_record`.
- Binding templates point project records to `workspace/projects/<project-id>`.
- Binding templates resolve Pal contacts from the central workspace contacts.
- External projects do not receive full Pal Packs, memory, reports, workflows, or eval suites by default.

## Forbidden Result

- A template defaults to `.agentpal/memory`, `.agentpal/state`, `.agentpal/reports`, `.agentpal/context`, `.agentpal/index`, `.agentpal/pals`, `.agentpal/workflows`, or `.agentpal/evals`.
- A template copies full AgentPal workspace contents into an external user project.
- A template treats keyword routing as the owner-selection method.

## R71 Verification Notes

Use path existence checks, JSON parse checks, and `rg "\.agentpal/(memory|state|reports|context|index|pals|workflows|evals)"` classification.

