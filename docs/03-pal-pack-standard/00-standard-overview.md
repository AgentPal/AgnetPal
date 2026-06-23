# Pal Pack Standard Overview

AgentPal v0.1.0-rc.1 is both a Pal Workspace and an early Pal Pack Standard practice.

The standard describes how to package a Pal so an agent runtime can read it, use it, verify its output, and maintain it over time.

## What The Standard Covers

- Pal identity and responsibility boundaries.
- Machine-readable metadata.
- Runtime entry files.
- Output contracts.
- Knowledge, skills, runbooks, and workflows.
- Memory, state, and report boundaries.
- Examples and evals.
- Contacts and registry rules.
- Public/private release boundaries.

## Workspace Vs Pal Pack

The AgentPal root is the workspace. It owns shared contacts, registry, orchestration, runtime notes, templates, prompts, examples, evals, release files, and public-safe placeholders.

A single Pal Pack lives under `pals/<Pal-Directory>/`. It owns one Pal's identity, professional assets, output contract, and learning rules.

## v0.1.0-rc.1 Boundary

This standard is file-driven. It does not require a service, package manager, UI, scanner, or installer.

## Related

- [Pal Pack structure](01-pal-pack-structure.md)
- [Root files](02-root-files.md)
- [Public/private boundary](11-public-private-boundary.md)
- [Pal Pack checklist](12-pal-pack-checklist.md)
