# R110 Asset Manifest Readiness Source Map

Date: 2026-06-28

## Purpose

Define how a future `asset-manifest.json` preview could be sourced for official Pals without generating real manifests in R110.

This file is a source map and readiness note only. No `official/pals/*/asset-manifest.json` file is created by R110.

## Source Rules

| Manifest area | Preview source | Status rule | Review need |
| --- | --- | --- | --- |
| root entries | `README.md`, `PAL.md`, `pal.json`, `AGENTS.md`, `SKILL.md` | present / missing from actual files | missing root entry blocks that Pal's future upgrade |
| asset groups | existing top-level directories | present / missing / not-applicable candidate | not-applicable dirs need human review |
| directory indexes | `README.md`, `index.md`, `INDEX.md` inside asset dirs | present / missing | missing index is warning unless group is required |
| current asset files | directory listing | present count only | summaries need review; do not copy full content |
| status | index / README text plus file existence | present / partial / missing / not-run | do not claim reviewed without evidence |
| public safety | memory/research/skills indexes and standards | pass / needs-review | credentials/private content must be excluded |
| known gaps | missing indexes, missing manifests, unreviewed dirs | public-safe summary | no internal report body |

## Per-Pal Manifest Preview Readiness

| Pal | can_preview_manifest | missing source files | risky dirs | should_generate_in_next_round | safe only as preview | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| Mira | partial | real `asset-manifest.json` absent; reports index absent; identity/core indexes absent | memory/state/reports require public-safety review | no real manifest in R111; metadata pilot first | yes | Strong memory/research/skills index coverage; Main Pal wording needs careful summary. |
| PalSmith | partial | real `asset-manifest.json` absent; reports index absent; core/state indexes absent | memory/research/reports/governance outputs require review | no real manifest in R111; metadata pilot first | yes | Strong governance indexes; good pilot after metadata-only pass. |
| Atlas | partial | real `asset-manifest.json` absent; research/identity/core indexes absent | developer examples and runtime refs require Agent Skill boundary review | no | yes | Skills index exists; manifest preview should preserve runtime-execution boundary. |
| Quinn | partial | real `asset-manifest.json` absent; research/identity/core indexes absent | quality evidence and validation wording require no-scanner boundary review | no | yes | Skills index exists; future manifest needs not-run/evidence status. |
| Morgan | partial | real `asset-manifest.json` absent; research/identity/core indexes absent | document/file workflow may reference runtime tools; keep as refs | no | yes | Skills index exists; file-tool refs require review. |
| Nova | partial | real `asset-manifest.json` absent; research/identity/core indexes absent | product docs must not become user project facts store | no | yes | Skills index exists; product artifacts are not Pal Skills by default. |
| Vega | partial | real `asset-manifest.json` absent; research/identity/core indexes absent | research notes must not become raw knowledge or copied source dumps | no | yes | Skills index exists; source summary boundaries need review. |
| Harper | partial | real `asset-manifest.json` absent; research/identity/core indexes absent | writing examples and source material need copyright/public-safety review | no | yes | Skills index exists; no publishing automation. |
| Rhea | partial | real `asset-manifest.json` absent; research/identity/core indexes absent | system/runtime safety docs must not become scanners/installers | no | yes | Skills index exists; command refs need execution-boundary review. |

## Preview Generation Boundary

A future preview may be generated outside official Pal directories as dry-run evidence only after a metadata pilot is approved.

The preview must not include:

- full report bodies
- credentials or secrets
- route maps
- private project data
- raw research dumps
- external project local paths as Pal asset sources
- runtime state dumps
- connector configuration

## Next-Round Recommendation

R111 should not generate real manifests. It may prepare metadata-only updates for 1-2 pilot Pals if approved. R113 may generate preview manifests outside official Pal dirs after R112 reruns the gate.
