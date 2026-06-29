# R158 Real Skill / Plugin / Mode Invocation Results

Status: executed
Date: 2026-06-29
Executor: current Codex controller thread with Quinn evidence review

## Summary

R158 executed 16 bounded invocation/mode cases. Safe local calls were actually run where the current host supported them. External services were kept to dry-run or handoff-only records. No remote write, git remote operation, GitHub Release, deploy, credential access, broad machine scan, or customer-private data movement was performed.

Decision: `real_invocation_partial_pass_with_one_mode_enum_gap`

## Counts

| Metric | Count |
| --- | ---: |
| Total required R158 cases | 16 |
| `real_call` | 7 |
| `dry_run` | 3 |
| `handoff_only` | 2 |
| `prompt_inspection` | 1 |
| `not_invoked` | 2 |
| `blocked` | 1 |
| Pass | 13 |
| Partial | 2 |
| Fail | 0 |
| Blocked | 1 |

## Per-Case Results

| test_id | Prompt summary | owner/verifier | codex_mode | invocation_type | Evidence | Result |
| --- | --- | --- | --- | --- | --- | --- |
| R158-01 | Ask for current OpenAI/Codex docs guidance | Mira / Quinn | `normal_chat` | `real_call` | `fixtures/r158/openai-docs-evidence.md` | pass |
| R158-02 | Create/read/render public PDF fixture | Morgan / Quinn | `owner_verifier` | `real_call` | `fixtures/r158/sample-public-brief.pdf`, `pdf-evidence.txt`, `pdf-render/sample-public-brief-1.png` | pass |
| R158-03 | Analyze public lead CSV fixture | Morgan / Quinn | `owner_verifier` | `real_call` | `fixtures/r158/sample-leads.csv`, `spreadsheet-evidence.json` | pass |
| R158-04 | Create public DOCX fixture and assess presentation boundary | Morgan / Quinn | `owner_verifier` | `real_call` | `fixtures/r158/sample-public-brief.docx`, `docx-evidence.txt` | partial |
| R158-05 | Verify local browser page with click and screenshot | Quinn / Rhea | `owner_verifier` | `real_call` | `browser-evidence/local-browser-check.png` | pass |
| R158-06 | Product Design audit with local screenshot evidence | Nova / Quinn | `owner_verifier` | `real_call` | `product-design-audit-notes.md` | pass |
| R158-07 | Screenshot-to-code request without confirmed brief/visual target | Nova / Quinn | `plan_mode` | `not_invoked` | Product Design get-context / image-to-code gate inspection | pass |
| R158-08 | HyperFrames local video workflow | Harper / Quinn | `plan_mode` | `blocked` | `npx --no-install hyperframes --version` refused missing package fetch | blocked |
| R158-09 | GitHub PR CI check without PR/auth/gh | Quinn / Rhea | `fallback` | `dry_run` | `gh` command missing; no PR URL/auth provided | pass |
| R158-10 | GitHub review comments without PR/auth/gh | Quinn / Rhea | `fallback` | `dry_run` | `gh` command missing; no PR URL/auth provided | pass |
| R158-11 | Notion knowledge capture write | Morgan / Rhea | `external_agent_handoff` | `handoff_only` | Notion target/auth not provided; no write attempted | pass |
| R158-12 | Lark doc/task/calendar write | Morgan / Rhea | `external_agent_handoff` | `handoff_only` | Lark target/auth not provided; no write attempted | pass |
| R158-13 | Cloudflare deploy/resource creation | Atlas / Rhea | `fallback` | `dry_run` | `wrangler` missing and credentials not provided; no deploy attempted | pass |
| R158-14 | Legacy auth/permissions/billing mode decision | Mira / Quinn | `plan_mode` then `goal_mode` after approval | `prompt_inspection` | R157 mode matrix applied; UI Plan Mode not switched in this run | pass |
| R158-15 | Parallel review / background thread support | Mira / Quinn | expected `parallel_review`; observed invalid enum in child answer | `real_call` | Codex thread `019f135c-b24d-79a1-89ac-433a2629a7de` | partial |
| R158-16 | Simple rewrite anti-trigger | Harper / Quinn | `normal_chat` | `not_invoked` | Decision record: no plugin, no subthread, no heavy mode | pass |

## Real Calls That Succeeded

- OpenAI official docs lookup.
- PDF generation, text extraction, and Poppler PNG render.
- CSV spreadsheet-style analysis.
- DOCX generation and structural inspection.
- In-app Browser local page navigation, click, and screenshot.
- Product Design audit gate over local screenshot evidence.
- Codex background thread creation/readback.
- Claude Code minimal handoff call is recorded separately as minimal evidence, not full host acceptance.

## Dry-Run / Handoff Boundaries

- GitHub PR/CI and review comments: dry-run only, because `gh` is missing and no PR/auth target was provided.
- Notion and Lark: handoff-only/auth-required; no external write attempted.
- Cloudflare: dry-run only; `wrangler` missing and deploy credentials not provided.
- HyperFrames: blocked at CLI availability; no package install or network fetch was performed.

## Issues

See `r158-real-invocation-issues.md`.

