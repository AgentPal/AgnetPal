# R158 Local Real Invocation Validation

Status: executed
Date: 2026-06-29

## Validation Checks

| Check | Result | Evidence |
| --- | --- | --- |
| R158 report files exist | pass | All required R158 report/decision files added |
| Host Capability Snapshot exists | pass | `evals/palbench/v0.5/agent-use/fixtures/r158/host-capability-snapshot.json` |
| Invocation records include evidence paths | pass | `r158-skill-plugin-invocation-records.md` |
| `codex_mode` fields use R157 enum in parent records | pass | Parent R158 tables use R157 enum values |
| Child-thread enum compliance | partial | Thread `019f135c-b24d-79a1-89ac-433a2629a7de` used invalid `background_thread_review` |
| Parse all visible JSON | pass | 110 JSON files parsed with PowerShell `ConvertFrom-Json -AsHashtable`, 0 failures |
| Parse `agentpal.json` | pass | included in the 110 JSON parse pass after metadata update |
| Parse central roster | pass | `registered_pals` count = 10; Faye present |
| Official Pal dir count = 10 | pass | `official/pals` count = 10 |
| All official Pal `pal.json` parse | pass | 10 parsed, 0 failures |
| New1 thin binding if touched | pass | `C:\Users\Administrator\Documents\New1\.agentpal` contains only `AGENTPAL.md` and `project.json` |
| Fake invocation scan | pass | Records separate `real_call`, `dry_run`, `handoff_only`, `not_invoked`, and `blocked` |
| Unauthorized external write scan | pass | No GitHub/Notion/Lark/Cloudflare write executed |
| Git remote action boundary | pass | No push/pull/fetch/tag/GitHub Release performed |
| Customer-private fixture scan | pass | R158 fixtures are public-safe placeholders |
| HyperFrames no-install boundary | pass | `npx --no-install` blocked package fetch; no install attempted |
| Claude Code full acceptance boundary | pass | Minimal call only; full host acceptance is not-run |

## New1 Thin Binding Evidence

`C:\Users\Administrator\Documents\New1\.agentpal` contains:

- `AGENTPAL.md`
- `project.json`

No `.agentpal/pals`, `.agentpal/memory`, `.agentpal/reports`, Pal Pack, docs, evals, release files, or thick workgroup directories were observed.

## Remote Boundary

No `git push`, `git pull`, `git fetch`, tag creation, GitHub Release, GitHub publication API action, Notion write, Lark write, Cloudflare deploy, or remote publication was performed.

## Validation Decision

`r158_real_invocation_partial_pass_ready_for_r159_enum_tightening`
