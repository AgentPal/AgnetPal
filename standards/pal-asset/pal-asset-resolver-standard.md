# Pal Asset Resolver Standard

Date: 2026-06-28

## Purpose

The Pal Asset Resolver is a logical no-code judgement process for deciding which Pal-owned assets and supporting context should be considered for a task.

It helps a Runtime, Brain, Mira, or current owner Pal form candidate references to:

- Pal Skills
- Workflows
- Runbooks
- Knowledge
- Memory
- Evals
- Agent Skill refs
- Context Access Lists
- Task Package recommendations
- Verification plans

It does not run as a program. It does not execute tasks. It does not route by keyword. It does not call external APIs.

## Status

This is a Markdown / JSON / protocol standard for AgentPal. It is not:

- CLI
- Web App
- Desktop App
- scanner
- validator
- installer
- daemon
- database
- connector
- marketplace or hub program
- auto sync engine
- auto execution engine
- keyword router
- deterministic semantic router

## Inputs

A Pal Asset Resolver judgement may use the following inputs when available and allowed:

| Input | Meaning | Boundary |
| --- | --- | --- |
| user task | The current user goal, constraints, deliverables, and language. | Do not infer hidden requirements. |
| pal id or candidate Pal list | A direct `/pal Name`, owner judgement candidate, or staged owner list. | Candidate only unless direct call is explicit. |
| central roster | `workspace/organization/contacts/pals.json` and `PAL_CONTACTS.md`. | Source of truth for Pal identities; not modified by resolver. |
| Org Pack recommendations | Recommended Pals, workflows, governance, and verification notes. | AI judgement input only; not route map. |
| project binding | External project `.agentpal/project.json` and `.agentpal/AGENTPAL.md` when bound. | Binding context only; no copied Pal body. |
| project record | `workspace/projects/<project-id>/` central record. | Project memory and capability records stay central by default. |
| Capability Inventory | Runtime, model, Skill, plugin, MCP, Pal, and business-system profiles. | No automatic scan, no keyword route, no external call. |
| available Runtime / model / skill / plugin / MCP notes | Current or recorded availability evidence. | Unknown or stale evidence stays unknown until current evidence exists. |
| current memory | Approved public-safe or project-approved summaries. | Do not load private memory broadly. |
| risk / approval boundaries | Safety, privacy, write, release, credential, external-system, and user-confirmation requirements. | High-risk actions require explicit approval and runtime evidence. |

## Outputs

A Pal Asset Resolver judgement should produce candidates and package guidance, not actions:

| Output | Meaning |
| --- | --- |
| candidate Pal Skills | Pal-owned methods that may fit the task. |
| candidate Workflows | Pal or Org Pack workflow candidates. |
| candidate Runbooks | Review or operational runbook candidates. |
| candidate Knowledge | Knowledge cards or indexes that may be relevant. |
| candidate Memory | Approved memory summaries or memory read needs. |
| candidate Evals | PalBench or Pal-owned evals that can verify behavior. |
| candidate Agent Skill refs | Host-runtime Skill, plugin, MCP, or tool candidates that may need availability checks. |
| context access list | Minimal can-read / cannot-read / need-output set. |
| task package recommendation | No-code Runtime Task Package outline when execution is needed. |
| verification plan | Evidence requirements, not-run handling, blockers, and acceptance criteria. |

## Resolver Process

1. Confirm task shape and deliverables.
2. Resolve the active context:
   - AgentPal Workspace, or
   - external project bound by thin binding.
3. Read central roster from the AgentPal Workspace.
4. If the task names a Pal, resolve it by display name and aliases.
5. If the task is ordinary or composite, use AI judgement to identify Pal candidates from the central roster.
6. Read only the selected or candidate Pal's loading-order slice from `pal-loading-order-standard.md`.
7. Read Org Pack recommendations only when the task or project record references an Org Pack, or when an organization pattern is explicitly in scope.
8. Read project binding only for bound external project context.
9. Read central project record only for relevant project memory, source map, task package, reports, or capability inventory.
10. Read Capability Inventory profiles only when availability, business-system, runtime, Skill, plugin, MCP, or risk context matters.
11. Produce candidate assets and a minimal context access list.
12. If real execution is needed, produce a task package recommendation rather than executing.
13. Produce a verification plan that preserves `unknown`, `not-run`, `missing`, and `blocked` states.

## Org Pack Relationship

Org Pack recommendations are AI judgement inputs only.

They may suggest:

- Pals to consider
- workflow candidates
- governance checkpoints
- capability references
- memory policy
- verification checklist

They must not:

- copy the central roster
- replace the central roster
- force a Pal owner
- define keyword routes
- define domain routes
- define role maps
- write into an external project `.agentpal/`
- change project binding files
- modify `workspace/organization/contacts/pals.json`

## Thin Binding Relationship

External projects provide binding and business context only.

A thin binding can provide:

- active project root
- AgentPal workspace root
- central project record ref
- runtime hint
- project-specific constraints
- current source files or docs when the user asks to read project content

It must not provide default local copies of:

- Pal Packs
- Org Packs
- central contacts
- Pal memory
- Pal workflows
- Pal evals
- Capability Inventory
- Business System profiles
- governance decision records

Default project-local `.agentpal/` thick directories remain forbidden unless the user explicitly approves a separate, public-safe, project-specific artifact outside the default binding path.

## Capability Inventory Relationship

Capability Inventory profiles can inform:

- host Runtime availability
- model or reasoning suitability
- Agent Skill / plugin / MCP candidates
- Business System governance
- evidence needs
- privacy and credential boundaries
- risk and approval requirements

They must not:

- probe the machine automatically
- scan plugins automatically
- call MCP tools automatically
- call external business systems automatically
- create connectors
- infer permissions from a system name
- make a Pal or Runtime selection deterministic
- convert `unknown` or `not-run` into `pass`

## Agent Skill Refs

An Agent Skill ref is a host-runtime capability candidate. It is not a Pal-owned Skill.

The resolver may name an Agent Skill ref only as a candidate with:

- availability: `available`, `unavailable`, `unknown`, or `not-run`
- evidence source
- fallback if unavailable
- required confirmation if it can change files, systems, or external data

Agent Skill refs must not be stored as Pal contacts and must not be treated as Pal-owned Skills.

## Memory Boundary

Memory candidates may include:

- approved public-safe organization memory
- central project memory summaries
- routing memory summaries
- runtime usage memory summaries
- verification memory summaries

Do not load raw private memory, private project reports, user secrets, or customer evidence unless the task explicitly allows that read and the current Runtime boundary permits it.

## Verification Plan Requirements

Every resolver result should state:

- what evidence would prove the candidate asset set is sufficient
- what checks are not-run
- what is missing
- what would block execution
- which owner Pal should review the final evidence
- whether a Runtime Task Package is needed

No evidence, no pass.

## Forbidden

The Pal Asset Resolver must not:

- keyword route
- domain route
- use a hardcoded role map
- execute directly
- call external APIs automatically
- call MCP tools automatically
- create scanners, validators, daemons, or connectors
- copy Pal assets into an external project
- copy Org Pack assets into an external project by default
- create external project `.agentpal/pals/`
- create external project `.agentpal/workflows/`
- create external project `.agentpal/evals/`
- create external project `.agentpal/capability-inventory/`
- create external project `.agentpal/business-systems/`
- modify central roster files
- store credentials, tokens, passwords, API keys, cookies, or secrets
- treat Org Pack recommendations as routes
- treat Capability Inventory as automatic discovery
- treat Agent Skill refs as Pal contacts

## Output Shape

Use this shape for a resolver result:

```text
resolver_target:
  task:
  active_context:
  selected_or_candidate_pals:
  central_roster_evidence:
  project_binding_evidence:
  org_pack_inputs:
  capability_inventory_inputs:
  candidate_pal_assets:
    skills:
    workflows:
    runbooks:
    knowledge:
    memory:
    evals:
  candidate_agent_skill_refs:
  context_access_list:
    can_read:
    cannot_read:
    need_output:
  task_package_recommendation:
  verification_plan:
  not_run:
  forbidden_actions_confirmed:
```

## Completion Bar

A resolver result is complete only when it:

- reads central roster evidence or reports it unavailable;
- keeps Org Pack recommendations as non-binding judgement input;
- keeps external project binding thin;
- distinguishes Pal-owned Skills from host Agent Skill refs;
- lists candidate assets instead of executing them;
- produces a Context Access List and task package recommendation when execution may be needed;
- includes a verification plan;
- preserves `unknown`, `missing`, `not-run`, and blockers.
