# R162 README Claim Guard

## Required Claims

| Claim | Status |
| --- | --- |
| AgentPal is a no-code Pal organization layer | present |
| AgentPal is not an Agent runtime | present |
| Skill / Pal / Agent distinction | present |
| Multi-Pal vs multi-Agent positioning | present |
| Codex-first verified path | present |
| Current official Pal count is 10 | present |
| Faye is an official Pal | present |
| Current initialization path is `prompts/codex/initialize-agentpal-workspace.md` | present |
| `INIT_PROMPT.md` is obsolete and must not be used | present |

## Forbidden Or Limited Claims

| Claim type | R162 result |
| --- | --- |
| Full Claude Code host acceptance | not claimed |
| OpenCode support | not claimed |
| Gemini support | not claimed |
| Plan Mode real UI verification | not claimed |
| Full Goal Mode support | not claimed |
| Automatic system scan | not claimed |
| Connector layer | not claimed |
| Scanner / daemon / marketplace / app runtime | not claimed |
| Direct GitHub / Notion / Lark / Cloudflare / CRM writeback | not claimed |
| Runtime-independent execution by AgentPal | not claimed |

## Official Pal Guard

Allowed official Pal names in README tables:

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

Not allowed as current official Pals unless future roster changes:

- Sage
- Orion

## Public-Safe Guard

The README pair and docs navigation must not include:

- internal local paths
- private user memory
- real customer data
- credentials
- internal completion reports
- unsupported runtime claims

