# Competitor Technical Route Comparison

## User Request

"Compare three products' technical approaches and tell me which claims are well-supported."

## When this Pal is a good candidate

Vega is a good candidate because the task needs source quality assessment, comparison, and uncertainty flags.

## When this Pal should not take the whole task

Vega should not decide product roadmap priority alone or implement a chosen technical route. Those later stages need their own owner candidates.

## Task Judgement

- domain_focus: comparative research.
- deliverables: comparison matrix, evidence quality notes, uncertainty flags.
- work_stages: define comparison criteria, gather sources, score evidence, synthesize.
- capability_needs: source credibility, technical comparison, claim alignment.
- pal_candidates: Vega for research; Nova candidate for product decision follow-up; Atlas candidate for implementation-package follow-up.
- runtime_candidates: browser/search Runtime if external sources are needed.
- verification_needs: source list, claim mapping, stale/weak evidence labels.

## Context Needs

Need product names, comparison criteria, allowed sources, recency needs, and desired output depth. Avoid unsupported claims.

## Suggested Task Package

- Goal: compare routes with evidence quality.
- Output: matrix, source notes, confidence level, open questions.
- Do not do: present weak claims as facts.

## Good Response Example

Vega states which claims are source-backed, which are inferred, and which need follow-up research before product or development choices.

## Bad Response Example

Vega chooses a winner based on marketing language alone or collapses research into an implementation plan.

## Verification / Acceptance Criteria

- Every major claim links to evidence.
- Weak evidence is labeled.
- Follow-up owner candidates are stage-specific.

## Notes

- Candidates are not fixed routes.
- Current v0.2 does not auto-run Deep Conductor.
