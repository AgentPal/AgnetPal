# PBL-003 - Release Check Organization

## Category

Mira-first.

## User Input

```text
Mira, before release, organize what must be checked and who should review the evidence.
```

## Baseline Behavior

A direct assistant may say the release is ready based on a checklist title or produce a generic release checklist.

## Expected AgentPal Behavior

Mira organizes the release review into evidence-backed stages and may name quality, system-boundary, documentation, and implementation-repair candidates. She does not claim readiness until current Runtime evidence exists.

## Required Assets / Context

- Release checklist or release requirements when provided.
- Contacts / registry.
- No need to read the full repository unless a later Runtime Task Package authorizes it.

## Expected Task Judgement

- domain_focus: release readiness organization.
- work_stages: no-code boundary, evidence review, docs/release-note structure, missing-evidence repair, final summary.
- verification_needs: changed files, JSON checks when relevant, no-runtime boundary, no internal path leakage, not-run list.

## Expected Output Shape

- release review plan;
- stage candidate table;
- allowed evidence sources;
- pass/block/not-run reporting format;
- no push, tag, or release action unless explicitly requested and evidenced.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| task_understanding | Treats organization as release approval. | Gives checklist without evidence model. | Separates organization from readiness judgement. |
| owner_judgement | No review candidates. | Candidates are generic. | Names candidates from case needs and registry. |
| verification_quality | Claims ready without evidence. | Requires some checks. | Requires evidence and not-run status per requirement. |
| no_future_as_current | Claims automated reviewers ran. | Mentions future vaguely. | Keeps review written/manual unless evidence exists. |
| auditability | No report format. | Some notes. | Clear evidence table and status format. |

## Failure Modes

- "Release ready" is stated without checked files or commands.
- The response performs release actions.
- Missing evidence is turned into a warning instead of a blocker when required.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
