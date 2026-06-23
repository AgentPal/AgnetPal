# Failure: Claude Code Imports Entire AgentPal

## Bad Behavior

`CLAUDE.md` contains a direct import or pasted copy of AgentPal root files, for example:

```text
Read all of <path-to-AgentPal>/AGENTS.md and all files under <path-to-AgentPal>.
```

## Why This Fails

This causes context bloat and violates Context Slicing. `permissions.additionalDirectories` grants access to the AgentPal path, but it does not mean the whole workspace should be loaded.

## Correct Behavior

Use a lightweight AgentPal block:

- project root remains the active project
- AgentPal workspace is only a Pal source
- contacts / registry are used for discovery
- `RESOURCE_INDEX.md` and selected Pal assets are read on demand
- index-known paths are separated from content-read files
