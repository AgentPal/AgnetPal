# Completion Report Dev Acceptance Repair

## User Request

"The completion report says docs changed, but I do not see a no-code check or diff summary. Repair the dev acceptance package."

## When this Pal is a good candidate

Atlas is a good candidate because the user asks for development acceptance repair: missing checks, file boundaries, and evidence requirements.

## When this Pal should not take the whole task

If the user wants independent pass/fail judgement, Quinn should be a verifier candidate. Atlas can prepare the repair package but should not overclaim final acceptance.

## Task Judgement

- domain_focus: development acceptance repair.
- deliverables: missing-evidence list and rerun package.
- work_stages: compare requirements to evidence, define missing commands, prepare report format.
- capability_needs: implementation evidence, check planning, file-scope reasoning.
- pal_candidates: Atlas for repair package; Quinn for acceptance review candidate.
- runtime_candidates: shell-capable Runtime for diff/check commands.
- verification_needs: command output, changed-file list, failure/not-run status.

## Context Needs

Need original requirements, completion report, changed-file list, and available check commands. Do not infer checks that were not run.

## Suggested Task Package

- Goal: repair the acceptance evidence package.
- Steps: list missing evidence, run or mark checks, update report, identify risk.
- Output: evidence table with pass/fail/not-run.

## Good Response Example

Atlas lists the missing no-code scan and diff check, gives exact commands or manual checks, and asks the Runtime to return outputs.

## Bad Response Example

Atlas edits the completion report to sound confident without actually collecting evidence.

## Verification / Acceptance Criteria

- Missing development evidence is explicit.
- Any unperformed check is labeled `not-run`.
- The repair package can be executed by a Runtime without broad file reads.

## Notes

- Candidates are not fixed routes.
- Current v0.2 does not auto-run Deep Conductor.
