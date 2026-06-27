# Release Readiness Evidence Gate

## User Request

"Review whether this release is ready based on the checklist, changed files, and test evidence."

## When this Pal is a good candidate

Quinn is a good candidate because the task is a quality gate: evidence, risks, missing checks, and acceptance status.

## When this Pal should not take the whole task

Quinn should not publish the release or edit release docs as the owner. Repairs need owner candidates and Runtime evidence.

## Task Judgement

- domain_focus: release quality gate.
- deliverables: findings, pass/block status, residual risk, required repairs.
- work_stages: read checklist, map evidence, classify risks, decide readiness.
- capability_needs: release gate review, risk severity, not-run handling.
- pal_candidates: Quinn for quality gate; Atlas or Morgan candidates for repair packages depending on the gap.
- runtime_candidates: file-reading Runtime for checklists and command outputs.
- verification_needs: checklist item evidence, command outputs, unresolved gaps.

## Context Needs

Need release criteria, changed-file list, test/check output, known skipped checks, and release boundary. Do not inspect unrelated project history by default.

## Suggested Task Package

- Goal: determine readiness without overclaiming.
- Output: findings first, evidence table, blockers, warnings, not-run items, final status.
- Evidence required: current outputs or explicit not-run labels.

## Good Response Example

Quinn leads with blockers, explains evidence strength, and refuses to mark readiness when required checks are missing.

## Bad Response Example

Quinn says "ready" because the summary sounds complete, or hides unresolved checks under "minor follow-up".

## Verification / Acceptance Criteria

- Findings are ordered by severity.
- Required checks have evidence or `not-run`.
- The final status matches the evidence.

## Notes

- Candidates are not fixed routes.
- Current v0.2 does not auto-run Deep Conductor.
