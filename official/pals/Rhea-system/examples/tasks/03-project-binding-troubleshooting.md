# Project Binding Troubleshooting

## User Request

"AgentPal in my project seems to read the wrong root. Diagnose the binding without changing files yet."

## When this Pal is a good candidate

Rhea is a good candidate because the task involves runtime/project boundary, active project root, and safe diagnostic scope.

## When this Pal should not take the whole task

Rhea should not edit binding files unless the user approves a repair package. Mira may summarize user-facing project context after evidence exists.

## Task Judgement

- domain_focus: runtime adapter and project binding safety.
- deliverables: diagnosis, root-boundary findings, repair package if needed.
- work_stages: identify expected roots, inspect binding files, compare claims, prepare repair.
- capability_needs: runtime boundary, least-privilege diagnostics, evidence reporting.
- pal_candidates: Rhea for diagnosis; Mira candidate for user-facing summary; Atlas candidate for repair package if files need edits.
- runtime_candidates: read-only file Runtime for binding inspection.
- verification_needs: active project root, AgentPal workspace root, binding file contents, not-run labels.

## Context Needs

Need the project binding files, current working directory, and expected AgentPal workspace path from user-provided context. Avoid scanning unrelated projects.

## Suggested Task Package

- Goal: diagnose root confusion without writes.
- Reads: named binding files only.
- Output: expected root, observed root, mismatch, repair package.
- Writes: none unless separately approved.

## Good Response Example

Rhea reports the two root concepts separately and prepares a bounded repair package only if a mismatch is proven.

## Bad Response Example

Rhea edits binding files immediately or treats the AgentPal Workspace as the active user project.

## Verification / Acceptance Criteria

- Diagnosis is read-only.
- Active project root and AgentPal workspace root are separated.
- Repair requires a later confirmed package.

## Notes

- Candidates are not fixed routes.
- Current v0.2 does not auto-run Deep Conductor.
