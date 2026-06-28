# R101 Official Pal Upgrade Gate Freeze

Date: 2026-06-28

## Purpose

This note freezes the minimum preflight and postflight gate for the next official
Pal metadata upgrade round.

R101 itself is a shared-navigation and gate-freeze round. It does not modify
`official/pals/**`, does not modify central contacts, and does not generate real
official `asset-manifest.json` files.

## Frozen Gate

Run this gate before any future official Pal metadata or manifest edit:

1. `git status --short --branch`
2. parse every visible `.json` file
3. parse `standards/schemas/pal.schema.json`
4. parse `standards/schemas/pal-asset-manifest.schema.json`
5. parse Pal asset JSON templates
6. parse `workspace/organization/contacts/pals.json`
7. verify registered active official Pal count is 9
8. verify official Pal directory count is 9
9. parse all official Pal `pal.json` files
10. verify `routing_policy` remains `ai_judgement_only`
11. verify `keyword_routing_allowed` remains `false`
12. verify no central roster diff unless a separate approved registration task
    exists
13. verify no out-of-scope official Pal diff
14. verify no active keyword/domain/role route map
15. verify no scanner, connector, marketplace, daemon, installer, auto sync, or
    auto execution behavior
16. verify no credential, token, password, cookie, API key, or secret values
17. verify no active thick external project binding
18. verify missing and not-run evidence stays visible

## Required Reference Gates

- `evals/palbench/pal-asset/r100b-official-pal-metadata-preflight.md`
- `evals/palbench/pal-asset/r100d-pal-metadata-upgrade-compatibility-gate.md`
- `evals/palbench/pal-asset/r100d-pal-manifest-backward-compatibility-cases.md`
- `release/integration-notes/r100d-official-pal-upgrade-gate-notes.md`

## Batch Rule

The next metadata-impacting upgrade must be one Pal or a small batch. Do not
rewrite all official Pals at once unless a prior one-Pal pilot has passed this
gate and the wider batch has a separate explicit approval.

## Commit Rule

Commit only after:

- preflight passes;
- the intended small batch is complete;
- postflight passes;
- selected R95 groups are rerun when shared entries or public safety surfaces
  changed;
- changed files match the approved scope.

Normal development rounds still must not push, pull, fetch, tag, create a
GitHub Release, or perform release/tag migration.

