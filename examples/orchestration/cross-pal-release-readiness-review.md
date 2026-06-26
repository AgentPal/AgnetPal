# Cross-Pal Release Readiness Review

This public-safe example shows how a release readiness review can use staged owner candidates without automated multi-agent execution.

## User Request

"Before I commit and release, recheck the changed docs, no-code boundary, quality evidence, and release notes."

## Conductor Judgement

Mira can conduct because the request mixes system boundary, quality review, documentation, and possible execution evidence. Quinn may own the final readiness judgement if the user asks for pass/block quality status.

## Staged Task Judgement

- domain_focus: release readiness.
- content_deliverables: boundary report, evidence review, release-note structure, final summary.
- final_deliverables: readiness status and commit/release recommendation.
- work_stages:
  - no-code boundary: Rhea candidate.
  - quality evidence: Quinn candidate.
  - documentation structure: Morgan candidate.
  - development evidence repair: Atlas candidate if missing checks need a package.
  - final summary: Mira candidate after evidence is available.
- runtime_candidates: shell/file Runtime for changed-file list, JSON parse, diff checks, and text scans.
- verification_needs: changed files, checks run, checks not run, blocker list.

## Context Access List

| Stage | Candidate | Can read | Cannot read | Need output |
| --- | --- | --- | --- | --- |
| Boundary | Rhea | changed-file list, no-code policy | unrelated user projects | no-code boundary status |
| Quality | Quinn | requirements, evidence, command outputs | hidden drafts | pass/block/not-run findings |
| Docs | Morgan | changed docs, release notes | private internal notes | doc structure issues |
| Repair | Atlas | missing dev evidence request | unrelated codebase | repair package if needed |
| Summary | Mira | accepted stage outputs | raw private data | user-facing closeout |

## Staged Task Package

- Goal: decide whether release readiness is evidenced.
- Constraints: no push, tag, or release action happens from this example; current v0.2 does not auto-run Deep Conductor.
- Steps: collect changed files, run allowed checks, review boundary, review evidence, structure docs findings, summarize.
- Output: readiness status, blockers, warnings, not-run list, next action.

## Good Response Example

Mira or Quinn separates the release question into evidence-backed stages and refuses to say ready until required checks are proven.

## Bad Response Example

The response treats a clean-looking summary as proof, hides not-run checks, or performs release actions without explicit user instruction.

## Verification / Acceptance Criteria

- The example separates readiness from release action.
- It names no-code, quality, docs, repair, and summary stages.
- It keeps candidates non-binding.
- It requires current Runtime evidence for execution claims.
