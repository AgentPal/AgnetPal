# Completion Report Summary

## User Request

"Codex says it finished. Summarize what happened and tell me what still needs attention."

## When this Pal is a good candidate

Mira is a good candidate for user-facing result synthesis when Runtime evidence has already been produced and the user wants a readable status closeout.

## When this Pal should not take the whole task

If the task requires independent quality judgement, Quinn should be a verifier candidate. If it requires source review or code planning, other specialist candidates may be needed.

## Task Judgement

- domain_focus: result summarization.
- deliverables: completion summary, evidence summary, gaps, next steps.
- work_stages: collect evidence, separate done/not-run/missing, produce closeout.
- capability_needs: evidence-aware reporting, concise synthesis.
- pal_candidates: Mira for summary, Quinn for verification candidate when risk is meaningful.
- runtime_candidates: current Runtime output as evidence source.
- verification_needs: do not mark unverified items as done.

## Context Needs

Use only the current Runtime result, changed-file list, test output, and user acceptance target. Do not infer hidden execution.

## Suggested Task Package

- Goal: summarize execution honestly.
- Evidence fields: files changed, checks run, checks not run, blockers, commit hash if available.
- Output: short final status and next recommended check.

## Good Response Example

Mira reports what changed, names the checks that actually ran, labels unrun checks as `not-run`, and keeps next actions concrete.

## Bad Response Example

Mira says "all verified" because the plan looked reasonable, or hides a failed/no-run check in friendly wording.

## Verification / Acceptance Criteria

- The report distinguishes completed, not-run, missing, and blocked.
- Execution claims cite current Runtime evidence.
- Specialist review is suggested only when needed by risk.

## Notes

- Candidates are not fixed routes.
- Current v0.2 does not auto-run Deep Conductor.
