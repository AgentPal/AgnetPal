# R110 Official Pal Metadata / Manifest Batch Proposal

Date: 2026-06-28

## Purpose

Recommend a conservative future execution sequence for official Pal `pal.json` v0.5 metadata and `asset-manifest.json` work.

R110 itself does not execute this proposal.

## Proposed Sequence

| Round | Scope | Output | Gate |
| --- | --- | --- | --- |
| R111 | Update 1-2 low-risk official Pal `pal.json` files, metadata only. Recommended pilot: Mira and PalSmith. | v0.5 metadata fields only; no real manifests. | R100-D + R110 gate before and after. |
| R112 | Rerun gate and repair pilot metadata if needed. | Fix-only metadata patch or issue record. | JSON parse, central roster, no manifest, no keyword routing, selected R95 groups if needed. |
| R113 | Generate preview manifests for the same pilot batch outside official Pal dirs or as dry-run evidence. | Public-safe preview artifacts only. | Manifest schema parse, source-map review, no official manifest files. |
| R114 | If approved, write real `asset-manifest.json` for the same pilot batch. | Real manifests for approved pilot Pals only. | R100-D postflight plus selected R95 groups. |
| Later batches | Continue in small groups. | Metadata first, preview second, real manifest third. | Repeat gate; do not batch all 9 without pilot evidence. |

## R111 Pilot Candidate Rationale

| Pal | Why candidate | Caution |
| --- | --- | --- |
| Mira | Recent memory/research/skills index coverage; Main Pal boundaries already reviewed in R105/R108/R109. | `name`, role wording, Main Pal special status, and external project write policy need review. |
| PalSmith | Recent memory/research/runbooks/skills index coverage; owns Pal asset governance and has strong boundary docs. | Governance capabilities must remain no-code and must not imply automatic roster edits, scanner behavior, or manifest generation. |

## Batch Rules

- Metadata-only first.
- One Pal or two Pals maximum for the pilot.
- No real official `asset-manifest.json` in R111.
- No central roster edit.
- No official Pal asset moves, deletes, or renames.
- No generated migration script.
- No scanner, validator, connector, daemon, marketplace/hub, auto-sync, or auto-execution behavior.
- Preserve old-Pal compatibility.
- Missing optional v0.5 fields are warnings until the approved execution round writes them.

## Human Approval Boundary

Entering R111 requires an explicit next-round objective or user confirmation. R110 does not authorize immediate metadata writes.

## R111 Expected Acceptance

R111 should commit only if:

- selected Pal `pal.json` files parse before and after;
- schema compatibility is checked;
- central roster remains unchanged;
- official Pal count remains 9;
- no real asset manifest is generated;
- no keyword routing, connector, scanner, or credential material appears;
- selected R95 groups are rerun if public loading or shared entries are affected;
- clean-copy pass is recorded.
