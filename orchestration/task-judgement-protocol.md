# Task Judgement Protocol

Task Judgement is the structured evaluation the current Main Pal or owner Pal performs before choosing a work shape.

In AgentPal v0.1.0-rc.1, this is a design aid and optional internal reasoning structure. It does not activate external agents, Subagent Mode, or Deep Conductor workflows.

## Purpose

Task Judgement helps decide whether a task can use a fast owner Pal answer or whether it should be staged, packaged, verified, or reserved for a future multi-step topology.

Deliverable-aware Task Judgement is an AgentPal system-level capability. It is not Mira-only. Mira is the default Main Pal, Leader Pal, and Conductor, but any directly called Pal or current owner Pal must perform deliverable-aware judgement before accepting a complex task as a single-owner task.

The current Main Pal or owner Pal must identify:

- `domain_focus`: the subject or knowledge domain of the request
- `content_deliverables`: reports, briefs, drafts, specifications, plans, or other content outputs
- `final_deliverables`: the user-visible final artifact or outcome
- `work_stages`: the meaningful stages required to reach the final deliverable
- `capability_needs`: the capability each stage requires
- `verification_needs`: the evidence or review needed before a completion claim

Topic domain is not the same as final deliverable. A research topic may still require an implementation-stage deliverable. A development request may still require research, product, writing, document, system, or quality stages.

Content-stage owner does not equal whole-task owner. If a task contains multiple obvious deliverables or stages, the current Main Pal / owner Pal should not compress the whole task into one Pal handoff. It should produce staged candidates or a staged Task Package.

## Task Judgement Packet Fields

- `task_goal`
- `domain_focus`
- `deliverables`
  - `content_deliverables`
  - `final_deliverables`
- `work_stages`
  - `stage_id`
  - `stage_goal`
  - `capability_needs`
  - `pal_candidates`
  - `runtime_candidates`
  - `skill_candidates`
  - `verification_needs`
- `overall_conductor`
- `task_type_candidates`
- `complexity`
- `risk_level`
- `needs_file_read`
- `needs_file_write`
- `needs_command`
- `needs_external_knowledge`
- `needs_skill`
- `needs_plugin`
- `needs_verification`
- `preferred_latency`
- `budget_sensitivity`
- `context_scope`
- `recommended_mode`
- `candidate_owner_pals`
- `candidate_capabilities`
- `decision_basis`
- `hardcoded_routing_policy`
- `context_access_list_needed`
- `evidence_required`
- `open_questions`

## Allowed Recommended Modes

`recommended_mode` is a candidate judgement input, not a hard rule.

- `fast_route`
- `single_owner`
- `owner_plus_verifier`
- `plan_execute_verify`
- `parallel_independent_review`
- `sequential_chain`
- `best_of_n_runtime`

## v0.1 Active Modes

Active in v0.1.0-rc.1:

- `fast_route`
- `single_owner`
- compact `task_package`
- staged `task_package`

Future design only:

- `owner_plus_verifier` as a separate workflow
- `plan_execute_verify` as an automated workflow
- `parallel_independent_review`
- `sequential_chain`
- `best_of_n_runtime`

## Judgement Principles

- Use current contacts / registry for Pal availability.
- Use capability profiles only as non-binding candidates.
- Do not route by keyword.
- Do not use task/domain -> fixed Pal maps.
- Do not turn capability examples into routes.
- Express Pal, Runtime, and Skill options as candidates, not fixed routes.
- The current Main Pal / owner Pal must consider the requested final deliverable, not only the topic domain.
- Any current owner Pal must perform deliverable-aware task judgement before accepting a complex task as a single-owner task.
- Do not assume complexity means multiple Pals.
- Do not assume simplicity means Mira should answer.
- Do not assume a directly called specialist owns every stage of a composite task.
- Direct `/pal Name` calls select the current speaking Pal; they do not remove that Pal's duty to identify stages outside its own responsibility.
- Prefer the smallest useful context slice.
- Ask for confirmation before high-risk writes, commands, deletion, publishing, or private-memory writes.

## Owner Pal Duty

Before accepting a complex task as a single-owner task, any current owner Pal must judge:

- whether the task is single-stage or multi-stage
- whether it contains multiple obvious deliverables
- which stages the current Pal is suited to own
- which stages need other Pal / Runtime / Skill candidates
- whether Mira should remain or resume the upper-level Conductor role
- whether a verification stage is needed
- whether the correct v0.1 output is a staged Task Package

If the task contains an implementation-stage deliverable, the owner Pal must not say that the Runtime will simply handle that stage after a content Pal finishes. The implementation stage needs Pal-layer judgement or a Task Package first; the current Runtime may execute only with evidence and within its permissions.

## Hardcoded Routing Boundary

Allowed:

- "candidate content-stage owner"
- "candidate implementation-stage owner"
- "candidate verifier"
- "candidate Runtime / Skill"
- case-specific reasoning from user goal, deliverables, available Pals, available runtime, context, and risk

Forbidden as current rules:

- keyword trigger
- fixed route
- task/domain -> Pal table
- "must route"
- "always handoff"
- statements that a particular artifact type always belongs to a particular Pal

Negative examples may mention forbidden route shapes only to prevent regressions.

## Output

For ordinary user answers, Task Judgement usually stays internal.

For audits, debugging, or PalBench, it may be written as `templates/orchestration/task-judgement-packet.md`.
