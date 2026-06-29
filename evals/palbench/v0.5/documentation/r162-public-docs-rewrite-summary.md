# R162 Public Docs Rewrite Summary

## Scope

R162 rewrote the first public documentation layer for AgentPal v0.5. The work used R161 documentation governance outputs, the user-provided README positioning draft, and the user-provided v0.5 paper draft as reference material.

This round did not rewrite the full `docs/` tree, did not add runtime code, and did not perform push, pull, fetch, tag, or GitHub Release operations.

## Files Updated

| File | Result |
| --- | --- |
| `README.md` | Rewritten as the English v0.5 public entry. |
| `README.zh-CN.md` | Rewritten as the Chinese v0.5 public entry, using the positioning draft while correcting current evidence and roster facts. |
| `docs/README.md` | Rewritten as a user navigation entry instead of a long historical index. |
| `SKILL.md` | Rewritten to clarify Workspace Skill entry, Pal / runtime boundary, official roster, and current initialization path. |
| `CONTRIBUTING.md` | Rewritten for v0.5 contribution, runtime-claim, and public-safety boundaries. |
| `CHANGELOG.md` | Condensed and updated with v0.5 public-docs rewrite and evidence boundary. |
| `RESOURCE_INDEX.md` | Updated with R162 evidence links. |
| `agentpal.json` | Updated with R162 documentation status and decision paths. |

`AGENTS.md` and `PAL.md` were checked and retained because they already preserve current v0.5 runtime gate and workspace identity boundaries.

## Positioning Changes

The rewritten README pair now says:

- AgentPal is a no-code AI team organization layer.
- AgentPal does not replace agent runtimes.
- Skill is a capability package.
- Pal is a working partner that uses Skills and Agents.
- Agent is the execution runtime.
- Multi-Pal and multi-Agent teams share the same goal, but AgentPal uses a lighter organization layer to reduce complexity and cost.
- AgentPal currently installs as a local workspace, not a package-manager dependency.
- Codex initialization uses `prompts/codex/initialize-agentpal-workspace.md`.

## Roster Correction

The user positioning draft contained Sage and Orion as draft Pal examples. R162 did not copy them into the public README because they are not registered official Pals.

The README pair uses the current 10 official Pals:

- Mira
- Atlas
- Nova
- Faye
- Vega
- Quinn
- Morgan
- Harper
- Rhea
- PalSmith

Source of truth: `workspace/organization/contacts/pals.json`.

## Runtime Claim Tightening

| Capability | Public wording after R162 |
| --- | --- |
| Codex | verified first path |
| Codex child/background thread and subagent usage | limited / evidence-backed only where host evidence and authorization exist |
| Claude Code | limited, minimal handoff evidence only |
| Generic CLI agents | compatibility path, not broad validation |
| DeepSeek / DeepSeek-TUI | experimental or version-help level |
| Plan Mode | UI evidence unavailable |
| Goal Mode | limited |
| OpenCode / Gemini | unavailable in current evidence |
| External systems | not generally validated for direct writeback |

## Readiness Decision

R162 decision value: `ready_for_r163_docs_directory_restructure`

Reason:

- The public README pair is now aligned with v0.5 positioning.
- The current initialization entry is unambiguous.
- The docs navigation entry is simplified.
- Overclaiming around non-Codex runtimes and automatic execution was removed from the first public path.

