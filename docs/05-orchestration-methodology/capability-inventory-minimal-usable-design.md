# Capability Inventory Minimal Usable Design

Capability Inventory is AgentPal's public-safe profile set for describing possible runtime, model, reasoning, Skill, plugin, MCP, and Pal capabilities. It helps Mira and owner Pals make better AI Judgement decisions without turning those decisions into hard-coded routes.

## What It Is

Capability Inventory is a small set of hand-written or maintainer-provided profiles:

- Runtime Profiles describe what a host runtime may be able to read, write, execute, configure, and report.
- Model Profiles describe model tendencies, availability candidates, cost/latency notes, and reasoning modes.
- Reasoning Profiles describe when low, medium, high, or xhigh reasoning may be useful.
- Skill Profiles describe what a Skill can help with, inputs, outputs, tools, limits, and evidence needs.
- Plugin Profiles describe plugin capabilities, permissions, risk, and evidence needs.
- MCP Profiles describe MCP-hosted tools/resources, access boundaries, and evidence needs.
- Pal Capability Profiles describe Pal identity, capability domains, output contracts, context needs, handoff notes, and verification style.

Profiles are inputs to Task Judgement. They are not automatic decisions.

## Why v0.2 Uses Manual Profiles

v0.2 deliberately starts with manual or semi-manual profiles because AgentPal remains a no-code Pal layer. Automatic environment scanning would create a new runtime product surface, new permission questions, and new failure modes.

Manual profiles are enough for the first useful version:

- maintainers can document common runtime shapes;
- users can copy and adapt examples;
- Mira or an owner Pal can read a small relevant profile slice;
- Task Packages can name evidence required before execution claims;
- false confidence is avoided because examples do not claim to describe the user's current machine.

## How Profiles Support AI Judgement

Typical flow:

1. Mira or the current owner Pal performs Task Judgement from the user goal.
2. The Pal decides whether Capability Inventory would materially improve the decision.
3. The Pal reads the smallest relevant profile index or profile, not the whole inventory.
4. The profile becomes one judgement input alongside user intent, deliverables, risk, contacts, registry, Pal assets, and available Runtime evidence.
5. The Pal outputs candidates, not rules.
6. If execution is needed, the Pal produces a Task Package or Context Access List.
7. After completion, experience may be recorded manually in an appropriate public-safe asset. v0.2 does not auto-write Routing Reward Memory.

## Profile Loading Budget

Profile loading follows Context Slicing:

- read one profile family index before opening examples when possible;
- load only the profile needed for the current stage;
- keep Runtime, Model, Skill, Plugin, MCP, and Pal profiles separate;
- do not read all profiles by default;
- report profile paths as content-read only when actually opened.

## Not A Routing Table

Profiles must not say:

- a task type always belongs to one Pal;
- one runtime always handles one artifact type;
- one model is always required for one task;
- one Skill, plugin, or MCP server should be invoked automatically.

Allowed wording:

- "candidate";
- "may help when";
- "depends on current runtime setup";
- "requires current evidence";
- "not a fixed route".

## Relationship To v0.3

Capability Inventory is useful now as a manual judgement input. In a later v0.3 track, richer Deep Conductor design, Routing Reward Memory, PalBench feedback, or runtime-provided capability data may refine profiles.

That future direction does not make v0.2 an automatic capability scanner. v0.2 does not activate Deep Conductor, automatic multi-agent execution, automatic profile refresh, or automatic model selection.

## What v0.2 Does Not Do

- It does not automatically scan the user's machine.
- It does not automatically call external Agents.
- It does not automatically choose or switch models.
- It does not replace user or runtime permission settings.
- It does not prove a runtime, model, Skill, plugin, or MCP server is available now.
- It does not replace current Task Judgement.
- It does not remove the need for evidence before execution claims.

## Acceptance

Capability Inventory is minimally usable when:

- runtime, model, reasoning, Skill, plugin, MCP, and Pal profile templates exist;
- illustrative examples parse as JSON;
- examples are marked `illustrative` and `not_auto_detected`;
- profiles are documented as AI Judgement inputs, not fixed routes;
- self-tests check profile loading budget, no fixed routing, and no runtime-code boundary.
