# Deep Conductor Master Goal

Deep Conductor is AgentPal's no-code coordination methodology for complex work.

Its goal is to improve outcomes inside existing host Agent Runtimes by making planning, allocation, context control, verification, and memory writeback more deliberate.

Deep Conductor is not an executor. It does not call Agents, run commands, write files, start background workers, or perform automatic multi-runtime orchestration. It produces no-code plans, Context Packets, Context Access Lists, and Runtime Skill-aware Task Packages for a host Runtime to execute with evidence.

## Core Goal

Deep Conductor coordinates:

- scheduling;
- task decomposition;
- planning;
- owner and verifier allocation;
- capability composition;
- context access control;
- prompt shaping;
- verification;
- routing and usage memory writeback.

The advantage comes from resource cognition, scheduling, context discipline, verification, and memory, not from AgentPal becoming a program.

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

## Candidate Rules

Candidates are never fixed routes.

A Deep Conductor packet may name a candidate Pal, host Runtime, model profile, reasoning profile, Runtime-installed Skill, plugin, or MCP server. That naming means "consider this because the current evidence and goal suggest it may help." It does not mean the candidate is available, authorized, or automatically invoked.

## Runtime Boundary

The host Agent Runtime remains responsible for:

- file reads and writes;
- shell commands;
- tool calls;
- browser or office-document operations;
- external publishing;
- system changes;
- evidence collection.

AgentPal remains responsible for:

- task judgement;
- owner and verifier selection;
- context boundaries;
- task package quality;
- verification requirements;
- routing memory structure;
- explaining what happened and what remains unverified.

## Acceptance

Deep Conductor guidance is acceptable when it:

- improves the host Runtime's chance of completing the user's real task;
- keeps Pal-owned Skills separate from Runtime-installed Skills;
- states evidence requirements;
- reports not-run and unavailable states honestly;
- avoids keyword routes and fixed owner maps;
- keeps private memory out of public examples;
- never claims automatic execution.
