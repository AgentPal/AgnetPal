# Direct Pal Choice Explanation

## User Request

"Should I ask Mira or use `/pal Quinn` for this completion report?"

## When this Pal is a good candidate

Mira is a good candidate because the user asks for routing explanation and wants to choose the right entry shape.

## When this Pal should not take the whole task

If the user asks for the actual evidence review, Quinn should be the owner candidate for that verification work.

## Task Judgement

- domain_focus: entry choice and owner explanation.
- deliverables: short guidance for Mira-first versus direct specialist call.
- work_stages: classify intent, identify owner candidate, explain direct call semantics.
- capability_needs: routing explanation, contacts/registry awareness, boundary clarity.
- pal_candidates: Mira for explanation; Quinn for actual quality review candidate.
- runtime_candidates: none unless the report must be opened or checked.
- verification_needs: confirm the user understands consult versus handoff.

## Context Needs

Need only the user's goal and whether they want explanation, consult, or actual review. No project files are needed until review begins.

## Suggested Task Package

- Goal: help the user choose entry path.
- Steps: state default Mira-first path, state direct call path, give one example command, name when evidence is required.
- Output: concise recommendation.

## Good Response Example

Mira says to ask Quinn directly if the goal is evidence review, and to ask Mira if the user wants help deciding owner or summarizing a multi-stage result.

## Bad Response Example

Mira claims only Mira can reach Quinn, or turns the question into a fixed routing rule for all completion reports.

## Verification / Acceptance Criteria

- The answer preserves direct `/pal Name` support.
- It avoids static task-to-Pal rules.
- It does not load files unless the user asks for review.

## Notes

- Candidates are not fixed routes.
- Current v0.2 does not auto-run Deep Conductor.
