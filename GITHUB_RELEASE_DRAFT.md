# AgentPal v0.5.0-rc.1

AgentPal v0.5.0-rc.1 is a release candidate for the AgentPal v0.5 no-code Pal organization workspace.

Mark this GitHub Release as a pre-release unless maintainers explicitly decide otherwise.

## What This Is

AgentPal is a Markdown / JSON / protocol workspace that gives existing agent runtimes a Pal team organization layer.

It helps organize:

- Pal identities and responsibilities
- central contacts and direct `/pal Name` calls
- Pal Pack assets
- no-code collaboration rules
- task packages and output contracts
- verification and release evidence
- thin binding for external projects

AgentPal is not an Agent runtime, multi-Agent runtime, app runtime, installer, daemon, scanner, connector layer, marketplace, or executor.

## Highlights

- Codex-first AgentPal workspace initialization.
- Current official roster of 10 Pals: Mira, Atlas, Nova, Faye, Vega, Quinn, Morgan, Harper, Rhea, and PalSmith.
- Faye included as the AI Delivery Pal for business scenario, workflow, data/interface, risk, and Delivery Pack shaping.
- PalSmith v0.5 creation and governance path retained for Pal and Pal Team design.
- Clear Skill / Pal / Agent boundary:
  - Skill is a capability package.
  - Pal is a working partner that can use Skills and Agents.
  - Agent is the execution runtime.
- Public docs rewritten around current v0.5 boundaries.
- Release-candidate claim guard and clean-copy validation passed locally.

## Runtime Support Boundary

- Codex: verified first path.
- Claude Code: limited / minimal handoff evidence only.
- Generic CLI Agent: compatibility prompt path.
- DeepSeek / DeepSeek-TUI: experimental or version-help level only.
- OpenCode / Gemini: unavailable in current evidence.
- Plan Mode UI: unavailable in current UI evidence.
- Goal Mode: limited evidence.
- External systems: not generally validated for direct writeback.

## Getting Started

1. Open the AgentPal directory in Codex.
2. Copy `prompts/codex/initialize-agentpal-workspace.md`.
3. Paste it into a fresh Codex conversation.
4. Confirm Mira welcomes you and lists the 10 official Pals.

Useful entry points:

- `README.md`
- `README.zh-CN.md`
- `START_HERE.md`
- `docs/README.md`
- `RESOURCE_INDEX.md`

## Validation Summary

Local R166 / R167 checks confirm:

- official Pal dirs = 10
- central active contacts = 10
- Faye included
- README and README.zh-CN Pal tables = 10 rows each
- JSON parse checks passed
- Markdown link check passed
- clean-copy / zip content checks passed
- claim guard passed
- no `.git`, internal development records, credentials, or deprecated `INIT_PROMPT.md` entry in the release package

## Not Included

- No runtime code.
- No CLI installer.
- No desktop app or web app.
- No daemon, scanner, validator, connector layer, marketplace, hosted service, or automatic executor.
- No automatic subagent launch or external Agent calls by AgentPal.
- No automatic capability scan of the user's system.
- No private memory, real customer data, credentials, tokens, or internal development reports.

## Publication Boundary

This draft is a release body template. It does not prove that the tag or GitHub Release has already been published.

Before publication, maintainers should confirm the intended commit, tag, pushed branch, and release artifact.
