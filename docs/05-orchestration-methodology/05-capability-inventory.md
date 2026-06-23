# Capability Inventory

Capability Inventory is AgentPal's method for describing what the current environment may be able to use.

It covers runtime, model, reasoning, Skill, plugin, MCP, and Pal capability profiles. Profiles are judgement inputs, not route rules.

## Status

- Current: Available as public-safe profile templates, illustrative examples, and capability matrices. No automatic scan is active in v0.1.0-rc.1.
- Future: May support manual refresh, validation, richer profiles, and routing-memory feedback.
- Research: PalBench can evaluate whether capability awareness improves Skill activation accuracy, runtime fit, verification quality, and cost per accepted result.

## Why it exists

AgentPal scheduling depends on facts that may change:

- what the host runtime can read or write
- whether shell, browser, plugin, MCP, or Skill access exists
- which model profiles are available
- what reasoning strengths are supported
- what evidence a tool can produce

Capability Inventory makes these facts explicit instead of forcing users to remember them.

## How it works

A capability profile should describe:

- id and type
- status and source
- capabilities
- limits
- risk notes
- evidence required
- whether the profile is non-binding

Profile types include:

- Runtime Profile
- Model Profile
- Reasoning Profile
- Skill Profile
- Plugin Profile
- MCP Profile
- Pal Capability Profile

Mira or an owner Pal may use profiles during judgement, but final routing remains case-by-case.

## What it is not

- Not an automatic environment probe in v0.1.
- Not proof that a capability exists in the user's current session.
- Not a task-to-Pal routing table.
- Not a model leaderboard.
- Not a place to store secrets, private paths, credentials, or private project data.

## Use safely

If capability facts are unknown, say they are unknown until scanned or confirmed.

Do not infer availability from an example profile.

