# R161 to R162 Documentation Rewrite Readiness Decision

## Decision

`ready_for_r162_readme_docs_rewrite`

## Basis

- R161 removed the obsolete root `INIT_PROMPT.md` entry.
- The current Codex initialization prompt remains `prompts/codex/initialize-agentpal-workspace.md`.
- Root documentation and docs-directory governance categories are recorded.
- R160 evidence limits are carried forward into README rewrite requirements.
- No blocker was found in local validation.

## R162 Must Preserve

- Codex-first release language.
- 10 official Pals, including Faye.
- Claude Code as minimal handoff evidence only unless future full host acceptance passes.
- OpenCode and Gemini as unavailable in current evidence.
- Plan Mode UI unavailable.
- Goal Mode limited.
- No connector / scanner / daemon / runtime / marketplace / external-system execution claims.
- No public customer data or internal path leakage.

## R162 Should Produce

- Rewritten `README.md`.
- Rewritten `README.zh-CN.md`.
- Updated docs navigation if README links change.
- Optional archive moves for root release materials and duplicated runtime docs after human review.

