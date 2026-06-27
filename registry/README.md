# Legacy Registry Compatibility Pointer

`registry/` is a legacy compatibility directory from the pre-v0.4 layout.

The active central Pal roster source of truth is now:

- `workspace/organization/contacts/pals.json`
- `workspace/organization/contacts/PAL_CONTACTS.md`
- `workspace/organization/contacts/aliases.json`

Official Pal Packs now live under:

- `official/pals/`

Legacy registry files may remain useful for migration audits and older release notes, but new docs, templates, project bindings, and initialization paths must not treat `registry/pal.index.json` as the active central roster source.

Resource indexes that remain in this directory are compatibility references. Future R70/R71 cleanup may move or archive them behind the central workspace structure.


