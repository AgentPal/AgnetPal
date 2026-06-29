# PalSmith

PalSmith is the AgentPal Pal for designing, reviewing, and improving Pals and Pal Teams.

In v0.5, PalSmith is a no-code Pal asset governor. It can help a user turn goals, source material, or repeated work into Pal Pack drafts, Task Packages, health checks, and repair plans. It does not become an installer, scanner, validator program, connector, marketplace, app runtime, or automatic execution system.

## What PalSmith Helps With

- design a single new Pal
- design a small Pal Team for a business goal
- classify source material into identity, knowledge, Skill, workflow, runbook, example, eval, memory candidate, or report
- prepare a bounded Runtime Task Package for approved file creation
- review a Pal Pack for completeness, privacy, and job fitness
- prepare repair steps when a draft is shallow, unsafe, or incomplete
- distinguish Pal-owned Skills from host runtime Skills

## What PalSmith Must Not Do

- mutate central contacts without a separate approved governance task
- register a draft as an official Pal automatically
- copy Pal assets into an external project's `.agentpal/` directory by default
- treat tools, models, plugins, MCP servers, raw repos, knowledge packs, or Skills as Pals
- claim local file writes without runtime evidence
- expose private user material in public examples or Pal Packs
- create fixed keyword routing rules

## Good First Prompt

```text
/pal PalSmith Help me design a Pal for customer onboarding QA.
Keep it as a draft, identify missing information, and do not modify central contacts.
```

For a team:

```text
/pal PalSmith Design a small Pal Team for a sales operations workflow.
Separate candidate Pals, required Skills, runtime capability candidates, privacy risks, and the first Task Package.
```

## Relationship With Faye

Faye shapes business delivery packages: scenarios, workflows, data lists, interface lists, risks, missing information, and Task Package readiness.

PalSmith can then turn a Faye Build Request into a Pal or Pal Team design. Quinn can review the plan and evidence before acceptance.

## Next Links

- [PalSmith end-to-end productization](palsmith-end-to-end-productization.md)
- [PalSmith v0.5 creation and upgrade](../03-user-guides/palsmith-v0.5-pal-creation-and-upgrade.md)
- [Create your first Pal](../02-getting-started/06-create-your-first-pal-in-5-minutes.md)
- [Official Pals](../99-reference/official-pals.md)
