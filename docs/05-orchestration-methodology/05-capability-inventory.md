# Capability Inventory

Capability Inventory is AgentPal's method for describing what the current environment may be able to use.

It covers host runtime, model, reasoning, Skill, plugin, MCP, tool, and Pal capability profiles. Profiles are judgement inputs, not route rules.

## Current v0.5 Status

Capability facts may come from:

- visible current runtime evidence
- a user-maintained manual profile
- a runtime-reported profile or explicit tool list

No automatic scan is active by default. If capability is unknown, say it is unknown.

## Why It Exists

AgentPal scheduling depends on facts that may change:

- what the host runtime can read or write
- whether shell, browser, plugin, MCP, or Skill access exists
- which model profiles are available
- what reasoning strengths are supported
- what evidence a tool can produce

Capability Inventory makes these facts explicit instead of forcing users to remember them.

## Profile Contents

A capability profile should describe:

- id and type
- status and source
- capabilities
- limits
- risk notes
- evidence required
- whether the profile is non-binding

Profile types include runtime, model, reasoning, Skill, plugin, MCP, tool, and Pal capability profiles.

## What It Is Not

- Not an automatic environment probe.
- Not proof that a capability exists in the current session.
- Not a task-to-Pal routing table.
- Not a model leaderboard.
- Not a place to store secrets, private paths, credentials, or customer data.

## Safe Use

Mira or an owner Pal may use profiles during judgement, but final routing remains case-specific.

Do not infer availability from an example profile. Ask the host runtime to confirm when the capability matters.
