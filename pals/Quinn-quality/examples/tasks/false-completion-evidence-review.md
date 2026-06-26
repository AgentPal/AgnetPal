# False Completion Evidence Review

## User Request

```text
/pal Quinn Review this completion report and tell me whether the work is actually proven complete.
```

## When this Pal is a good candidate

Quinn is a good candidate because the requested output is acceptance and evidence review, especially where false completion is possible.

## When this Pal should not take the whole task

Quinn should not perform the original implementation or research. Quinn reviews evidence and can request a repair package from the relevant owner candidate.

## Task Judgement

- domain_focus: evidence-based quality review.
- deliverables: findings, evidence status, missing proof, acceptance judgement.
- work_stages: map requirements, inspect evidence, classify gaps, report status.
- capability_needs: acceptance criteria, false-completion detection, not-run handling.
- pal_candidates: Quinn for verification; Atlas, Vega, or other owner candidates for repairs depending on missing evidence.
- runtime_candidates: shell/file-reading Runtime if evidence files or command outputs must be inspected.
- verification_needs: requirement-by-requirement evidence table.

## Context Needs

- stated requirements;
- affected paths;
- command outputs;
- test coverage;
- known not-run checks;
- risk boundary.

## Suggested Task Package

- Goal: determine whether completion is proven.
- Input: requirements, changed files, command outputs, claimed checks.
- Output: pass/fail/blocked/not-run status with evidence.
- Do not do: infer completion from confidence language.

## Good Response Example

Quinn checks each requirement against current evidence, marks missing evidence as not complete, and reports `not-run` explicitly.

## Bad Response Example

Quinn accepts a summary as proof, treats search results as full verification, or smooths missing checks into a pass.

## Verification / Acceptance Criteria

- every requirement has evidence status;
- missing, weak, contradictory, and not-run evidence are separated;
- final status does not overclaim completion.

## Notes

- Candidates are not fixed routes.
- Current v0.2 does not auto-run Deep Conductor.
