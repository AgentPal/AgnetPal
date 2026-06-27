# Multi-Pal Collaboration Prompt Cards

These prompt cards show copyable ways to use Mira, `/pal Name`, and `@Pal` in v0.3 no-code collaboration.

`/pal` and `@Pal` are AgentPal plain-text protocols. They do not require native CLI command support.

## 1. Ask Mira To Split The Work

User input:

```text
Mira, help me split this release task into owner, reviewer, evidence, and next action.
```

Expected behavior: Mira performs staged judgement and names owner / reviewer candidates case by case.

Context Packet type: none first, or `review` / `delegate` if another Pal is needed.

Should not happen: Mira should not assume every release task has a fixed reviewer.

## 2. `/pal Atlas` Development Task Package

User input:

```text
/pal Atlas Turn this feature request into a Codex development task package.
```

Expected behavior: Atlas becomes current owner candidate, applies core gates, and produces a development task package or staged judgement.

Context Packet type: `direct_owner`.

Should not happen: Mira should not silently take back the task, and `/pal` should not start a separate Agent.

## 3. `/pal Vega` Research Judgement

User input:

```text
/pal Vega Judge what evidence we need before making this roadmap claim public.
```

Expected behavior: Vega becomes current owner candidate for research judgement and states source / uncertainty needs.

Context Packet type: `direct_owner`.

Should not happen: Vega should not claim current facts without evidence.

## 4. `/pal Quinn` Completion Report Review

User input:

```text
/pal Quinn Review whether this completion report proves the work is actually done.
```

Expected behavior: Quinn becomes current owner candidate for verification and maps claims to evidence.

Context Packet type: `direct_owner` or `review` if another owner sends it.

Should not happen: Quinn should not pass a report without evidence.

## 5. `@Quinn` Acceptance Consult

User input:

```text
Mira, I am preparing a release. @Quinn review the acceptance risks from the evidence summary only.
```

Expected behavior: Mira or the current owner creates a `review` Context Packet for Quinn.

Context Packet type: `review`.

Should not happen: Quinn should not receive full chat history or become owner automatically.

## 6. `@Vega` Evidence Consult

User input:

```text
Atlas, before writing the task package, @Vega check what source evidence is missing.
```

Expected behavior: Atlas sends Vega a bounded consult packet and keeps owner responsibility.

Context Packet type: `consult`.

Should not happen: Vega should not receive unrelated implementation files.

## 7. Owner Sends Packet To Reviewer

User input:

```text
Atlas, generate a Context Packet for Quinn to review this implementation plan.
```

Expected behavior: Atlas prepares `from_pal: Atlas`, `to_pal_candidate: Quinn`, and `mode: review`.

Context Packet type: `review`.

Should not happen: the packet should not include Atlas draft notes that are irrelevant to verification.

## 8. Mira Summarizes Final Reports

User input:

```text
Mira, summarize Atlas and Quinn final reports and tell me the unresolved risk.
```

Expected behavior: Mira summarizes accepted final reports, separates agreement, conflict, evidence gaps, and next action.

Context Packet type: summary stage reading final reports only.

Should not happen: Mira should not invent specialist conclusions that are absent from the reports.

## 9. Upgrade Consult To Handoff

User input:

```text
Mira, based on Quinn's review, hand the release verification task to Quinn.
```

Expected behavior: Mira creates a handoff or owner_transfer packet and Quinn accepts only after core gates.

Context Packet type: `handoff` or `owner_transfer`.

Should not happen: the earlier `@Quinn` consult should not be retroactively treated as ownership transfer without this explicit instruction.

## 10. User Overrides A Pal Suggestion

User input:

```text
Mira, I understand Atlas suggested Quinn, but keep Atlas as owner and ask Quinn only for review.
```

Expected behavior: Mira honors the user override unless it conflicts with safety or impossible scope.

Context Packet type: `review`.

Should not happen: the override should not become a permanent rule for future tasks.
