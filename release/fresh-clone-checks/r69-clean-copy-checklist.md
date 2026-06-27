# R69 Fresh Clone Clean-Copy Checklist

Use this checklist before claiming that a fresh clone can understand the current AgentPal Workspace layout without relying on stale v0.3 paths.

## Required Layout Signals

- Root `README.md`, `AGENTS.md`, `PAL.md`, `SKILL.md`, and `RESOURCE_INDEX.md` point to `workspace/organization/contacts/` for central Pal roster discovery.
- Official bundled Pal Packs live under `official/pals/`.
- `pals/`, `contacts/`, and `registry/` are compatibility pointers or legacy records, not the active source of truth.
- Project binding templates live under `templates/project-binding/`.
- `projects/project-workgroup-template/agentpal/` is a compatibility pointer only.

## External Project Binding

Expected new Codex binding files:

- `.agentpal/project.json`
- `.agentpal/AGENTPAL.md`
- protected AgentPal block in `AGENTS.md`

Expected new Claude Code additions:

- `.agentpal/project.json`
- `.agentpal/AGENTPAL.md`
- protected AgentPal block in `CLAUDE.md`
- `.claude/settings.local.json`
- `.gitignore` entry for `.claude/settings.local.json`

Must not create by default:

- `.agentpal/memory/`
- `.agentpal/state/`
- `.agentpal/reports/`
- `.agentpal/context/`
- `.agentpal/index/`
- `.agentpal/pals/`
- `.agentpal/workflows/`
- `.agentpal/evals/`

## Official Pal Asset Visibility

- `official/pals/*/PAL.md`, `SKILL.md`, `AGENTS.md`, `README.md`, and `pal.json` are visible to Git when untracked.
- Runtime state and private memory under `official/pals/*/state/` and `official/pals/*/memory/user/` remain ignored.
- `official/pals/*/reports/**/README.md` placeholders may be visible.
- Real historical reports and state are stored under `archive/migration-from-v0.3/official-pal-history/`.

## Legacy Reference Review

Classify remaining old references as one of:

- `active-bug`: current install, runtime, or user-facing docs still point to old source-of-truth paths.
- `compatibility-pointer`: a file intentionally redirects old readers to current paths.
- `historical-archive`: old release or migration record kept for history.
- `regression-case`: eval text intentionally preserves the old shape being tested.

Fresh-clone readiness requires zero `active-bug` references.
