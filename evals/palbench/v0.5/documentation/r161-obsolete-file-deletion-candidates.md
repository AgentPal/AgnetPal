# R161 Obsolete File Deletion Candidates

## Deleted In R161

| File | Category | Action | Reason |
| --- | --- | --- | --- |
| `INIT_PROMPT.md` | delete_obsolete | deleted | Obsolete duplicate root entry; current Codex initialization prompt is `prompts/codex/initialize-agentpal-workspace.md`. |

## Candidate Moves, Not Deleted In R161

| File or directory | Category | Proposed action | Reason |
| --- | --- | --- | --- |
| `GITHUB_RELEASE_DRAFT.md` | move_to_evidence_archive | move under release evidence/history | Release working draft, not first-entry docs. |
| `RELEASE_CHECKLIST.md` | move_to_evidence_archive | move under release evidence/history | Release checklist, not product docs. |
| `RELEASE_MANIFEST.md` | move_to_evidence_archive | move under release evidence/history | Release manifest, not user docs. |
| `RELEASE_NOTES.md` | move_to_evidence_archive | move under release evidence/history | Release notes should be linked from releases, not used as start page. |
| `docs/10-using-agentpal-with-claude-code.md` | delete_duplicate / rewrite_required | merge with `docs/04-runtime-guides/` | Duplicates runtime-guide location and must reflect limited Claude evidence. |
| `docs/11-using-agentpal-with-cli-agents.md` | delete_duplicate / rewrite_required | merge with `docs/04-runtime-guides/` | Duplicates runtime-guide location and must avoid unsupported CLI-host claims. |
| `docs/08-release-candidate/` | move_to_evidence_archive | archive | Release-candidate history. |
| `docs/research/` | move_to_evidence_archive | archive | Research/future design material, not current behavior docs. |
| `docs/09-roadmap/` | move_to_evidence_archive | archive | Roadmap material, not current behavior docs. |

## Active Reference Result

After R161 deletion and `RESOURCE_INDEX.md` update, active entry docs do not reference `INIT_PROMPT.md`.

Historical references may remain inside cleanup/evidence records because they document why the old entry was removed.

