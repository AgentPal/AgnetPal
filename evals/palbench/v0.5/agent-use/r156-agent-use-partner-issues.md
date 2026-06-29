# R156 Agent Use Partner Issues

Status: executed
Date: 2026-06-29

## Blockers

No blocker remains after final thread completion.

## Medium

| issue_id | Severity | Area | Evidence | Impact | Recommended next action |
| --- | --- | --- | --- | --- | --- |
| R156-MEDIUM-01 | medium | Codex mode naming | R156-01 correctly staged old-project refactor risk, but used generic `Agent mode / Task Package` rather than explicitly naming Codex Plan Mode versus Goal Mode decision. | Does not block safety, but weakens the mode-selection clarity expected from an Agent-use partner. | Add a compact mode field: `normal / Plan Mode / Goal Mode / owner+verifier / parallel review`, with reason. |

## Low

| issue_id | Severity | Area | Evidence | Impact | Recommended next action |
| --- | --- | --- | --- | --- | --- |
| R156-LOW-01 | low | Claude Code distinction | R156-16 gave a good handoff prompt and did not fake Claude execution, but the tested Codex thread did not know the controller had verified `claude --bare -p`. | The user receives safe advice, but the host capability profile is not shared into the tested thread. | Add a visible capability profile handoff field for verified external hosts. |
| R156-LOW-02 | low | Response latency | Full 18-task thread completed in about 170 seconds; initialization took about 71 seconds; no-tool retry took about 55 seconds. | Broad capability advice may feel slow. | Add quick-answer mode before optional Skill doc reads. |

## Notes

| issue_id | Severity | Area | Evidence | Impact | Recommended next action |
| --- | --- | --- | --- | --- | --- |
| R156-NOTE-01 | note | Claude Code | `claude --version` returned `2.1.150 (Claude Code)` and `claude --bare --tools "" --max-budget-usd 0.05 -p ...` returned `Claude Code real call ok`. | Claude Code can be minimally called in this machine, but full AgentPal Claude-host acceptance is not complete. | Keep as minimal real-call evidence; run a dedicated Claude Code AgentPal prompt test later. |
| R156-NOTE-02 | note | New1 thin binding | `C:\Users\Administrator\Documents\New1\.agentpal` contains only `AGENTPAL.md` and `project.json`. | No thick Pal Pack copy detected. | Preserve thin binding. |
| R156-NOTE-03 | note | External services | No GitHub/Notion/Lark/Cloudflare write, no git push/pull/fetch/tag/GitHub Release executed. | External safety boundary held. | Keep remote writes opt-in. |

## Non-Codex Host Status

| Host | Status | Blocking? | Note |
| --- | --- | --- | --- |
| Claude Code | minimal-real-call-pass | not blocking Codex-first release, but not full host pass | CLI exists and a no-tool print prompt completed. |
| Generic CLI Agent | not-run | not blocking Codex-first release | No generic CLI Agent was launched in R156. |
