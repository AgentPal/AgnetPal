# R161 Documentation Governance Audit

## Scope

R161 audited documentation governance for the AgentPal Workspace after R160. It did not rewrite public docs, did not create runtime code, and did not perform any remote GitHub operation.

Audited current facts:

- Workspace root: `J:\开发\AgentPal`
- Current release posture: Codex-first, evidence-limited release readiness
- Official Pal count: 10
- Official Pals: Mira, Atlas, Vega, Rhea, PalSmith, Quinn, Morgan, Harper, Nova, Faye
- Faye status: official Pal
- Claude Code status: minimal handoff evidence only, not full host acceptance
- OpenCode / Gemini status: unavailable in R159 evidence
- Plan Mode status: UI unavailable in R160 evidence
- Goal Mode status: active-goal evidence with UI capture limitation
- External project writeback: not validated as a general public claim

## Current Evidence Inputs

| Area | Files checked |
| --- | --- |
| Root entry files | `README.md`, `README.zh-CN.md`, `AGENTS.md`, `PAL.md`, `SKILL.md`, `START_HERE.md`, `RESOURCE_INDEX.md`, release root files |
| Workspace metadata | `agentpal.json`, `workspace/organization/contacts/pals.json`, `workspace/organization/contacts/PAL_CONTACTS.md` |
| Runtime prompts | `prompts/codex/initialize-agentpal-workspace.md`, `prompts/claude/CLAUDE.md`, runtime guide docs |
| Public docs | `docs/` directory tree |
| Standards/templates/examples | `standards/`, `templates/`, `examples/` |
| Evidence | `evals/palbench/v0.5/agent-use/`, `release/fresh-clone-checks/`, `release/integration-notes/` |

## Main Findings

| Finding | Severity | Status | Notes |
| --- | --- | --- | --- |
| Root README files are too broad for v0.5 release entry | high | rewrite_required | They mix historical development, future-oriented language, and release evidence into first-entry docs. |
| `INIT_PROMPT.md` is an obsolete duplicate entry | high | deleted_obsolete | Current entry is `prompts/codex/initialize-agentpal-workspace.md`; active docs no longer reference `INIT_PROMPT.md`. |
| Root release draft/checklist/manifest/notes are not user first-entry docs | medium | move_to_evidence_archive | Keep as release evidence or history, but not as first-entry public usage docs. |
| Runtime support claims need tightening | medium | rewrite_required | Public docs must claim Codex-first only; Claude Code remains minimal handoff evidence unless fully tested later. |
| Docs tree contains multiple historical version tracks | medium | rewrite_required / move_to_evidence_archive | Keep evidence, but split user docs from release/eval/history material. |
| Public docs must avoid internal path leakage | blocker check | pass | Public R161 outputs do not include internal report path. |

## Old Entry / Old Wording Scan

| Pattern | Result |
| --- | --- |
| `INIT_PROMPT.md` in active entry docs | none after deletion and `RESOURCE_INDEX.md` update |
| `START_HERE.md` | still valid as quick start index |
| `OpenCode` / `Gemini` | present in historical/evidence files; public rewrite must not claim support |
| `Claude Code` | present; rewrite must say minimal handoff evidence only unless future full host acceptance passes |
| `Plan Mode` | present; rewrite must say UI unavailable in R160 |
| `Goal Mode` | present; rewrite must say limited evidence, not full UI-host claim |
| scanner / daemon / connector / marketplace expansion | no new implementation added by R161 |

## Governance Decision

R161 decision value: `ready_for_r162_readme_docs_rewrite`

Reason:

- Obsolete root entry `INIT_PROMPT.md` was deleted.
- Active initialization path is unambiguous: `prompts/codex/initialize-agentpal-workspace.md`.
- Root and docs rewrite boundaries are now separated into user docs, evidence archives, deletion candidates, and human-decision areas.
- No blocker was found in JSON validity, Pal count, public-path leakage, or local-only execution boundaries.

