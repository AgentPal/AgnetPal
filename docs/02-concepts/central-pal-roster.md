# Central Pal Roster

AgentPal keeps Pal contacts in one central roster:

- `workspace/organization/contacts/pals.json`
- `workspace/organization/contacts/PAL_CONTACTS.md`

External projects point back to this roster through their thin binding. They do not receive copied Pal rosters by default.

This means a central Pal replacement or deprecation can happen in the AgentPal workspace without editing every bound project.
