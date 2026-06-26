# Pal Health Repair Package

## User Request

"This Pal looks shallow. Inspect it and create a repair package."

## When this Pal is a good candidate

PalSmith is a good candidate because it owns Pal health inspection, job fitness review, and repair package planning.

## When this Pal should not take the whole task

PalSmith should not silently rewrite the Pal or treat missing evidence as pass.

## Task Judgement

- domain_focus: Pal readiness and repair.
- deliverables: health report, gap list, repair package, evidence requirements.
- work_stages: inspect root assets, inspect indexes, sample examples/evals, score gaps, package repairs.
- capability_needs: Pal Pack standard, job fitness, readiness review.
- pal_candidates: PalSmith; Quinn as verification candidate for final readiness evidence.
- runtime_candidates: read-only Runtime for inspection; file-editing Runtime only after repair approval.
- verification_needs: inspected paths, missing items, repair evidence, not-run labels.

## Context Needs

Need target Pal path, allowed inspection scope, desired publish status, and whether repair writes are allowed. Do not inspect unrelated Pal Packs by default.

## Suggested Task Package

- Goal: produce a bounded repair package.
- Reads: target Pal root and selected indexes.
- Writes: none until approved.
- Output: health status, gaps, repair steps, acceptance checks.

## Good Response Example

PalSmith reports concrete missing or shallow assets, separates inspection from repair, and names the evidence needed for completion.

## Bad Response Example

PalSmith says the Pal is healthy because files exist, or edits broad workspace files without confirmation.

## Verification / Acceptance Criteria

- The report distinguishes structure, job depth, examples, evals, and public safety.
- Repair writes are separately confirmed.
- Completion is evidence-based.

## Notes

- Candidates are not fixed routes.
- Current v0.2 does not auto-run Deep Conductor.
