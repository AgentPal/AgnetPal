# First 30 Minutes with AgentPal

This guide is for a fresh clone. It uses public-safe examples only. You do not
need to install an app, call an API, connect a CRM, create a GitHub token, or
use real customer data.

## 0. What You Need

- A local clone of AgentPal.
- An agent runtime that can read Markdown / JSON files, such as Codex, Claude
  Code, OpenCode, OpenHands, or a similar tool.
- A fake project name, for example `demo-content-team`.

## 1. Open AgentPal In Your Agent Runtime

Open the AgentPal directory as its own workspace. Do not open an unrelated user
project and call it AgentPal.

## 2. Read START_HERE

Read [START_HERE](../../START_HERE.md). It gives the shortest map for what to
read, what to try, and what to avoid.

## 3. Meet Mira, PalSmith, And Faye

Read [What is AgentPal?](../00-overview/what-is-agentpal.md).

Use this prompt:

```text
Mira, explain Mira, PalSmith, and Faye for a first-time AgentPal user.
Keep it practical and do not treat recommended Pals as fixed routes.
```

## 4. Inspect The Combined Pack Example

Open:

```text
examples/combined-packs/content-ops-with-accounting-advisor/README.md
```

This example shows how reusable Org Pack and FDE Pack assets can be combined
without storing customer-private data in a reusable pack.

## 5. Inspect The Video Growth Delivery Pack

Open:

```text
examples/delivery-packs/video-growth-delivery-pack/README.md
```

Notice the shape: project, flows, task packages, Pal team blueprint, Faye Build
Request, acceptance notes, and training notes.

## 6. Understand Project Thin Binding

Read:

```text
templates/project-binding/README.md
docs/01-getting-started/bind-external-project.md
```

Allowed project-local binding files are limited to small pointer files and
protected instruction blocks. AgentPal does not default-copy `.agentpal/pals/`,
`.agentpal/memory/`, `.agentpal/reports/`, `.agentpal/org-pack/`,
`.agentpal/fde-pack/`, `.agentpal/delivery-pack/`, or
`.agentpal/capability-inventory/`.

## 7. Prepare A Fake External Project

Use a placeholder only:

```text
workspace/projects/demo-content-team/
```

Do not create a real private project record during this walkthrough. Do not
paste real customer files, private screenshots, CRM exports, tokens, passwords,
API keys, cookies, or secrets.

## 8. Ask Mira To Explain The Pack

Use:

```text
Mira, explain examples/combined-packs/content-ops-with-accounting-advisor/
for a fake project. Identify reusable assets, private boundaries, and what a
new user should read next.
```

## 9. Ask Faye To Draft A Delivery Pack

Use:

```text
Mira, for a fake project called demo-content-team, judge whether Faye should
draft a public-safe Delivery Pack outline. Do not use real customer data and do
not create a real external project binding.
```

Faye is a delivery-owner pattern. Faye may draft a Delivery Pack structure, but
does not execute work, connect systems, or publish anything.

## 10. Ask PalSmith To Review The Pal Team Blueprint

Use:

```text
Mira, ask PalSmith to review the fake Pal Team Blueprint as no-code asset
governance. Keep recommended Pals as AI judgement inputs only.
```

PalSmith can review asset fitness and missing fields. PalSmith must not mutate
central contacts, official Pal files, or external project `.agentpal/` folders
without a separate approved task.

## 11. Where Outputs Should Go

For public reusable walkthrough notes, use the example walkthrough folder.

For a real private project, approved private records belong under:

```text
workspace/projects/<project-id>/
```

Do not store private facts in reusable examples.

## 12. What Not To Do

- Do not read the whole repository as default context.
- Do not create real external project `.agentpal/delivery-pack/` folders.
- Do not paste credentials or customer-private data.
- Do not treat recommended Pals as fixed routing.
- Do not claim v0.5 is remotely published.
- Do not push, tag, or create a GitHub Release without explicit authorization.
