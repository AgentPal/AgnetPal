# Publish Your Pal Pack

## Status

Current for AgentPal `v0.1.0-rc.1`.

Publishing means making a Pal Pack safe and discoverable. It does not mean a Pal marketplace is live.

## Before Registration

Complete the [Pal Pack checklist](../03-pal-pack-standard/12-pal-pack-checklist.md).

At minimum, verify:

- required files exist
- `pal.json` uses `type: pal-pack`
- `core/output-contract.md` exists
- placeholder indexes and README files exist
- memory, state, and reports are public-safe
- examples and evals use synthetic data

## Add To Contacts / Registry

Only after the directory is a valid Pal Pack, update:

- `contacts/pals.json`
- `contacts/PAL_CONTACTS.md`
- `registry/pal.index.json`
- `registry/pal.index.md`

These files are the source of truth for Pal discovery.

## Do Not Register

- ordinary Skills
- plugins
- models
- MCP servers
- runtimes
- raw repositories
- knowledge packs
- persona packs

## Final Smoke Check

Ask the runtime to call the Pal with `/pal Name` and verify the response uses the Pal identity, output contract, and an asset or fallback method.
