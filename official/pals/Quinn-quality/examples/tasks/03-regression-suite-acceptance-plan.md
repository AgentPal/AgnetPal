# Regression Suite Acceptance Plan

## User Request

"Create acceptance criteria for a lightweight regression suite and tell me how to know it passed."

## When this Pal is a good candidate

Quinn is a good candidate because the deliverable is a quality plan with failure modes, acceptance evidence, and pass/fail reporting.

## When this Pal should not take the whole task

Quinn should not implement the tests or write feature docs unless separately scoped through the appropriate owner candidates.

## Task Judgement

- domain_focus: regression acceptance design.
- deliverables: acceptance criteria, evidence table, failure conditions.
- work_stages: identify risks, define cases, define evidence, define report format.
- capability_needs: test strategy, quality gates, evidence review.
- pal_candidates: Quinn for acceptance plan; Atlas candidate for implementation package if files or commands are needed.
- runtime_candidates: none for plan; command-capable Runtime if executing checks later.
- verification_needs: each case has expected input, expected behavior, and evidence.

## Context Needs

Need feature scope, risk areas, previous failures, available check methods, and reporting expectations.

## Suggested Task Package

- Goal: make regression pass/fail visible.
- Output: case list, acceptance criteria, evidence required, report format.
- Do not do: substitute broad confidence for concrete checks.

## Good Response Example

Quinn defines the suite with clear pass, fail, blocked, and not-run statuses for each case.

## Bad Response Example

Quinn writes vague "test everything" advice or says the suite passes without execution evidence.

## Verification / Acceptance Criteria

- Each case has an expected result.
- Evidence format is defined.
- The report can distinguish pass, fail, blocked, and not-run.

## Notes

- Candidates are not fixed routes.
- Current v0.2 does not auto-run Deep Conductor.
