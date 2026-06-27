# Legacy Contacts Compatibility Pointer

`contacts/` is a legacy compatibility directory from the pre-v0.4 layout.

The active central Pal roster source of truth is now:

- `workspace/organization/contacts/pals.json`
- `workspace/organization/contacts/PAL_CONTACTS.md`
- `workspace/organization/contacts/aliases.json`

Official Pal Packs now live under:

- `official/pals/`

Do not use this directory as the active central roster for new docs, templates, project bindings, or initialization paths. Existing files are retained only so older release notes, older local sessions, and migration audits can explain what changed.

When adding, replacing, deprecating, or removing a Pal, update the central roster under `workspace/organization/contacts/`. External project bindings should not copy this directory.

Unknown or invalid Pal candidates should be recorded through the current central organization workflow, not promoted here as active contacts.


