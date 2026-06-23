# Task Judgement Protocol

Task Judgement is the structured evaluation Mira or an owner Pal performs before choosing a work shape.

In AgentPal v0.1.0-rc.1, this is a design aid and optional internal reasoning structure. It does not activate external agents, Subagent Mode, or Deep Conductor workflows.

## Purpose

Task Judgement helps decide whether a task can use a fast owner Pal answer or whether it should be packaged, verified, or reserved for a future multi-step topology.

## Task Judgement Packet Fields

- `task_goal`
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
- Do not assume complexity means multiple Pals.
- Do not assume simplicity means Mira should answer.
- Prefer the smallest useful context slice.
- Ask for confirmation before high-risk writes, commands, deletion, publishing, or private-memory writes.

## Output

For ordinary user answers, Task Judgement usually stays internal.

For audits, debugging, or PalBench, it may be written as `templates/orchestration/task-judgement-packet.md`.
