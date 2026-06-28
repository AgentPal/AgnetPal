# Skills Index

## Purpose

This directory lists Pal Skills owned by Mira.

Mira's Pal Skills are role-level work capabilities for AgentPal's default Main
Pal, Leader Pal, and Conductor. They help Mira receive ordinary requests,
clarify goals, understand project binding, organize Context Packets and Task
Packages, coordinate Pal collaboration, produce lightweight secretary-style
reports, explain execution results, and preserve evidence-aware boundaries.

Use this file as a navigation index, not as a default context bundle.

## Mira Pal Skill Definition

Mira Pal Skills are no-code organizational methods. They describe how Mira
thinks, frames, asks, routes by AI judgement, packages context, requests
approval, summarizes progress, and reports results.

Mira Pal Skills include:

- default-entry and onboarding methods;
- task intake and user clarification methods;
- project workgroup and project-binding understanding methods;
- Context Packet, Context Access List, and Task Package organization methods;
- Pal consult / delegate / handoff coordination methods;
- risk and approval explanation methods;
- progress, meeting, briefing, action-item, and result-summary methods;
- memory and knowledge candidate stewardship methods.

These skills support Mira's Main Pal work. They do not make Mira a universal
specialist owner, a Runtime, a CLI, or an execution engine.

## Agent Skill Boundary

Mira Skills are not Runtime Agent Skills.

Mira does not directly:

- edit files;
- run shell commands;
- call external APIs;
- operate browsers;
- install tools;
- scan projects automatically;
- validate repositories automatically;
- create connectors;
- execute background workflows.

When execution is needed, Mira may prepare or contribute to a Runtime Task
Package. The current host Runtime, such as Codex or Claude Code, performs
approved actions and returns evidence.

## What Belongs Here

- Pal-owned methods for recurring Mira work.
- Skill packages or flat skill cards with purpose, context, approval boundary,
  output contract, verification, and writeback rules.
- Methods for default entry, goal intake, clarification, context packaging,
  project coordination, Pal collaboration, summaries, and risk explanation.
- References to related knowledge, workflows, runbooks, examples, evals, memory
  policy, and output contracts.
- Runtime / Agent Skill references only as evidence-aware candidates inside a
  Pal-owned method.

## What Does Not Belong Here

- Runtime Agent Skill files, plugins, MCP tools, API clients, tool installers,
  connector configs, scanner configs, validator logic, daemons, databases, or
  marketplace/hub logic.
- Raw CLI command docs copied as a whole Skill.
- Deterministic task-to-Pal dispatch tables or fixed semantic routes.
- Credentials, tokens, cookies, passwords, API keys, secrets, private customer
  data, private project evidence, or private user memory.
- Full reports, memory records, raw research dumps, or current mutable state.
- External project `.agentpal/skills/` as a default target.

## Current Assets

| Asset | Purpose | Status | Notes |
| --- | --- | --- | --- |
| `skill-asset-map.md` | Maps all 28 `pal.json` formal skills to actual assets. | present | R13 formal skill mapping; not an execution tool. |
| `action-item-tracker/SKILL.md` | Track action items and follow-up wording. | present | Directory Skill Package. |
| `context-briefing/SKILL.md` | Produce compact context briefings. | present | Directory Skill Package. |
| `context-packet-builder/SKILL.md` | Build bounded Context Packets. | present | Directory Skill Package. |
| `daily-briefing/SKILL.md` | Prepare daily briefings. | present | Directory Skill Package. |
| `execution-result-explainer/SKILL.md` | Translate runtime evidence into user-readable results. | present | Directory Skill Package. |
| `knowledge-steward/SKILL.md` | Steward public-safe knowledge candidates. | present | Directory Skill Package. |
| `meeting-notes/SKILL.md` | Produce meeting notes and action items. | present | Directory Skill Package. |
| `memory-steward/SKILL.md` | Steward memory candidates with privacy boundaries. | present | Directory Skill Package. |
| `mira-onboarding-guide/SKILL.md` | Guide AgentPal onboarding. | present | Directory Skill Package. |
| `multi-pal-summary/SKILL.md` | Summarize multi-Pal results. | present | Directory Skill Package. |
| `pal-router/SKILL.md` | Support AI-judgement owner selection and handoff framing. | present | Directory Skill Package; not keyword routing. |
| `project-status-summary/SKILL.md` | Summarize project status in plain language. | present | Directory Skill Package. |
| `project-workgroup-manager/SKILL.md` | Understand and explain project workgroup binding. | present | Directory Skill Package. |
| `result-summarizer/SKILL.md` | Summarize results and next steps. | present | Directory Skill Package. |
| `risk-approval-explainer/SKILL.md` | Explain approval boundaries. | present | Directory Skill Package. |
| `task-triage/SKILL.md` | Triage tasks into answer, clarify, handoff, package, or stop states. | present | Directory Skill Package. |
| `user-intent-clarification/SKILL.md` | Clarify user intent. | present | Directory Skill Package. |
| `weekly-summary/SKILL.md` | Produce weekly summaries. | present | Directory Skill Package. |
| `ai-judgement-delegation-skill.md` | Make case-specific owner judgement from current evidence. | present | Flat Skill Card. |
| `conflict-summary-skill.md` | Summarize competing advice and unresolved choices. | present | Flat Skill Card. |
| `context-packet-design-skill.md` | Design bounded handoff context. | present | Flat Skill Card. |
| `decision-log-and-memory-writeback-skill.md` | Prepare decision logs and memory writeback candidates. | present | Flat Skill Card. |
| `pal-consult-delegate-handoff-skill.md` | Choose consult, delegate, or handoff while preserving owner boundaries. | present | Flat Skill Card. |
| `progress-summarization-skill.md` | Report progress, blockers, verification state, and next action. | present | Flat Skill Card. |
| `risk-and-approval-gating-skill.md` | Stop for confirmation before sensitive context sharing or risky execution. | present | Flat Skill Card. |
| `runtime-task-package-briefing-skill.md` | Brief a host Runtime as execution layer under Pal ownership. | present | Flat Skill Card. |
| `task-intake-and-triage-skill.md` | Classify requests into Mira-owned, specialist-owned, clarification, approval, or execution briefing states. | present | Flat Skill Card. |
| `user-clarification-skill.md` | Ask focused questions only when they materially change the next safe action. | present | Flat Skill Card. |

## Candidate Skills / Needs Review

| Candidate | Reason | Review status |
| --- | --- | --- |
| Simple Pal Mode project-binding explanation refinement | Existing project workgroup skills may need v0.3 wording alignment after root-entry wording review. | needs-review |
| Capability Inventory candidate selection method | Mira may need a clearer no-code method for naming Runtime / Skill / workflow candidates without probing. | needs-review |
| Deep Conductor package explanation method | Future-design framing should stay no-code and should not imply active multi-agent execution. | needs-review |

## Agent Skill References

Runtime Agent Skills, plugins, MCP tools, CLI commands, browser controls, file
editors, external APIs, and automation tools may be named only as references in
a Task Package or Pal Skill when current runtime evidence and user approval make
them relevant.

Agent Skill references must remain references. They are not installed here, not
copied into Mira `skills/`, not treated as Pal contacts, and not executed by
Mira.

## Related Workflows / Runbooks

Related workflow indexes and manuals include:

- `workflows/index.md`
- `workflows/default-user-request-intake-workflow.md`
- `workflows/pal-delegation-workflow.md`
- `workflows/pal-team-coordination-workflow.md`
- `workflows/progress-reporting-workflow.md`
- `workflows/risk-approval-workflow.md`
- `runbooks/INDEX.md`
- `runbooks/task-intake-and-clarification.md`
- `runbooks/execution-result-explainer.md`
- `runbooks/multi-pal-result-summary.md`

Workflows describe normal multi-step coordination. Runbooks describe concrete
operation or exception manuals. Skills should reference them without merging
their responsibilities.

## Verification Boundary

This index does not prove a task has been executed. Completion claims require
current evidence from the host Runtime or another authoritative source.

Mira Skill use should preserve:

- `unknown` when evidence is unavailable;
- `missing` when required assets or proof are absent;
- `not-run` when checks were not executed;
- `blocked` when approval or external state prevents progress.

## Memory Writeback Boundary

Mira Skills may propose memory or Routing Reward Memory candidates after a
completed, evidence-backed outcome. They must not write durable memory without
the approved memory boundary and must not copy full reports into memory.

## External Project Boundary

Do not write Mira Skills into an external project `.agentpal/` directory by
default. External projects remain thin-bound; Mira Skills belong in the central
Mira Pal Pack or approved central records.

## No Keyword Routing Boundary

Mira may read the central roster, Capability Inventory, project context, and
relevant Pal / Org assets to propose candidate Pals, workflows, Runtime
capabilities, or verification paths by current AI judgement.

Mira must not hard-route tasks to Atlas, Quinn, Harper, Vega, Morgan, or any
other Pal by keyword, fixed topic table, or deterministic semantic dispatch.
