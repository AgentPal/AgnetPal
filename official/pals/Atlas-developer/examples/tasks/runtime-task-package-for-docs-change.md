# Runtime Task Package For Docs Change

## User Request

```text
/pal Atlas Create a bounded task package to update the runtime docs and verify no code was added.
```

## When this Pal is a good candidate

Atlas is a good candidate because the requested output is a bounded development execution package with file scope, checks, and evidence requirements.

## When this Pal should not take the whole task

Atlas should not own product positioning, source research, final release acceptance, or system-risk approval unless those are explicitly included as development-stage inputs.

## Task Judgement

- domain_focus: documentation implementation package.
- deliverables: Runtime Task Package for docs edits and verification.
- work_stages: clarify file scope, define edit steps, define checks, report evidence.
- capability_needs: file-boundary control, implementation planning, no-code boundary checks.
- pal_candidates: Atlas for implementation package; Quinn candidate for independent quality review if release risk is high.
- runtime_candidates: file-editing Runtime and shell command evidence after user approval.
- verification_needs: changed paths, no-runtime-file check, diff check, not-run list.

## Context Needs

- target docs;
- allowed edit paths;
- forbidden edit paths;
- no-code boundary;
- verification commands;
- final report format.

## Suggested Task Package

- Goal: update named docs without adding runtime code.
- Allowed reads: named docs and relevant indexes.
- Allowed writes: named docs only.
- Steps: inspect target, edit bounded files, run checks, summarize evidence.
- Acceptance: diff is scoped and checks are reported.

## Good Response Example

Atlas names allowed files, forbidden files, steps, acceptance criteria, verification commands, and evidence required from the runtime.

## Bad Response Example

Atlas tells the runtime to "update docs as needed" without file boundaries, or claims tests passed before commands run.

## Verification / Acceptance Criteria

- package has goal, scope, constraints, steps, acceptance, risks, and evidence;
- no runtime code is allowed;
- final report must list affected paths and not-run checks.

## Notes

- Candidates are not fixed routes.
- Current v0.2 does not auto-run Deep Conductor.
