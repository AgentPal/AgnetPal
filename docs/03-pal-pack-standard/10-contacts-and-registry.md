# Contacts And Registry

## Status

Current for AgentPal `v0.1.0-rc.1`.

`contacts/` and `registry/` are the source of truth for Pal discovery.

## Source Files

- `contacts/pals.json`
- `contacts/PAL_CONTACTS.md`
- `contacts/mention-aliases.md`
- `registry/pal.index.json`
- `registry/pal.index.md`

## What They Control

- display name
- aliases
- directory path
- role
- direct call such as `/pal Atlas`
- discoverable / contactable state
- allowed collaboration modes

## What Must Not Enter Contacts

- ordinary Skills
- plugins
- models
- MCP servers
- runtimes
- raw repositories
- knowledge packs
- persona packs

These can support a Pal, but they are not Pals unless packaged as valid Pal Pack directories and intentionally registered.

## Maintenance Rule

Adding, removing, or renaming a Pal should mainly update contacts and registry. Individual Pal Packs should not maintain hard-coded route maps for other Pals.
