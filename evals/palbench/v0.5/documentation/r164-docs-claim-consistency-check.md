# R164 Docs Claim Consistency Check

Date: 2026-06-30

## Required Claim Surface

| Claim | Result |
| --- | --- |
| AgentPal is a lightweight Pal team organization layer | pass |
| AgentPal is not an Agent runtime or execution layer | pass |
| Codex-first verified path is preserved | pass |
| Claude Code is limited/minimal handoff, not full host acceptance | pass |
| Generic CLI Agent is compatibility path, not broad host acceptance | pass |
| OpenCode / Gemini are unavailable in current evidence | pass |
| DeepSeek is experimental/version-help only where mentioned | pass |
| Plan Mode UI unavailable; Goal Mode limited | pass |
| Host capability requires visible evidence, manual profile, or runtime-reported profile | pass |
| No connector / scanner / daemon / marketplace / app runtime claim | pass |
| External project binding remains thin | pass |
| Official roster is 10 Pals and includes Faye | pass |
| No Sage / Orion current roster residue | pass |
| Customer-private data excluded from public examples and Pal Packs | pass |

## Scans

Commands executed:

```text
stale-current-claim scan over README.md, README.zh-CN.md, docs, RESOURCE_INDEX.md, and agentpal.json
```

Result: no matches.

```text
internal-path-and-attachment-id scan over README.md, README.zh-CN.md, docs, RESOURCE_INDEX.md, agentpal.json, evals/palbench/v0.5/documentation, and release
```

Result: no matches.

## Notes

Some historical evidence and migration documents still mention older version numbers or old rollout identifiers. Those are not primary user docs and remain historical traceability. R164 rewrote high-visibility current user and integrator docs rather than deleting historical evidence.

## Result

Status: `pass`
