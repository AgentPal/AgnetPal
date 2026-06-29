# R157 Agent-use Decision Protocol Issues

Status: executed
Date: 2026-06-29

## Summary

No blocker, high, or medium issue remains in R157.

| issue_id | severity | area | finding | expected | actual | recommended_fix | fixed_in_R157 | blocks_R158 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| R157-NOTE-01 | note | Claude Code | R157 adds acceptance card but does not run full Claude Code host acceptance | Full host acceptance requires a real Claude Code project task and Quinn verification | Minimal call evidence only remains from R156 | Run in R158 or a dedicated host acceptance round | no | no |
| R157-NOTE-02 | note | Generic CLI Agent | Generic CLI real host remains not-run | Keep not-run until actual process evidence exists | Correctly not claimed | Run only if Generic CLI support is needed beyond Codex-first release | no | no |
| R157-NOTE-03 | note | Real invocation | R157 adds invocation record but does not invoke real plugins | R157 is protocol enhancement only | Correctly deferred to R158 | Use records in R158 real Skill/plugin/mode invocation tests | yes | no |

