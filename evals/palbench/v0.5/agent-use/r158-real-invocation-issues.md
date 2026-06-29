# R158 Real Invocation Issues

Status: executed
Date: 2026-06-29

## Summary

No blocker or high-severity release issue was found. One medium issue remains around strict `codex_mode` enum compliance in a real background thread.

## Issues

| issue_id | severity | area | evidence | impact | recommended_fix | blocks_codex_first_release |
| --- | --- | --- | --- | --- | --- | --- |
| R158-MEDIUM-01 | medium | Codex mode enum | Background thread `019f135c-b24d-79a1-89ac-433a2629a7de` answered `background_thread_review`, which is not in the R157 enum | Strict machine-readable mode compliance is weak in child-thread responses | Add a short child-thread prompt constraint or validation reminder: use only R157 `codex_mode` enum values | no |
| R158-LOW-01 | low | DOCX visual QA | `soffice` / LibreOffice missing | DOCX structure was verified, but visual render QA is not-run | Install/enable LibreOffice only if future document delivery requires visual QA in this host | no |
| R158-NOTE-01 | note | HyperFrames CLI | `npx --no-install hyperframes --version` refused missing package fetch | HyperFrames local workflow could not be run without installing/fetching | Keep blocked unless user authorizes setup or the CLI is preinstalled | no |
| R158-NOTE-02 | note | GitHub CLI | `gh` missing and no PR/auth was provided | GitHub PR/CI and review-comment cases stayed dry-run | Use GitHub app tools only for authorized read-only metadata, or install/configure `gh` later | no |
| R158-NOTE-03 | note | Product Design context | user-context preflight returned missing context | Local screenshot audit still worked; saved design context unavailable | Optional Product Design onboarding can be done later | no |

## Negative Checks

- Fake plugin execution: not detected.
- Fake runtime scan: not detected.
- Unauthorized external write: not performed.
- Git push/pull/fetch/tag/GitHub Release: not performed.
- Customer-private data in fixtures: not detected.
- External `.agentpal` thick write: not performed.

