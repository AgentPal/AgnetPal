# No-Code AgentPal Review

## User Request

"Review this AgentPal change and confirm it did not add runtime code or a hidden service."

## When this Pal is a good candidate

Rhea is a good candidate because the task concerns no-code boundary, runtime dependencies, installers, services, and system-impact risk.

## When this Pal should not take the whole task

Rhea should not judge product value or write the docs herself. Rhea reviews system/runtime boundary evidence.

## Task Judgement

- domain_focus: no-code boundary review.
- deliverables: boundary findings, changed-file classification, risk status.
- work_stages: inspect changed files, classify extensions, scan risky terms, report evidence.
- capability_needs: system safety, no-code policy, evidence review.
- pal_candidates: Rhea for boundary review; Quinn candidate for release quality gate if needed.
- runtime_candidates: shell/file-list Runtime for evidence.
- verification_needs: changed files, extension scan, risky artifact scan, not-run labels.

## Context Needs

Need changed-file list, diff summary, and no-code boundary policy. Do not scan private external directories.

## Suggested Task Package

- Goal: verify no runtime layer was introduced.
- Checks: changed-file extensions, dependency manifests, installer/service terms, hidden execution claims.
- Output: pass/block/not-run with evidence.

## Good Response Example

Rhea reports the exact changed files and says whether any new code, dependency manifest, UI, installer, or service artifact appeared.

## Bad Response Example

Rhea says "looks like docs" without checking changed files, or executes a risky operation while reviewing safety.

## Verification / Acceptance Criteria

- Changed-file evidence is listed.
- New runtime artifacts are absent or clearly flagged.
- Any unavailable check is labeled `not-run`.

## Notes

- Candidates are not fixed routes.
- Current v0.2 does not auto-run Deep Conductor.
