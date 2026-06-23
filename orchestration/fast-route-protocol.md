# Fast Route Protocol

Fast Route is the default scheduling shape for clear AgentPal v0.1 work.

It keeps the path short: Mira receives the user goal, checks contacts / registry, chooses one suitable owner Pal by AI judgement, gives a short handoff, and the owner Pal answers in Simple Pal Mode.

Fast Route is not a hard-coded semantic route table. It is a lightweight decision pattern.

## When To Use

Use Fast Route when:

- one registered Pal can own the requested work product
- the task can be handled from the current context plus a small owner-Pal asset slice
- no independent review is needed before the first useful answer
- no external Agent runtime orchestration is required
- the user has not asked for a deeper workflow plan

## Mira Responsibilities

Mira handles:

- user goal intake
- current project / workspace boundary check
- contacts and registry lookup
- case-by-case owner judgement
- optional Capability Inventory consultation when needed
- minimal Context Packet or Context Access List preparation
- short handoff to the owner Pal
- later summary or routing explanation when the user asks

Mira does not write the owner Pal's professional body after handoff.

## Owner Pal Responsibilities

The owner Pal handles:

- its own Level 0 identity assets
- relevant Level 1 indexes
- one to three task-relevant assets when needed
- its own Output Contract
- honest fallback if a relevant asset is missing
- evidence and execution-layer reporting when real tools or files were involved

## Fast Route Output Shape

```text
Mira：我判断这次更适合由 <Owner Pal> 接手，因为 <short case-specific reason>。我交给 <Owner Pal>。

<Owner Pal>：我接手。<owner answer using its contract>
```

## v0.1 Boundary

Fast Route is the current active path through Simple Pal Mode. It does not activate Subagent Mode, parallel child workflows, external Agent calls, or Deep Conductor execution.

