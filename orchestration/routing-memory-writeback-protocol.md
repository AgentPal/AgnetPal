# Routing Memory Writeback Protocol

Routing Memory Writeback is the v0.3 no-code process for recording routing decisions and outcomes in a public-safe way.

It is not model training, not an automatic database, not a route map, and not a keyword dispatcher.

## Purpose

Record enough about routing and verification outcomes to improve future AI Judgement:

- what task type was handled;
- which owner candidate was chosen;
- which verifier or runtime candidate was used;
- what reasoning strength was selected;
- which Runtime-installed Skill candidates were considered or used;
- which Pal-owned Skills or methods shaped the package;
- how much context was read;
- whether verification passed;
- whether rework was needed.

## Record Types

Use two records:

- Routing Decision Record: written when a plan or workflow is chosen.
- Routing Result Record: written after evidence, user acceptance, or verifier judgement exists.

## Required Decision Fields

- `record_id`
- `created_at`
- `task_summary`
- `task_type`
- `topology_candidate`
- `owner_pal_candidate`
- `verifier_pal_candidate`
- `runtime_candidate`
- `model_or_reasoning_candidate`
- `runtime_skill_candidates`
- `runtime_skills_used`
- `pal_owned_skills_used`
- `context_index_known_count`
- `context_content_read_count`
- `decision_basis`
- `privacy_review`
- `not_a_fixed_route`

## Required Result Fields

- `record_id`
- `decision_record_id`
- `completed_at`
- `verification_result`
- `evidence_summary`
- `not_run_items`
- `false_completion_caught`
- `rework_count`
- `user_accepted`
- `failure_reason`
- `runtime_skills_used`
- `pal_owned_skills_used`
- `what_worked`
- `what_failed`
- `next_time_recommendation`
- `privacy_review`
- `not_a_fixed_route`

## Privacy Boundary

Do not record:

- private user content;
- private project facts;
- credentials, tokens, secrets, raw logs;
- full file content;
- local absolute paths;
- raw external Agent traces.

Use synthetic examples in public release files. Runtime-private or project-private records belong in ignored memory or the user's project-local state.

## Reuse Rule

Routing Memory may inform future candidates. It must never say a future task must use the same Pal, runtime, Skill, model, or topology.

Future judgement still depends on the current user goal, current contacts / registry, current runtime evidence, risk, context, and user constraints.

## Cross-Runtime Rule

When a task continues in a different host Runtime, Routing Memory may summarize previous owner, verifier, Runtime, model/reasoning, Skill, and verification outcomes. The current host Runtime must still prove current availability and permissions before using tools or Skills.

Runtime Skill usage results can be linked to `templates/memory/runtime-skill-usage-memory-record.md`. This records host Runtime experience only; it does not make the Skill a Pal-owned Skill and does not prove future availability.
