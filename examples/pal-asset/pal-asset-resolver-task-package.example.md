# Pal Asset Resolver Task Package Example

## Scenario

User task:

```text
用户在 content-ops-demo 项目中想整理 Notion 内容计划流程。
```

This example shows a logical Pal Asset Resolver result. It is public-safe and synthetic. It does not execute anything, call Notion, create a connector, store credentials, or write into an external project `.agentpal/` directory.

## Resolver Target

```yaml
resolver_target:
  task: "整理 content-ops-demo 项目的 Notion 内容计划流程"
  active_context: "external project bound by thin binding"
  expected_deliverable: "task package recommendation for organizing a content planning workflow"
  execution_status: "not-run"
```

## Required Reads

The current Runtime / Brain reads only the bounded sources needed for judgement:

1. central roster:
   - `workspace/organization/contacts/pals.json`
   - `workspace/organization/contacts/PAL_CONTACTS.md`
2. project binding:
   - `<content-ops-demo>/.agentpal/project.json`
   - `<content-ops-demo>/.agentpal/AGENTPAL.md`
3. central project record if present:
   - `workspace/projects/content-ops-demo/`
4. Org Pack recommendation if the project record or user task references it:
   - an approved Org Pack under the AgentPal Workspace, not the external project `.agentpal/`
5. Capability Inventory business-system profile:
   - organization profile or project profile for a Notion-like Business System, if present
6. selected Pal assets by loading order:
   - `pal.json`
   - `PAL.md`
   - `AGENTS.md`
   - `SKILL.md`
   - task-relevant index / workflow / runbook / knowledge / eval files only

## Candidate Pal Selection

Candidate Pal selection remains AI judgement.

The task mentions content and Notion, but that must not create a keyword route to Harper, Morgan, Vega, PalSmith, or any other Pal.

Possible candidates from the current central roster:

| Candidate | Why it may be considered | Non-route boundary |
| --- | --- | --- |
| Mira | Conductor for project-bound task intake and staged Task Package. | Mira is not default owner for specialist work. |
| Morgan | Document and file workflow judgement may fit workflow organization and source preservation. | Not selected by "Notion" or "content" keywords. |
| Harper | Writing/content craft may fit editorial planning language. | Not selected by "content" keyword. |
| Nova | Product/workflow scope may fit if user wants process design and prioritization. | Not selected by project category. |
| PalSmith | Pal/Org asset governance may fit if the task is about Org Pack or Pal asset recommendations. | Not used as a universal resolver. |
| Quinn | Verification plan and acceptance evidence candidate. | Not automatic verifier for every task. |

The selected owner must be decided from the user's actual deliverable, available project context, risk, and evidence.

## Org Pack Input

If an Org Pack recommends Pals or workflow candidates, treat it as:

```yaml
org_pack_recommendation:
  status: "input_only"
  may_suggest:
    - candidate_pals
    - workflow_candidates
    - governance_checkpoints
    - verification_checklist
  must_not:
    - force_owner_pal
    - define_keyword_route
    - copy_org_pack_into_external_project
    - modify_central_roster
```

## Capability Inventory Input

The Notion business-system profile, if present, is a governance input:

```yaml
business_system_profile:
  profile_type: "business-system"
  system_family: "notion-like"
  status: "example_or_project_confirmed_only"
  access: "unknown_until_confirmed"
  credentials: "must_not_store"
  external_writes: "requires_user_authorization_and_runtime_evidence"
  routing_boundary: "AI judgement input only"
```

It must not call Notion, discover Notion workspaces, validate credentials, sync pages, or infer write access.

## Candidate Assets

Example candidate asset set:

```yaml
candidate_pal_assets:
  workflows:
    - pal: "Morgan"
      candidate_ref: "document workflow or source organization workflow"
      reason: "workflow organization and content preservation may be central to the task"
      availability: "requires selected Pal asset read"
    - pal: "Harper"
      candidate_ref: "content planning or editorial structure workflow"
      reason: "may help if the deliverable is editorial plan quality"
      availability: "requires selected Pal asset read"
  runbooks:
    - candidate_ref: "project-bound task package runbook"
      reason: "execution should remain in the central project record"
  knowledge:
    - candidate_ref: "Capability Inventory Notion business-system profile"
      reason: "Notion access/write boundaries affect task package"
    - candidate_ref: "Org Pack workflow policy"
      reason: "Org Pack recommendations can inform reusable workflow shape"
  memory:
    - candidate_ref: "workspace/projects/content-ops-demo/memory/project-memory.md"
      reason: "project-specific process memory if approved and present"
      privacy: "central project record only"
  evals:
    - candidate_ref: "pal-asset resolver thin-binding boundary eval"
      reason: "checks no keyword route, no connector, no external project thick write"
```

## Candidate Agent Skill Refs

```yaml
candidate_agent_skill_refs:
  - name: "Notion connector or MCP"
    status: "not-run"
    role: "availability candidate only"
    fallback: "manual Notion facts from user or public-safe project notes"
    boundary: "must not call external API unless user explicitly authorizes and current Runtime provides evidence"
```

Agent Skill refs are not Pal-owned Skills and not Pal contacts.

## Context Access List

```yaml
context_access_list:
  can_read:
    - "central contacts from AgentPal Workspace"
    - "thin project binding files"
    - "central project record paths relevant to content-ops-demo"
    - "referenced Org Pack recommendation if present"
    - "Capability Inventory Notion business-system profile if present"
    - "selected Pal loading-order slice after owner judgement"
  cannot_read:
    - "all Pal Packs"
    - "all Org Packs"
    - "all project files"
    - "private Notion workspace data"
    - "credentials, tokens, cookies, secrets"
    - "external project .agentpal/pals or .agentpal/workflows"
  need_output:
    - "candidate Pal asset list"
    - "task package recommendation"
    - "verification plan"
    - "not-run register"
```

## Task Package Recommendation

```yaml
task_package_recommendation:
  owner_pal: "to be selected by AI judgement after bounded reads"
  verifier_candidate: "Quinn if verification risk justifies it"
  runtime_role: "read/write only after a bounded task package and evidence"
  proposed_steps:
    - "Confirm whether the user wants workflow documentation, content calendar cleanup, or Notion page changes."
    - "Read current project binding and central project record."
    - "Read any Org Pack workflow recommendation referenced by the project record."
    - "Read Notion business-system profile or record access as unknown/not-run."
    - "Select owner Pal by AI judgement."
    - "Prepare a workflow organization task package."
    - "Require user confirmation before any external Notion write."
  allowed_writes:
    - "central project record task package, if user approved"
  forbidden_writes:
    - "external project .agentpal/pals/"
    - "external project .agentpal/workflows/"
    - "external project .agentpal/capability-inventory/"
    - "external project .agentpal/business-systems/"
    - "workspace/organization/contacts/pals.json"
    - "Notion external pages without explicit user authorization and runtime evidence"
```

## Verification Plan

```yaml
verification_plan:
  must_check:
    - "central roster was read from AgentPal Workspace"
    - "Org Pack recommendations were treated as input only"
    - "no keyword route was used"
    - "external project stayed thin-bound"
    - "No Notion API call happened unless explicitly authorized"
    - "No credential was stored"
    - "Task package recommendation separates Pal owner from Runtime execution"
  not_run:
    - "Notion availability check"
    - "external API call"
    - "project file modification"
  pass_condition:
    - "resolver produces candidate assets and a task package recommendation only"
```

## Forbidden Actions Confirmed

This example does not:

- copy Pal assets into `content-ops-demo/.agentpal/`
- copy Org Pack assets into `content-ops-demo/.agentpal/`
- create `.agentpal/capability-inventory/`
- create `.agentpal/business-systems/`
- create a Notion connector
- store Notion credentials
- route by keyword
- modify central contacts
- call an external API
- execute a workflow
