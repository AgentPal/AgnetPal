# Start Here: AgentPal v0.5

If you just cloned AgentPal, start here.

AgentPal is a no-code AI organization framework. It is used with existing Agent
runtimes such as Codex, Claude Code, OpenCode, OpenHands, or similar tools. It
helps those runtimes work with named Pals, reusable knowledge, task packages,
context rules, verification habits, and public-safe organization examples.

AgentPal is not a standalone app, CLI, connector, scanner, installer, daemon,
background service, marketplace, or automation runtime. It does not replace
Codex, Claude Code, OpenCode, OpenHands, or your current agent runtime. The
runtime still performs real file reads, edits, commands, tool calls, and any
publication action, and it must report evidence.

AgentPal 是挂载到 Codex / Claude Code / OpenCode 等 Agent Runtime 上使用的
no-code AI 团队组织框架。它不是桌面 App、CLI 工具、后台服务、连接器、扫描器或自动执行平台。

The v0.5 local release preflight has passed. Remote publication still requires
explicit user authorization. No GitHub Release has been created by the local
preflight rounds.

## Choose Your Path

### 1. Five minutes: understand the shape

Read these in order:

1. [README](README.md)
2. [What is AgentPal?](docs/00-overview/what-is-agentpal.md)
3. [Final local release status](release/current/v0.5-final-local-release-status.md)

After five minutes, you should know that AgentPal is a Markdown / JSON /
protocol workspace, not an app. You should also know that Mira is the normal
entry Pal, PalSmith helps create and review Pal assets, and Faye is the delivery
owner pattern for turning a business goal into a Delivery Pack.

### 2. Thirty minutes: walk through first use

Read:

1. [First 30 Minutes with AgentPal](docs/01-getting-started/first-30-minutes.md)
2. [First AgentPal Team Walkthrough](examples/walkthroughs/first-agentpal-team/README.md)
3. [Fresh-clone usability checklist](release/current/v0.5-fresh-clone-usability-checklist.md)

This path does not require a real customer project, real CRM, real GitHub token,
or real private data. It uses a fake project placeholder and public-safe example
packs.

### 3. Create an AI team or Delivery Pack

Start with:

1. [Faye, Delivery Packs, and Deep Conductor overview](docs/00-overview/faye-delivery-pack-deep-conductor-overview.md)
2. [Org Pack / FDE / Asset Boundary overview](docs/00-overview/org-pack-fde-asset-boundary-overview.md)
3. [Org + FDE combined pack usage scenario](docs/04-usage-scenarios/org-fde-combined-pack-usage-scenario.md)
4. [Video Growth Delivery Pack example](examples/delivery-packs/video-growth-delivery-pack/README.md)
5. [Sales CRM Delivery Pack example](examples/delivery-packs/sales-crm-delivery-pack/README.md)

Use these as reference assets. They are not programs. They do not connect to a
CRM, publish content, scan systems, or route work by keyword.

## The Main Ideas

### Pal

A Pal is a working companion for an agent runtime. It has identity, knowledge,
skills, memory rules, workflows, context rules, output contracts, and
verification habits. A Pal is more than one skill, but it is not a separate
agent runtime.

### Mira

Mira is the default Main Pal, Leader Pal, and Conductor. Ordinary work starts
with Mira. Mira judges whether to answer, ask a focused question, prepare a
Task Package, or hand off to another registered Pal.

### PalSmith

PalSmith is the no-code Pal asset governance Pal. PalSmith helps create,
inspect, improve, version, and prepare Pal assets and Pal team blueprints. In
v0.5, PalSmith remains the only official Pal with an asset manifest pilot.

### Faye

Faye is the AI Delivery Pal pattern. Faye turns a business goal into a Delivery
Pack, Pal Team Blueprint, Faye Build Request, first Task Packages, acceptance
notes, and training notes. Faye is not an executor, connector, or publishing
tool.

### Org Pack, FDE Pack, and Delivery Pack

An Org Pack describes reusable organization structure. An FDE Pack describes
reusable expert delivery method. A Delivery Pack describes how one business goal
should be delivered. These packs are public-safe no-code assets, not apps.

### Thin Binding

External projects stay thin-bound. The allowed project-local binding surface is
small: `.agentpal/project.json`, `.agentpal/AGENTPAL.md`, protected root
instruction blocks such as `AGENTS.md` or `CLAUDE.md`, optional
`.claude/settings.local.json`, and `.gitignore` entries.

AgentPal does not default-copy Pals, memory, reports, Org Packs, FDE Packs,
Delivery Packs, workflows, governance records, or capability inventory into an
external project's `.agentpal/` directory.

### Central Project Record

Project memory, source maps, derived knowledge, task records, verification
reports, governance notes, and capability inventory belong in the AgentPal
Workspace under `workspace/projects/<project-id>/` by default. In this
onboarding walkthrough, that path is a placeholder and does not create a real
private project record.

## Safe First Prompt

Open AgentPal in your runtime and say:

```text
Mira, explain this AgentPal workspace for a new user. Keep it practical:
what should I read first, what is safe to try, and what should I avoid?
```

Then try:

```text
Mira, walk me through examples/walkthroughs/first-agentpal-team/ using a fake
project only. Do not use real customer data or create real external project
records.
```

## What A Good First Session Looks Like

A good first session is small. You are not trying to activate every Pal, read
every standard, or create a real delivery system. You are trying to prove that
you understand the shape of the workspace.

In a good first session:

1. The runtime opens the AgentPal repository itself.
2. Mira explains the visible entry points.
3. You inspect one public-safe example.
4. You ask for a fake Context Packet.
5. You ask for a fake Task Package.
6. You ask what evidence would be needed before calling the task complete.
7. You stop before adding private data or publishing anything.

The useful result is not a finished business deployment. The useful result is a
clear mental model: AgentPal gives your runtime a Pal organization layer, and
your runtime remains responsible for real execution.

## How To Use AgentPal With A Real Project Later

When you are ready to connect AgentPal to a real external project, use thin
binding. Thin binding means the project receives a small local pointer back to
AgentPal, not a copy of all AgentPal assets.

The external project remains the active project. AgentPal remains the Pal
workspace. Keep that separation clear:

- project source files stay in the external project;
- AgentPal Pal assets stay in the AgentPal Workspace;
- private project memory normally belongs under the matching central project
  record in `workspace/projects/<project-id>/`;
- reusable public examples stay free of private facts.

This matters because it prevents a reusable pack from quietly becoming a
private customer archive. It also prevents project `.agentpal/` folders from
turning into a second copy of the AgentPal workspace.

## How To Read The Examples

Read examples as patterns, not as installed products.

The combined pack example shows how reusable organization assets and expert
delivery assets can reference each other. The Delivery Pack examples show what
a concrete delivery package can look like for a fictional business goal. The
Deep Conductor examples show no-code governance records and task packaging
shapes.

None of those examples prove that the runtime has executed work. If a runtime
actually reads files, edits files, calls tools, or prepares publication, it must
return evidence. If no evidence exists, keep the state as `missing`, `not-run`,
or `needs-more-evidence`.

## Where To Go After The Walkthrough

After the walkthrough, choose one next step:

- If you only want to understand the framework, read the FAQ and glossary.
- If you want to bind a real project, read the project-binding templates and
  runtime guide for your host tool.
- If you want to create a Pal or AI team, start with PalSmith and the Pal Pack
  templates.
- If you want to shape a business delivery workflow, start with the Faye
  overview and Delivery Pack examples.
- If you want to publish v0.5 remotely, stop and run a separate authorization
  round with the exact push target, tag, release title, release notes, and
  commands.

## What Not To Do First

Do not start by reading every file. Use the index and the walkthrough.

Do not paste secrets, tokens, customer data, private screenshots, invoices,
contracts, CRM exports, payroll data, or production logs into reusable examples.

Do not treat recommended Pals as a route map. Recommended Pals are AI judgement
inputs only.

Do not publish, tag, push, or create a GitHub Release unless a separate round
has explicit user authorization for the exact target, tag, release title,
release notes, and commands.
