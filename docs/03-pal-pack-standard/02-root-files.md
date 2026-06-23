# Root Files

## Status

Current for AgentPal `v0.1.0-rc.1`.

Pal Pack root files tell a runtime what this Pal is, how to load it, and where the machine-readable metadata lives.

## Required Root Files

| File | Purpose |
| --- | --- |
| `AGENTS.md` | Runtime instructions local to this Pal Pack |
| `PAL.md` | Human-readable identity, role, responsibilities, boundaries, collaboration policy |
| `README.md` | Maintainer and user entry point |
| `SKILL.md` | Skill-aware runtime entry; must say this is a Pal Pack, not one ordinary Skill |
| `pal.json` | Machine-readable id, display name, aliases, role, path, direct call, collaboration flags |

## Workspace Root Is Different

The AgentPal root also has `AGENTS.md`, `PAL.md`, `SKILL.md`, and `agentpal.json`, but those describe the whole workspace. A Pal Pack's root files describe only one Pal.

## Good Minimal Rule

If a runtime only reads five files before work, it should still understand:

- who the Pal is
- what the Pal owns
- what the Pal must not do
- how to invoke it
- where its output contract is

## Common Mistakes

- Writing `SKILL.md` as if the Pal were a single-purpose Skill.
- Omitting `pal.json`, which makes discovery harder.
- Letting a Pal maintain a hard-coded list of other Pals instead of using contacts and registry.
