# Why Pal?

## Status

Current concept document for AgentPal `v0.1.0-rc.1`.

This page explains why AgentPal uses the Pal concept, why Skills and Agent teams leave a real middle-layer gap, and why the name is Pal.

## The Real Problem

Users increasingly use agent runtimes for automation and professional work: coding, documents, research, file workflows, content, testing, release checks, and project maintenance.

When users want to make agents work better, the usual answers are:

- add more Skills
- build an Agent team

Both are useful, but neither fully solves the day-to-day organization problem.

Skills are lightweight, but they are usually fragmented. Agent teams can be powerful, but they are often heavy to configure, coordinate, and maintain. Many users do not need a full Agent team at the start. They need a working layer that understands goals, organizes capabilities, controls context, preserves useful memory, and checks results.

That missing middle layer is what AgentPal calls a Pal.

## Why Skills Are Not Enough

Skill is a capability.

A Skill can teach an agent runtime how to do one focused thing: generate a document, check a contract, write a specific report, run a test, call a tool, or organize a file type.

That is valuable, but it creates practical problems as the number of Skills grows.

Users may not remember:

- which Skills are installed
- which Skill fits the current task
- how to trigger a Skill
- what input a Skill needs
- which Skills can be combined
- which Skill is outdated, duplicated, or unreliable
- which Skill worked well last time

Skills are usually single-purpose. They do not normally own long-term project context, user preference, workflow history, verification habits, or cross-task memory. They may produce an output, but they usually do not own the full responsibility of deciding whether the result is complete.

Users should not need to remember hundreds of skills. They should be able to remember a few Pals and what they are responsible for.

## Why Agent Teams Can Be Too Heavy

Agent teams are useful for complex execution, parallel work, and large automated workflows. They can also be expensive and difficult to operate.

A real Agent team often needs:

- role configuration for each Agent
- tool permissions
- context boundaries
- communication rules
- result merging
- conflict handling
- cost and token controls
- execution evidence and review rules

Multi-agent workflows can duplicate context. The same project background, user preference, and task goal may be loaded several times. If coordination is weak, each Agent may understand the task differently, and the user may not know which result is authoritative.

Agent teams are best suited for heavier automation, advanced users, or tasks where parallel execution is worth the added coordination cost.

Many users simply want their current runtime, such as Codex, Claude Code, or another Markdown/JSON-capable CLI agent, to work with better context and clearer standards.

## The Missing Middle Layer

The gap is between scattered Skills and full Agent teams.

AgentPal defines Pal as the middle working layer:

- lighter than a full Agent team
- broader than a single Skill
- portable across compatible runtimes
- structured enough to hold identity, knowledge, Skills, workflows, memory rules, output contracts, verification, and collaboration protocols

Pal is not a bigger Skill. Pal is not a replacement for agents. Pal helps existing agent runtimes work with better context, clearer task packages, and stronger verification.

## Why The Name Pal

In real work, a person in a role carries many layers of knowledge and skill:

- general education
- professional training
- role-specific knowledge
- company-specific processes
- tools and systems
- history and preferences
- habits for judging whether work is complete

An accountant is not just someone who has a "make spreadsheet" Skill. A developer is not just someone who has a "write code" Skill. A document specialist is not just someone who has a "format document" Skill.

In real work, we do not remember every skill a coworker has. We remember people and roles.

We do not usually say:

```text
Use skill A, skill B, and skill C.
```

We say:

```text
Ask the accountant.
Ask QA.
Ask the developer.
Ask the document specialist.
```

A Pal turns hundreds or thousands of Skills, knowledge cards, workflows, and memories into a few memorable working companions.

That is why the concept is called Pal. It is a human-friendly working companion, not a single tool.

## What A Pal Is

A Pal is a portable working companion made of:

- identity
- knowledge
- Skills
- memory rules
- workflows and runbooks
- context rules
- output contracts
- verification habits
- collaboration protocols

A Pal is not:

- a single Skill
- an independent Agent process
- a new Agent runtime
- a desktop app, web app, installer, daemon, or marketplace

In AgentPal `v0.1.0-rc.1`, a Pal is loaded by the current runtime in Simple Pal Mode. `/pal Name` enters that Pal's working mode. It does not launch a separate Agent.

## How AgentPal Solves This

AgentPal gives compatible runtimes a Pal layer.

### Pal Manages Skills

The user does not need to remember every Skill. A Pal can judge which Skills, runbooks, workflows, knowledge cards, or fallback methods fit the task.

If no good Skill exists and the task repeats, the Pal can turn the repeated work into a Skill, runbook, workflow, or knowledge card.

### Pal Carries Memory Boundaries

A Pal can preserve useful working context without publishing private memory. It can distinguish user preference, project state, public-safe knowledge, and runtime-private material.

### Pal Organizes Workflows

A Pal can turn a vague goal into a clearer path: understand the task, choose context, prepare a Task Package, request evidence, review output, and summarize next steps.

### Pal Controls Context

AgentPal uses Context Slicing and Asset Loading Budget rules so the runtime reads the right small slice instead of the whole workspace.

### Pal Verifies Results

A Pal should not accept "done" without evidence. It can ask whether files changed, commands succeeded, links work, tags point to the intended commit, and outputs satisfy the user's original goal.

## Skill Vs Pal

| Dimension | Skill | Pal |
| --- | --- | --- |
| Core idea | A focused capability | A working companion that organizes capabilities |
| Typical scope | One task type or method | Goal understanding, context, workflow, verification, and memory rules |
| Identity | Usually none or minimal | Clear role, boundary, tone, and responsibility |
| Memory | Usually not owned by the Skill | Can define memory and learning boundaries |
| Workflow | Usually short or single-purpose | Can organize multi-step work |
| Verification | Often limited | Should define evidence and acceptance expectations |
| User experience | User chooses the Skill | User asks the Pal responsible for the work |
| Best for | Reusable single capability | Professional work that needs context and judgment |

Skill is a capability. Pal is a working companion that organizes capabilities.

## Agent Team Vs Pal Team

| Dimension | Agent Team | Pal Team |
| --- | --- | --- |
| Core unit | Multiple Agent runtimes or Agent processes | Multiple Pal Packs used by the current runtime |
| Execution | Agents may execute directly | Pals shape tasks; the runtime executes |
| Configuration weight | Higher | Lower in Simple Pal Mode |
| Context use | Can duplicate context across Agents | Can use Context Slicing and Task Packages |
| Coordination | Agent-to-Agent workflow | Pal handoff, consultation, review, and summary |
| Best for | Heavy automation and parallel execution | Organizing professional perspectives before, during, or after runtime execution |
| v0.1.0-rc.1 status | Not provided by AgentPal | Methodology and Simple Pal Mode collaboration only |

Pal Team is not a multi-agent runtime. It is a collaboration layer made of professional Pal Packs.

## Summary

Skill solves a single capability.

Agent teams solve complex execution.

Pal solves the organization problem between users, capabilities, context, workflow, memory, and verification.

AgentPal does not replace existing agent runtimes. It helps them work with clearer roles, better context, stronger Task Packages, and more reliable completion checks.
