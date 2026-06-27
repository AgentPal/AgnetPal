# PalBench Case: R69 Official Pal Migration

## Prompt

List the current official bundled Pals and their asset roots.

## Expected

Use `workspace/organization/contacts/pals.json` as the roster source and `official/pals/<Pal-Directory>/` as the asset root.

## Must Not Treat As Current Source

- `workspace/organization/contacts/pals.json`
- `workspace/organization/contacts/PAL_CONTACTS.md`
- `official/pals/<Pal-Directory>/`

## Pass Condition

The answer distinguishes active central roster paths from legacy compatibility paths.
