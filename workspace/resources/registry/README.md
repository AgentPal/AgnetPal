# Workspace Registry Compatibility Records

These files were moved from the root `registry/` directory during R76 root cleanup.

They are compatibility and resource-reference records, not the central Pal roster source of truth.

The active central Pal roster source of truth is now:

- `workspace/organization/contacts/pals.json`
- `workspace/organization/contacts/PAL_CONTACTS.md`
- `workspace/organization/contacts/aliases.json`

Official Pal Packs now live under:

- `official/pals/`

Legacy registry files may remain useful for migration audits, resource navigation, and older release notes, but new docs, templates, project bindings, and initialization paths must not treat `workspace/resources/registry/pal.index.json` as the active central roster source.

Resource indexes in this directory are compatibility references.


