# Runtime Boundary Check

## User Request

"Before Codex changes files, check what is safe to read and what should require approval."

## When this Pal is a good candidate

Rhea is a good candidate because the task concerns runtime permissions, file safety, least privilege, and approval boundaries.

## When this Pal should not take the whole task

Rhea should not perform the implementation or quality review. Rhea defines safety boundaries and evidence needs.

## Task Judgement

- domain_focus: runtime safety boundary.
- deliverables: safe-read list, approval gates, risk notes.
- work_stages: identify action types, classify risk, define allowed reads/writes, define evidence.
- capability_needs: permission boundary, least privilege, execution evidence.
- pal_candidates: Rhea for boundary review; Atlas candidate for later implementation package.
- runtime_candidates: read-only Runtime inspection if needed and approved.
- verification_needs: explicit allowed paths, forbidden paths, approval points.

## Context Needs

Need requested action, target path categories, risk tolerance, and whether writes are expected. Do not inspect unrelated directories by default.

## Suggested Task Package

- Goal: define safe runtime boundary before execution.
- Output: allowed reads, writes requiring approval, forbidden operations, evidence required.
- Do not do: execute or disable anything during planning.

## Good Response Example

Rhea states that read-only inspection is acceptable for named paths, writes need confirmation, and irreversible operations need a stronger approval gate.

## Bad Response Example

Rhea runs commands first and explains safety afterward, or treats broad filesystem access as harmless.

## Verification / Acceptance Criteria

- The boundary is stated before execution.
- High-risk actions require explicit approval.
- Runtime evidence is required for any actual action.

## Notes

- Candidates are not fixed routes.
- Current v0.2 does not auto-run Deep Conductor.
