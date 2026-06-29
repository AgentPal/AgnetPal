# AgentPal v0.5.0-rc.1 Release Notes

AgentPal v0.5.0-rc.1 is a local release-candidate package for AgentPal v0.5.

This package is GitHub-ready for maintainer review, but it is not a published GitHub Release until an authorized maintainer performs the tag, push, and GitHub Release steps.

## What AgentPal Is

AgentPal is a no-code Pal organization layer for existing agent runtimes.

It provides a readable Markdown / JSON / protocol workspace for:

- Pal identities and responsibilities
- central Pal contacts
- Pal Pack assets
- task packages and output contracts
- no-code collaboration and verification rules
- project thin binding guidance
- public-safe templates, examples, standards, and evidence records

AgentPal does not replace Codex, Claude Code, OpenCode, OpenHands, Gemini CLI, DeepSeek-TUI, or other host runtimes. The host runtime still performs real file edits, commands, tool calls, publishing, and external-system actions.

## Built-In Pals

The v0.5 official Pal roster contains 10 active Pals:

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

The source of truth is `workspace/organization/contacts/pals.json`.

## Main v0.5 Changes

- Reframed the public README and docs around AgentPal as a no-code Pal team organization layer, not an Agent runtime.
- Clarified the Skill / Pal / Agent relationship.
- Added Faye as the official AI Delivery Pal.
- Updated Codex-first initialization using `prompts/codex/initialize-agentpal-workspace.md`.
- Preserved thin binding for external projects.
- Added and validated v0.5 documentation governance, claim guard, release-candidate scope, and fresh-clone evidence records.
- Kept non-Codex host claims conservative and evidence-bound.

## Current Runtime Support Claims

- Codex: verified first path.
- Claude Code: limited / minimal handoff evidence only.
- Generic CLI Agent: compatibility prompt path.
- DeepSeek / DeepSeek-TUI: experimental or version-help level only.
- OpenCode / Gemini: unavailable in current evidence.
- Plan Mode UI: unavailable in current UI evidence.
- Goal Mode: limited evidence.

## What This Package Does Not Include

- No Agent runtime.
- No multi-Agent runtime.
- No desktop app or web app.
- No CLI installer, daemon, scanner, connector layer, marketplace, hosted runtime, or automatic executor.
- No automatic subagent launch or external Agent calls by AgentPal.
- No automatic capability scan of the user's machine.
- No general direct writeback integration for GitHub, Notion, Lark, Cloudflare, CRM, or customer systems.
- No real customer data, credentials, tokens, private memory, or internal development records.

## Validation Summary

R166 release-candidate preflight passed before R167 package preparation:

- official Pal directories: 10
- central active contacts: 10
- Faye included: yes
- README and README.zh-CN Pal tables: 10 rows each
- core JSON parse: pass
- visible JSON parse: pass
- Markdown link check: 158 files, 0 missing
- clean-copy validation: pass
- claim guard: pass
- internal path leak scan: pass
- credential scan: pass
- added executable artifact check: pass

R167 prepares the local zip package and re-checks the package contents before any remote publication action.

## Getting Started

1. Clone, download, or unzip the AgentPal package.
2. Open the AgentPal directory as a Codex project.
3. Open `prompts/codex/initialize-agentpal-workspace.md`.
4. Paste the prompt into a fresh Codex conversation.
5. Confirm Mira appears and lists the 10 official Pals.

Start from:

- `README.md`
- `README.zh-CN.md`
- `START_HERE.md`
- `docs/README.md`
- `RESOURCE_INDEX.md`

## Publication Boundary

This local package does not mean a GitHub Release exists.

Tag creation, `git push`, and GitHub Release publication require explicit maintainer authorization in a separate release operation.
