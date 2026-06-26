# Capability Profiles

This directory holds public-safe Capability Inventory profiles and illustrative examples.

Capability profiles describe possible runtimes, models, reasoning modes, Skills, plugins, MCP servers, and Pal capabilities as AI Judgement inputs. They are not route maps and not automatic environment probes.

## v0.2 Use Flow

1. Mira or an owner Pal performs Task Judgement from the user goal.
2. The Pal decides whether a capability profile is useful.
3. The Pal reads the smallest relevant profile, not the full inventory.
4. The profile informs candidate selection.
5. The Pal outputs candidates in a Task Package or Context Access List when needed.
6. Completion still requires current Runtime evidence.
7. Experience may be recorded manually later; v0.2 does not auto-write routing memory.

## Rules

- Examples are illustrative only.
- Do not treat a profile as proof that the user's environment has that capability.
- Do not encode task/domain to Pal, runtime, model, Skill, plugin, or MCP choices.
- Do not store private credentials, private paths, or private project data.
- Keep profile loading bounded by Context Slicing.
- Use profiles to support AI Judgement, Context Access Lists, Task Packages, verification, and PalBench.

## Subdirectories

| Directory | Purpose |
| --- | --- |
| `runtime-profiles/` | Runtime capability examples |
| `model-profiles/` | Model capability examples |
| `reasoning-profiles/` | Reasoning strength examples |
| `skill-profiles/` | Skill capability examples |
| `plugin-profiles/` | Plugin capability examples |
| `mcp-profiles/` | MCP capability examples |
| `pal-profiles/` | Pal capability examples |

AgentPal v0.2 active runtime remains Simple Pal Mode only. Capability Inventory does not activate Deep Conductor or automatic multi-agent execution.
