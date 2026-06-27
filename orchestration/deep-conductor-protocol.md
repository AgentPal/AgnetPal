# Deep Conductor Protocol

Deep Conductor is AgentPal's no-code coordination methodology for complex work.

It improves existing host Agent Runtime usage by making scheduling, task decomposition, planning, allocation, capability composition, context control, verification, and memory writeback explicit.

Deep Conductor is not an executor. It does not run commands, call external Agents, launch parallel workers, modify files, publish artifacts, or operate as an AgentPal runtime.

## Master Goal

Use the same available Pals, host Runtimes, models, reasoning modes, Runtime-installed Skills, plugins, MCP tools, project context, and verification evidence more effectively than ad hoc prompting.

Deep Conductor should help the current host Runtime:

- understand the user's deliverables;
- select Pal-layer owner and verifier candidates by AI judgement;
- select Runtime / Model / Reasoning / Runtime-installed Skill / Plugin / MCP candidates from current evidence;
- control context access;
- package execution instructions;
- collect final reports;
- verify results;
- write public-safe routing memory.

The strength comes from resource cognition, scheduling, context discipline, verification, and memory, not from AgentPal becoming a program.

## Master Loop

1. Receive Goal.
2. Load Pal / Project / Routing Memory.
3. Understand Deliverables.
4. Read Capability Inventory.
5. Identify Runtime / Model / Reasoning / Runtime-installed Skill / Plugin / MCP / Pal candidates.
6. Choose Workflow Topology.
7. Build Context Access Lists / Context Packets.
8. Shape Prompts by Runtime / Model / Skill capability.
9. Generate Runtime Skill-aware Task Packages.
10. Collect Final Reports.
11. Verify Results.
12. Synthesize, Explain, and Write Routing Memory.

## Outputs

Deep Conductor produces written, no-code artifacts:

- staged judgement;
- workflow topology;
- Context Access Lists;
- Context Packets;
- Runtime Skill-aware Task Packages;
- verifier packets;
- final report requirements;
- routing and usage memory writeback fields.

These artifacts can guide Codex, Claude Code, OpenCode, OpenHands, Gemini CLI, or another host Runtime. They do not prove that those Runtimes or Skills are available.

## Candidate Boundary

All Pal, Runtime, Model, Reasoning, Runtime-installed Skill, Plugin, and MCP names are candidates unless current execution evidence proves actual use.

Do not turn capability profiles into routes. Do not route by keyword, domain table, file extension, or hard-coded owner map.

## Version Boundary

AgentPal v0.1 and v0.2 remain Simple Pal Mode. v0.3 may document no-code Deep Conductor patterns, but those patterns are not automatic execution.

Deep Conductor docs, examples, templates, and evals do not authorize Subagent Mode, child-agent calls, external Agent orchestration, group chat, or multi-runtime automation.
