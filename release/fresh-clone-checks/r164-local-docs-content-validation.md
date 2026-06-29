# R164 Local Docs Content Validation

Date: 2026-06-30

## Validation Summary

| Check | Result |
| --- | --- |
| `agentpal.json` parses | pass |
| `workspace/organization/contacts/pals.json` parses | pass |
| official Pal `pal.json` files parse | pass |
| central contacts count | pass, 10 registered / 10 active |
| Faye in active contacts | pass |
| official Pal `pal.json` count | pass, 10 |
| stale current-roster names Sage / Orion | pass, no matches |
| obsolete `INIT_PROMPT` current entry | pass, no matches |
| old official 9 Pal current claim | pass, no matches |
| internal R164 report path leak | pass, no matches |
| Markdown local links | pass, 156 files checked, 0 missing links |
| `git diff --check` | pass |

## Commands

```text
Get-Content -Raw agentpal.json | ConvertFrom-Json
Get-Content -Raw workspace/organization/contacts/pals.json | ConvertFrom-Json
Get-ChildItem official/pals -Filter pal.json -Recurse -File | ConvertFrom-Json
```

```text
stale-current-claim scan over README.md, README.zh-CN.md, docs, RESOURCE_INDEX.md, and agentpal.json
```

```text
internal-path-and-attachment-id scan over README.md, README.zh-CN.md, docs, RESOURCE_INDEX.md, agentpal.json, evals/palbench/v0.5/documentation, and release
```

```text
git diff --check
```

## Remote Operations

No push, pull, fetch, tag, or GitHub Release operation was performed.

## Source Directory Boundary

This validation was performed in the AgentPal workspace. No external project write was performed.

## Result

Status: `pass`
