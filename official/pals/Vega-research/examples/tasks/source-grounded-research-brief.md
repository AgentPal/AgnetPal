# Source-Grounded Research Brief

## User Request

```text
/pal Vega Research whether a feature direction is supported by current user needs and summarize uncertainty.
```

## When this Pal is a good candidate

Vega is a good candidate because the output is research framing, source inventory, evidence matrix, synthesis, and uncertainty reporting.

## When this Pal should not take the whole task

Vega should not own a later implementation, product scope commitment, final marketing page, or release acceptance stage without staged judgement.

## Task Judgement

- domain_focus: source-grounded feature research.
- deliverables: research brief, evidence matrix, uncertainty notes.
- work_stages: frame question, define source rules, collect evidence, synthesize, hand off.
- capability_needs: source credibility, claim-evidence alignment, uncertainty reporting.
- pal_candidates: Vega for research candidate; Nova candidate for product scope if the user asks what to build.
- runtime_candidates: web/search Runtime only when freshness or external sources are required.
- verification_needs: sources read, dates, claims mapped to evidence.

## Context Needs

- research question;
- allowed sources;
- recency needs;
- user segment;
- source credibility criteria;
- output format.

## Suggested Task Package

- Goal: produce a source-grounded brief with uncertainty.
- Reads: approved sources or search results.
- Output: source inventory, evidence table, synthesis, gaps, recommendations.
- Evidence: links or local source identifiers and dates.

## Good Response Example

Vega separates facts, source-backed claims, inferences, uncertainty, and recommended next research. If browsing is required, the runtime evidence includes sources read.

## Bad Response Example

Vega gives confident recommendations without sources or hides stale evidence.

## Verification / Acceptance Criteria

- source inventory exists;
- claims map to evidence;
- uncertainty is explicit;
- no unsupported current-events claim is made.

## Notes

- Candidates are not fixed routes.
- Current v0.2 does not auto-run Deep Conductor.
