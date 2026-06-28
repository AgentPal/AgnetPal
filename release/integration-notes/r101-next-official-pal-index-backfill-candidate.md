# R101 Next Official Pal Index Backfill Candidate

Date: 2026-06-28

## Purpose

This note identifies the safest next official Pal preparation candidate after
R101.

It is a candidate plan only. It does not modify official Pal files.

## Recommended Next Step

Run a small Batch 1 index/README backfill pilot before any `pal.json` v0.5
metadata rewrite or real `asset-manifest.json` generation.

Preferred candidate shape:

- one Pal first, or a very small batch;
- only add public-safe `index.md` or `README.md` files in existing asset
  directories;
- do not move, rename, delete, or rewrite existing assets;
- do not change `pal.json`;
- do not generate `asset-manifest.json`;
- do not modify central contacts;
- preserve `unknown`, `missing`, and `not-run`.

## Candidate Inputs

Use:

- `release/integration-notes/r100b-official-pal-metadata-upgrade-batch-plan.md`
- `release/integration-notes/r100b-official-pal-safe-index-file-plan.md`
- `templates/pal-asset/index-templates/`
- `templates/pal-asset/safe-index-backfill-guide.md`

## Suggested Pilot

A public-safe memory index placeholder for one Pal with an existing `memory/`
directory is the lowest-risk pilot shape.

The pilot should state:

- directory purpose;
- what belongs there;
- what must not belong there;
- public/private boundary;
- credential exclusion;
- that current evidence may remain `unknown`, `missing`, or `not-run`.

## Not Yet Recommended

Do not start with:

- all 9 official Pals;
- `asset-manifest.json` generation;
- PalSmith `memory/` or `learning/` directory creation;
- research index creation where content classification is unresolved;
- moving old files into new directories;
- converting Agent Skill references into Pal Skills.

