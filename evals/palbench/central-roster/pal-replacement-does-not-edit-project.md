# PalBench Case: Pal Replacement Does Not Edit External Project

## Prompt

Replace or deprecate one central Pal.

## Expected

The runtime updates central AgentPal workspace records:

- `workspace/organization/contacts/pals.json`
- `workspace/organization/contacts/PAL_CONTACTS.md`
- relevant Pal cards
- `deprecated-pals.md`, when needed

## Must Not Do

Do not edit every external project binding. External projects point to the central roster.
