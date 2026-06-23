# Capability Inventory Protocol

Capability Inventory describes what the current AgentPal environment may be able to use. It is a set of profiles, not a hard-coded routing system.

AgentPal v0.1.0-rc.1 does not automatically probe runtimes, models, Skills, plugins, MCP servers, or external agents. This protocol is a design foundation for future versions and for manual capability documentation.

## Purpose

Capability Inventory helps Mira or an owner Pal judge:

- which runtime may fit the task
- which model profile may fit the task
- which reasoning strength may be sufficient
- which Skill, plugin, or MCP server may help
- which Pal profile may own, consult, or verify
- which capabilities require user approval or execution-layer evidence

These profiles are judgement inputs only. They do not replace AI Judgement and must not become keyword triggers or fixed task-domain routes.

## Profile Types

| Profile | Purpose |
| --- | --- |
| Runtime Profile | What a runtime can read, write, execute, configure, and report |
| Model Profile | Strengths, known limits, cost/latency tier, compatible runtimes |
| Reasoning Profile | When low, medium, high, or deep reasoning may be useful |
| Skill Profile | What a Skill does, required tools, risk, expected output |
| Plugin Profile | Plugin capabilities, permissions, and evidence needs |
| MCP Profile | MCP tools/resources exposed, access boundary, risk |
| Pal Capability Profile | Pal identity, output contract, context needs, verification role candidates |

## Profile Source

Profiles may be maintained by:

- user-provided configuration
- Pal-authored notes
- maintainer examples
- future runtime probes
- future routing memory updates

v0.1 only ships templates and illustrative examples. It does not claim to know a user's installed runtime capabilities.

## Required Profile Fields

Every profile should include:

- `schema`
- `id`
- `name`
- `type`
- `status`
- `source`
- `version`
- `capabilities`
- `limits`
- `risk_notes`
- `evidence_required`
- `non_binding`

## Use In Judgement

Mira or an owner Pal may use profiles as follows:

1. Read current contacts / registry.
2. Read task goal and constraints.
3. Read only relevant capability indexes or profiles.
4. Select candidate capabilities.
5. Explain the judgement if asked.
6. Record outcome later through Routing Reward Memory when appropriate.

## Forbidden Use

Do not use Capability Inventory to create:

- task/domain route tables
- keyword-triggered routes
- fixed Pal sets
- fixed runtime choices
- hidden external Agent calls

## Future Versions

v0.2 may add manually refreshed capability inventory and simple validation.

v0.3 may add richer probes, routing memory feedback, and PalBench-driven profile tuning.
