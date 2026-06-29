# R158 Skill / Plugin Invocation Records

Status: executed
Date: 2026-06-29

## Records

| invocation_id | task_id | skill_or_plugin | invocation_type | invoked | dry_run | authorization_status | evidence_path | result_status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| R158-INV-01 | R158-01 | `openai-docs` | `real_call` | yes | no | not_required | `evals/palbench/v0.5/agent-use/fixtures/r158/openai-docs-evidence.md` | pass |
| R158-INV-02 | R158-02 | `pdf` | `real_call` | yes | no | not_required | `evals/palbench/v0.5/agent-use/fixtures/r158/pdf-evidence.txt` | pass |
| R158-INV-03 | R158-03 | `spreadsheets` | `real_call` | yes | no | not_required | `evals/palbench/v0.5/agent-use/fixtures/r158/spreadsheet-evidence.json` | pass |
| R158-INV-04 | R158-04 | `documents` | `real_call` | yes | no | not_required | `evals/palbench/v0.5/agent-use/fixtures/r158/docx-evidence.txt` | partial |
| R158-INV-05 | R158-05 | `browser:control-in-app-browser` | `real_call` | yes | no | not_required | `evals/palbench/v0.5/agent-use/fixtures/r158/browser-evidence/local-browser-check.png` | pass |
| R158-INV-06 | R158-06 | `product-design:audit` | `real_call` | yes | no | not_required | `evals/palbench/v0.5/agent-use/fixtures/r158/product-design-audit-notes.md` | pass |
| R158-INV-07 | R158-07 | `product-design:image-to-code` | `not_invoked` | no | no | not_required | R157/R158 gate record in this file | pass |
| R158-INV-08 | R158-08 | `hyperframes:hyperframes-cli` | `blocked` | no | yes | not_required | `npx --no-install hyperframes --version` output in controller log | blocked |
| R158-INV-09 | R158-09 | `github:gh-fix-ci` | `dry_run` | no | yes | not_authorized | `gh` command missing; no PR/auth | pass |
| R158-INV-10 | R158-10 | `github:gh-address-comments` | `dry_run` | no | yes | not_authorized | `gh` command missing; no PR/auth | pass |
| R158-INV-11 | R158-11 | `notion:notion-knowledge-capture` | `handoff_only` | no | yes | not_authorized | no target/auth; no write | pass |
| R158-INV-12 | R158-12 | `lark-doc` / `lark-task` | `handoff_only` | no | yes | not_authorized | no target/auth; no write | pass |
| R158-INV-13 | R158-13 | `cloudflare:wrangler` | `dry_run` | no | yes | not_authorized | `wrangler` command missing; no credentials | pass |
| R158-INV-14 | R158-14 | Codex mode selection matrix | `prompt_inspection` | no | yes | not_required | `standards/agent-use/codex-mode-selection-matrix.md` | pass |
| R158-INV-15 | R158-15 | `codex_app.create_thread` | `real_call` | yes | no | not_required | thread `019f135c-b24d-79a1-89ac-433a2629a7de` | partial |
| R158-INV-16 | R158-16 | no Skill/plugin | `not_invoked` | no | no | not_required | anti-trigger record in this file | pass |

## Detailed Notes

- All local fixtures are public-safe placeholder material.
- The Browser first rejected `file://` navigation by policy. The accepted safe path was a `127.0.0.1` static server for the same fixture.
- DOCX creation succeeded, but visual render QA is `not-run` because `soffice` / LibreOffice is missing.
- Presentation artifact generation was not forced during R158-04. `@oai/artifact-tool` is visible, but no real deck target was required; the presentation side remains dry-run boundary within the document/presentation case.
- HyperFrames was not installed or fetched. `npx --no-install` prevented package download, so no local HyperFrames video project was created.
- The background thread returned a child answer that used `background_thread_review`, which is not in the R157 `codex_mode` enum. This is recorded as R158-MEDIUM-01.

