# Pal Teams and Deep Conductor

## Status

Applies to AgentPal `v0.1.0-rc.1`.

- Pal Team concepts: current as documentation and methodology.
- Simple Pal Mode and Fast Route: current in `v0.1.0-rc.1`.
- Deep Conductor: future design, not active as a full runtime feature in `v0.1.0-rc.1`.
- Subagent calls and multi-agent execution: runtime-layer capabilities, not AgentPal Pal-layer capabilities.

AgentPal `v0.1.0-rc.1` is Simple Pal Mode only.

## Pal Is Not Only A Single Companion

A Pal can be used directly as one working companion. For many tasks, that is enough.

When work becomes more complex, multiple Pals can also collaborate as a Pal Team. The goal is not to make every Pal an independent Agent process. The goal is to organize professional perspectives, context boundaries, Task Packages, verification standards, and learning records.

## What A Pal Team Is

A Pal Team is a group of professional Pal Packs that coordinate work through the current runtime.

A Pal Team can help with:

- task understanding
- ownership judgment
- context organization
- Task Package creation
- professional review
- risk checks
- verification standards
- result summaries
- repeated-task learning

For example, a release-readiness task may involve:

- Mira for intake, routing, and summary
- Atlas for development and repository perspective
- Quinn for quality, evidence, and release gate review
- Morgan for documentation and file workflow perspective
- Rhea for system, command, path, and permission boundaries
- Nova for product scope and user-facing release framing
- Vega for research and source-quality review
- Harper for public communication and writing quality

These Pals do not all need to execute actions. Each Pal contributes a professional lens, bounded context needs, evidence requirements, or review standards.

## What A Pal Team Is Not

A Pal Team is not:

- a group of independent Agent runtimes
- every Pal becoming an Agent process
- a multi-agent runtime by itself
- a desktop app, web app, installer, daemon, or marketplace
- permission to call tools, run commands, or publish without runtime evidence and user approval where needed

AgentPal is a Pal layer. The host runtime performs execution.

## Simple Pal Mode

Simple Pal Mode is the current active path in `v0.1.0-rc.1`.

`/pal Atlas` means the current runtime works in Atlas Pal mode. It reads Atlas assets, follows Atlas boundaries, and uses Atlas output expectations.

It does not launch an Atlas Agent.

The same rule applies to every Pal. A Pal is a working companion and a Pal Pack. It is not an Agent process.

## Fast Route

Fast Route is the current clear-task handoff pattern.

Use Fast Route when:

- one owner Pal can reasonably handle the task
- the task is clear and bounded
- risk is low or can be handled with evidence requirements
- a multi-Pal workflow would add overhead without better results

Fast Route avoids turning every task into a multi-Pal meeting. It keeps common work small, fast, and auditable.

## Multi-Pal Collaboration

Some tasks need more than one professional perspective.

A Pal Team may collaborate through:

- owner Pal handoff
- consultant sections
- reviewer sections
- Context Packets
- Task Package fragments
- verification requests
- final summary

The important rule is bounded context. Multiple Pals should not all read everything by default. Each Pal should receive only the context needed for its role.

The owner Pal remains responsible for organizing the final answer or Task Package unless the workflow explicitly hands summary back to Mira.

## Subagent And Multi-Agent Calls

Subagent calls and multi-agent execution belong to the runtime layer.

Codex, Claude Code, or another runtime may provide ways to call subagents, run parallel workers, use tools, or delegate execution. AgentPal does not claim to be that runtime.

AgentPal can help decide whether such execution is useful. It can:

- shape the Task Package
- define context slices
- set output contracts
- limit what each execution unit should read
- define evidence requirements
- review returned results
- record routing and verification lessons

Pal Team prepares and reviews work. The runtime executes work.

## Deep Conductor

Deep Conductor is AgentPal's future advanced orchestration design for complex tasks.

It should judge:

- task complexity
- risk level
- runtime capability
- model and reasoning strength
- Skill, plugin, MCP, and tool availability
- Pal ownership and review needs
- context access boundaries
- verification path
- routing memory and repeated-task learning

Deep Conductor is not active as a full runtime feature in `v0.1.0-rc.1`.

In future releases, Deep Conductor may combine Task Judgement Packets, Capability Inventory, Workflow Topology, Context Access Lists, Task Packages, Pal Isolation, Verification Result Records, Routing Decision Records, and Routing Reward Memory.

## When Not To Use Deep Conductor

Not every task needs deep orchestration.

Do not use Deep Conductor when:

- Mira can answer an ordinary message directly
- a direct `/pal Name` call is enough
- Fast Route can hand the task to one owner Pal
- the task only needs a small Task Package
- the overhead would be larger than the benefit

Simple tasks should stay simple.

## Relationship Summary

| Layer | Meaning | AgentPal v0.1.0-rc.1 status |
| --- | --- | --- |
| Skill | A capability | Current, usually owned by a Pal or runtime |
| Pal | A working companion that organizes capabilities | Current as Pal Pack and Simple Pal Mode |
| Pal Team | A collaboration layer across professional Pals | Current as documentation and bounded same-runtime method |
| Subagent / multi-agent execution | Runtime-layer execution capability | Not provided by AgentPal itself |
| Deep Conductor | Future transparent orchestration mode for complex tasks | Future design, not active |

Skill is capability.

Pal is a working companion.

Pal Team is a collaboration layer.

Subagents and multi-agent execution belong to the runtime layer.

Deep Conductor is the future transparent orchestration mode for complex tasks.

AgentPal's current goal is conservative: keep `v0.1.0-rc.1` usable through Simple Pal Mode while documenting a clear future path for more complex orchestration.
