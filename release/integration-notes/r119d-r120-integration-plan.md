# R119-D R120 Integration Plan

Date: 2026-06-28

## Purpose

This plan prepares the R120 single-thread integration round for R119-A/B/C Org Pack, FDE Pack, and reusable/private asset-boundary outputs.

R119-D does not perform the R120 integration. It defines the recommended integration order and boundaries.

## Recommended R120 Order

1. Start from a clean local worktree.
2. Read R119-A/B/C/D internal reports.
3. Read R119-A/B/C public outputs and validations.
4. Run `evals/palbench/org-pack/r119d-org-fde-integration-gate.md`.
5. Repair only integration-scoped issues.
6. Update shared navigation entries.
7. Run local validation.
8. Run clean-copy validation.
9. Commit locally.
10. Do not push, tag, fetch, pull, or create a release.

## Shared Navigation Updates

R120 may update the following only after R119-A/B/C evidence passes:

- `README.md`
- `README.zh-CN.md`, if present and in scope
- `RESOURCE_INDEX.md`
- `agentpal.json`, only if the existing schema supports navigation metadata and the change is explicitly scoped

Updates should add Org Pack / FDE / asset-boundary navigation only. They must not claim release publication, runtime execution, connector availability, marketplace availability, or automatic installation.

## Navigation Content To Add

Add concise links to:

- Org Pack practical structure and examples;
- FDE Pack standard and templates;
- reusable vs customer-private asset boundary;
- R119 PalBench gates and validation records;
- R120 integration summary and validation once created.

## R120 Required Checks

R120 should verify:

- R119-A files exist;
- R119-B files exist;
- R119-C files exist;
- R119-D gate / checklist / issue template / R120 plan exist;
- templates JSON parse;
- examples JSON parse;
- no credentials;
- no customer-private leak;
- no connector / marketplace / scanner;
- no keyword routing;
- central roster unchanged;
- official Pal unchanged;
- external project thin binding preserved;
- index update notes exist;
- no untracked R119 files left;
- clean-copy pass.

## Fix Policy

Allowed in R120:

- missing index update note;
- typo or heading repair in new R119 integration notes;
- navigation-only README / RESOURCE_INDEX / `agentpal.json` updates;
- public-safe template/example metadata correction;
- explicit `missing`, `not-run`, or `needs-review` status correction.

Not allowed in R120 without a separate task:

- Pal metadata rollout;
- new official Pal `asset-manifest.json`;
- central roster change;
- official Pal asset rewrite;
- connector, scanner, validator, installer, daemon, database, marketplace, hub, auto-sync, or auto-execution implementation;
- customer-private data insertion into reusable public packs;
- external project `.agentpal/` thick-binding writes.

## No Remote Action Policy

R120 must not run:

- `git push`
- `git pull`
- `git fetch`
- tag creation or modification
- GitHub Release creation or modification
- release/tag migration
- remote overwrite of local work

Remote publication belongs to a later explicit release task with current evidence.

## Expected R120 Commit

Suggested local commit message:

```text
docs: integrate org fde pack foundations
```

Use a different message if R120 narrows or changes the integration scope.
