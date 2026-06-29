# R161 Docs Restructure Plan

## Goal

Prepare R162 to rewrite public-facing docs without losing evidence history or overclaiming runtime support.

## Proposed Structure

| Target group | Content |
| --- | --- |
| Current user docs | Root README files, `START_HERE.md`, current getting-started docs, Codex initialization, thin external project binding. |
| Pal Pack / authoring docs | `docs/03-pal-pack-standard/`, `docs/07-authoring-pals/`, official Pal docs. |
| Runtime adapter docs | `docs/04-runtime-guides/`, with clear Codex-first support and non-Codex limitations. |
| No-code methodology docs | Deep Conductor, Capability Inventory, Context Access List, Workflow Topology, Routing Reward Memory, PalBench as protocols and evidence assets. |
| Evidence archive | PalBench results, release checks, release notes, R143-R160 history, validation records. |
| Research / future design archive | Research docs, roadmap docs, experimental host notes, future orchestration ideas. |

## R162 Work Packages

| Package | Owner judgement | Output |
| --- | --- | --- |
| README rewrite | Quinn + Mira review | Public English and Chinese README pair. |
| Runtime claim tightening | Quinn + Rhea review | Evidence-backed runtime-support wording. |
| Docs index cleanup | Quinn | Updated doc navigation and archive links. |
| Release evidence link map | Quinn | Short link map from README to evidence archive. |
| Non-Codex host wording | Rhea + Quinn review | Honest not-run / partial / unavailable wording. |

## Acceptance Criteria For R162

- README no longer uses `INIT_PROMPT.md`.
- README does not overclaim Claude Code, OpenCode, Gemini, Plan Mode, Goal Mode, connectors, scanners, daemons, or external execution.
- README names AgentPal as a no-code Pal organization layer.
- README says Codex-first clearly.
- README reflects 10 official Pals and includes Faye.
- Evidence/history remains accessible but is not the first user path.

