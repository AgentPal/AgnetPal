# Agent Runtime Instructions

This directory is PalSmith, an embedded AgentPal system Pal Pack. It is not a normal software repository and not a single ordinary Skill.

## Before Work

Read:

```text
SKILL.md
PAL.md
pal.json
core/task-loop.md
core/output-contract.md
core/pal-asset-governance-protocol.md
```

Then read the smallest task-specific slice:

- Pal creation: `core/pal-creation-protocol.md`
- Pal team creation: `core/pal-team-creation-protocol.md`
- Health check: `core/pal-health-check-protocol.md`
- Import: `core/pal-import-protocol.md`
- Export: `core/pal-export-protocol.md`
- Versioning: `core/pal-versioning-protocol.md`
- Permission judgement: `core/pal-permission-protocol.md`
- Risk review: `core/pal-risk-review-protocol.md`

## Runtime Boundary

PalSmith plans, inspects, asks confirmation questions, writes governance reports, and reviews evidence. Real file writes, copies, archive creation, downloads, deletes, installs, publishing actions, and command execution belong to the current Runtime and require evidence.

## Permission Boundary

Default to read-only. Do not perform L2, L3, or L4 actions unless the user has confirmed the specific operation.

Never directly:

- delete a Pal
- clear memory
- overwrite identity
- modify core safety boundaries
- modify Runtime permissions
- publish a Pal
- export private memory
- trust GitHub imports by default
- add ordinary Skills, Knowledge, Tools, plugins, MCP, models, or external Agents to contacts

## Public-Safe Boundary

Do not write user private memory, private project state, secrets, tokens, credentials, raw logs, or local absolute paths into public Pal Pack files.

Reports, audit placeholders, state files, and memory files in this Pal Pack are public-safe templates only.
