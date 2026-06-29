# Multi-Pal Collaboration Prompt Cards

These prompt cards show copyable ways to use Mira, `/pal Name`, and `@Pal` in v0.5 no-code collaboration.

`/pal` and `@Pal` are AgentPal plain-text protocols. They do not require native CLI command support.

## 1. Ask Mira To Split The Work

```text
Mira, help me split this release task into owner, reviewer, evidence, and next action.
```

Expected behavior: Mira performs staged judgement and names owner / reviewer candidates case by case.

Should not happen: Mira should not assume every release task has a fixed reviewer.

## 2. Direct Development Task Package

```text
/pal Atlas Turn this feature request into a Codex development task package.
```

Expected behavior: Atlas becomes current owner candidate, applies core gates, and produces a development task package or staged judgement.

Should not happen: `/pal Atlas` should not start a separate Agent.

## 3. Business Delivery Package

```text
/pal Faye Turn this sales follow-up idea into a business scenario, workflow, data list, interface list, risk list, and Task Package.
```

Expected behavior: Faye shapes delivery readiness without claiming connector, executor, app runtime, auto-sync, or customer-system execution.

Should not happen: Faye should not claim access to a CRM or write customer data into public examples.

## 4. Completion Report Review

```text
/pal Quinn Review whether this completion report proves the work is actually done.
```

Expected behavior: Quinn maps claims to evidence and marks missing, partial, blocked, or not-run honestly.

Should not happen: Quinn should not pass a report without evidence.

## 5. Acceptance Consult

```text
Mira, I am preparing a release. @Quinn review the acceptance risks from the evidence summary only.
```

Expected behavior: Mira or the current owner creates a bounded review packet for Quinn.

Should not happen: Quinn should not receive full chat history or become owner automatically.

## 6. Evidence Consult

```text
Atlas, before writing the task package, @Vega check what source evidence is missing.
```

Expected behavior: Atlas sends Vega a bounded consult packet and keeps owner responsibility.

Should not happen: Vega should not receive unrelated implementation files.

## 7. Pal Team Design

```text
/pal PalSmith Use this FAYE_BUILD_REQUEST to design a candidate Pal Team.
Do not modify central contacts.
```

Expected behavior: PalSmith designs candidate Pals, collaboration rules, runtime capability candidates, privacy boundaries, and a first Task Package.

Should not happen: PalSmith should not register official Pals automatically.

## 8. Mira Summarizes Final Reports

```text
Mira, summarize Faye, PalSmith, and Quinn final reports and tell me the unresolved risk.
```

Expected behavior: Mira summarizes accepted final reports, separates agreement, conflict, evidence gaps, and next action.

Should not happen: Mira should not invent specialist conclusions that are absent from the reports.

## Boundary

Deep Conductor can help decide stages, owners, capability candidates, and verification needs. It does not automatically start subagents, background workflows, external Agents, or tool execution.
