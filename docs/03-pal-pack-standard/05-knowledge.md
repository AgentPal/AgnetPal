# Knowledge

## Status

Current for AgentPal `v0.1.0-rc.1`.

`knowledge/` stores short, public-safe knowledge cards and an index that helps the runtime choose the right slice.

## Minimum

```text
knowledge/index.md
```

An empty or early Pal can start with only `knowledge/index.md`. The index should say what knowledge exists now, what is missing, and that the runtime should not load every file by default.

## Standard Pattern

```text
knowledge/
├─ index.md
├─ identity/
├─ methods/
├─ safety/
└─ references/
```

Use whatever subdirectories fit the Pal. Do not invent heavy structure before there is real content.

## Source Boundary

Do not copy large third-party documents, private user material, customer data, or unreleased project facts into knowledge cards. Link, summarize cautiously, and keep copyright and privacy boundaries visible.

## Current Information

Facts that change over time, such as prices, laws, API behavior, model names, or software versions, need fresh verification by the host runtime before use.
