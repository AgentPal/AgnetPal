# Cross-Pal Product Research Dev QA Docs

This public-safe example shows how Mira can organize a composite deliverable in Simple Pal Mode. It is a written staged Task Package example, not automatic Deep Conductor execution.

## User Request

"Research a product category, propose the MVP, implement a docs page, verify it, and write release notes."

## Conductor Judgement

Mira is the first Pal because the user did not directly call a specialist and the request contains multiple deliverables.

## Staged Task Judgement

- domain_focus: product research to documented release artifact.
- content_deliverables: research brief, product scope, release notes.
- final_deliverables: docs page and evidence-backed completion report.
- work_stages:
  - research stage: Vega candidate for source plan, evidence matrix, uncertainty.
  - product stage: Nova candidate for MVP scope and non-goals.
  - implementation stage: Atlas candidate for docs page package and file scope.
  - verification stage: Quinn candidate for evidence review.
  - documentation stage: Morgan candidate for release-note structure.
- runtime_candidates: search/browser Runtime for sources if approved; file-editing Runtime for docs page; shell Runtime for checks.
- verification_needs: source list, diff, rendered or reviewed page evidence, not-run list.

## Context Access List

| Stage | Candidate | Can read | Cannot read | Need output |
| --- | --- | --- | --- | --- |
| Research | Vega | user brief, approved sources | unrelated repo files, private memory | evidence matrix and uncertainty notes |
| Product | Nova | Vega summary, user constraints | raw source dump unless needed | MVP scope and non-goals |
| Implementation | Atlas | accepted scope, target docs path | unrelated Pal Packs | file-scope package and checks |
| Verification | Quinn | requirements, changed paths, command outputs | hidden reasoning drafts | pass/block/not-run review |
| Documentation | Morgan | accepted evidence, release boundary | unsupported claims | release-note structure |

## Staged Task Package

- Goal: produce an evidence-backed docs page and release-note package.
- Constraints: candidates are not fixed routes; Runtime is executor only; current v0.2 does not auto-run Deep Conductor.
- Steps:
  1. Mira writes this staged package and asks focused clarifications.
  2. Vega prepares research evidence if approved.
  3. Nova turns accepted evidence into product scope.
  4. Atlas prepares or executes the docs implementation package with Runtime evidence.
  5. Quinn reviews evidence and labels missing checks.
  6. Morgan structures release notes from accepted evidence.
- Output format: stage outputs, changed files, evidence, unresolved risks.

## Good Response Example

Mira states that the task is composite, names provisional stage candidates, separates Pal ownership from Runtime execution, and asks focused questions about sources, target docs location, and release boundary.

## Bad Response Example

Mira gives the whole request to one topic Pal, or says the Runtime will handle the page and QA without Pal-layer judgement.

## Verification / Acceptance Criteria

- The example names stage candidates and Context Access Lists.
- It keeps Runtime separate from Pal ownership.
- It requires evidence before completion.
- It does not claim automatic multi-Pal execution.
