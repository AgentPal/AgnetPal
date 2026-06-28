# R116 PalSmith Asset Manifest Writeback Rollback Plan

Date: 2026-06-28

## Purpose

Define the rollback plan for a future R117 PalSmith official manifest writeback.

R116 does not write the official manifest.

## Rollback Target

If R117 writes an official manifest and a post-writeback gate fails, rollback should remove or revert only:

`official/pals/PalSmith-pal-governor/asset-manifest.json`

## Rollback Steps

1. Remove or revert `official/pals/PalSmith-pal-governor/asset-manifest.json`.
2. Confirm `official/pals/PalSmith-pal-governor/pal.json` remains unchanged.
3. Confirm `workspace/organization/contacts/pals.json` remains unchanged.
4. Re-run JSON parse checks for visible `.json` files.
5. Re-run PalSmith `pal.json` parse and all official Pal `pal.json` parse.
6. Confirm official manifest count returns to the expected pre-writeback state.
7. Confirm PalSmith still loads by root entries and directory convention fallback.
8. Record rollback evidence under `release/fresh-clone-checks/` or `release/integration-notes/`.

## Non-Targets

Rollback must not modify:

- central roster;
- `PAL_CONTACTS.md`;
- PalSmith `pal.json`;
- Mira or any other official Pal;
- PalSmith asset directories;
- external project `.agentpal/`;
- release tags or GitHub releases.

## Safety Note

R117 should commit the official manifest writeback separately from any later cleanup so rollback remains narrow and reviewable.
