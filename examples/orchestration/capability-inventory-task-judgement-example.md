# Capability Inventory Task Judgement Example

This example shows Capability Inventory used as a minimal AI Judgement input. It does not activate automatic scanning, model switching, Skill invocation, or Deep Conductor.

## User Task

"Mira, help me judge whether this task fits the current Runtime or needs a more detailed Task Package."

## Task Judgement

- domain_focus: runtime execution readiness.
- deliverables: candidate judgement and compact Task Package.
- work_stages:
  - intake: Mira candidate for task framing.
  - runtime capability check: read one Runtime Profile only if execution is being considered.
  - owner/stage candidate check: read one Pal Capability Profile only if a specialist stage appears.
  - package: produce Task Package with evidence needs.
- capability_needs: runtime capability, permission boundary, Pal ownership, verification evidence.
- runtime_candidates: current Runtime only if current permissions and evidence support it.
- profile_candidates: one relevant runtime profile, one relevant Pal profile, and optionally one reasoning profile.
- verification_needs: current runtime evidence, allowed paths, not-run checks.

## Minimal Profiles Read

For this task, Mira reads only:

- `capabilities/runtime-profiles/codex.example.json` if the current runtime is Codex-like.
- `capabilities/pal-profiles/mira-main.example.json` because Mira is conducting intake.
- `capabilities/reasoning-profiles/reasoning-strengths.example.json` only if the task risk requires reasoning-level guidance.

Mira does not read all Runtime, Model, Skill, Plugin, MCP, or Pal profiles.

## Why These Profiles Are Candidates

- The runtime profile may help identify whether file reads, writes, commands, and evidence are plausible in a Codex-like environment.
- The Mira profile may help confirm that Mira can conduct the judgement but should not replace specialist owners.
- The reasoning profile may help shape prompt depth when the task is ambiguous or evidence-heavy.

These profiles are illustrative. They do not prove current environment capability.

## Output Task Package

Task Package:

- Goal: decide whether the task can proceed with current Runtime evidence or needs a detailed package.
- Context summary: user asks for runtime suitability judgement.
- Relevant profiles read: one runtime profile, one Pal profile, optional reasoning profile.
- Candidate judgement: current Runtime may be a candidate if it can provide file/command evidence now.
- Constraints: no automatic scan; no fixed route; no execution claim without evidence.
- Steps: ask for target files if missing, define allowed reads/writes, list required checks, mark not-run items.
- Acceptance criteria: candidate reasoning is explicit, profile use is minimal, Runtime evidence is required before completion.

## Good Response Pattern

Mira says the profile suggests what to check, then asks for or uses current Runtime evidence before claiming capability.

## Bad Response Pattern

Mira says a runtime profile exists, so the Runtime should execute the task immediately.

## Notes

- Profiles are AI Judgement inputs, not fixed routes.
- Current v0.2 does not auto-detect profiles.
- Current v0.2 does not auto-run Deep Conductor.
