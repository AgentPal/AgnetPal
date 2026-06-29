# R161 Root Docs Keep / Rewrite / Delete Matrix

## Summary Counts

| Category | Count |
| --- | ---: |
| keep_current | 8 |
| rewrite_required | 5 |
| move_to_evidence_archive | 4 |
| delete_obsolete | 1 |
| Total audited root files | 18 |
| Final root files after deletion | 17 |

## Matrix

| File | Category | Decision |
| --- | --- | --- |
| `.gitignore` | keep_current | Keep as repository hygiene metadata. |
| `agentpal.json` | keep_current | Keep as current workspace metadata; update R161 status. |
| `AGENTS.md` | keep_current | Keep as runtime instruction gate. |
| `LICENSE` | keep_current | Keep. |
| `PAL.md` | keep_current | Keep as root Pal identity. |
| `RESOURCE_INDEX.md` | keep_current | Keep and update R161 evidence references. |
| `START_HERE.md` | keep_current | Keep as quick start index. |
| `THIRD_PARTY_NOTICES.md` | keep_current | Keep. |
| `README.md` | rewrite_required | Rewrite for v0.5 Codex-first public entry. |
| `README.zh-CN.md` | rewrite_required | Rewrite in sync with English README. |
| `SKILL.md` | rewrite_required | Tighten current capability boundary and avoid old runtime overclaims. |
| `CHANGELOG.md` | rewrite_required | Condense release history for public reader. |
| `CONTRIBUTING.md` | rewrite_required | Align contribution wording with v0.5 Pal Pack / workspace boundary. |
| `GITHUB_RELEASE_DRAFT.md` | move_to_evidence_archive | Keep as release working material, not first-entry docs. |
| `RELEASE_CHECKLIST.md` | move_to_evidence_archive | Keep as release evidence/checklist material. |
| `RELEASE_MANIFEST.md` | move_to_evidence_archive | Keep as release manifest material. |
| `RELEASE_NOTES.md` | move_to_evidence_archive | Keep as release notes material. |
| `INIT_PROMPT.md` | delete_obsolete | Deleted in R161; replaced by `prompts/codex/initialize-agentpal-workspace.md`. |

## Root Rewrite Guardrails

- Do not claim full Claude Code support without full host acceptance evidence.
- Do not claim OpenCode or Gemini support while current evidence is unavailable.
- Do not claim Plan Mode UI support while R160 says UI unavailable.
- Do not claim automatic multi-agent runtime, scanner, daemon, connector, app runtime, marketplace, or external system execution.
- Keep AgentPal described as a no-code Pal organization layer, not an Agent execution layer.

