# Capability Inventory Minimal Usable Self-Test

This Markdown self-test checks the R43 minimal Capability Inventory implementation. It is not a script, scanner, validator, or CLI.

## Required Files

| File group | Expected result |
| --- | --- |
| Runtime profiles | `codex.example.json`, `claude-code.example.json`, `generic-cli.example.json` exist and parse |
| Model profiles | `generic-strong-model.example.json`, `generic-economy-model.example.json` exist and parse |
| Reasoning profiles | `reasoning-strengths.example.json` exists and parses |
| Skill profiles | at least two generic Skill examples exist and parse |
| Plugin / MCP templates | plugin and MCP profile templates exist and parse |
| Pal profiles | at least five Pal capability examples exist and parse |
| Design doc | minimal usable design exists |
| Protocol | Capability Inventory protocol explains v0.2 manual profile flow |

## Required Profile Fields

Every example profile should include:

- `example_status`
- `not_auto_detected`
- `used_for`
- `not_a_fixed_route`

## Boundary Checks

- Profiles are illustrative unless maintained by user or maintainer.
- Profiles do not claim to describe the user's current environment.
- Profiles do not replace Task Judgement.
- Profiles do not trigger Runtime, Skill, plugin, or MCP execution.
- Profiles do not make a Pal an Agent.
- Runtime evidence remains required for execution claims.

## Expected R43 Result

Expected result: pass after JSON parse and boundary scans succeed.
