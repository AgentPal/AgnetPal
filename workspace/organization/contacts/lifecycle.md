# Pal Lifecycle

Pal status values:

- `active`: available for AI-judged routing and direct calls.
- `candidate`: present for review, not default routable.
- `deprecated`: kept for compatibility, not selected for new work unless directly requested.
- `retired`: no longer used; retained only in historical references.

Lifecycle changes must update:

- `workspace/organization/contacts/pals.json`
- `workspace/organization/contacts/PAL_CONTACTS.md`
- the relevant Pal card
- `deprecated-pals.md`, when status becomes deprecated or retired

External project bindings should not need changes when a central Pal is replaced or deprecated.
