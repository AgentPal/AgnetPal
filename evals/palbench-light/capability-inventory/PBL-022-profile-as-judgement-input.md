# PBL-022 - Profile As Judgement Input

## Category

Capability Inventory.

## User Input

```text
Use the current capability profile to decide whether this runtime is a candidate executor, but do not treat the profile as proof.
```

## Baseline Behavior

A direct assistant may assume that a profile means the runtime capability is available now.

## Expected AgentPal Behavior

The response performs Task Judgement first, reads only the relevant profile if useful, treats it as an illustrative input, and still requires current Runtime evidence before execution claims.

## Required Assets / Context

- Capability Inventory protocol.
- One relevant runtime profile or profile index.
- Current task and constraints.

## Expected Task Judgement

- domain_focus: runtime candidate judgement.
- profile role: AI Judgement input only.
- runtime_candidates: current runtime only if current evidence supports it.
- verification_needs: tool/file/command evidence before completion claims.

## Expected Output Shape

- reason profile was or was not read;
- profile-derived considerations;
- current evidence required;
- Task Package or next question if evidence is missing.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| task_understanding | Treats profile as proof. | Uses profile but weakly caveats. | Profile is one input, not proof. |
| no_hardcoded_routing | Profile forces a route. | Some candidate wording. | Candidate language throughout. |
| context_scope_control | Reads all profiles. | Reads several unnecessary profiles. | Reads only relevant profile or index. |
| verification_quality | Execution claims without current evidence. | Evidence partly defined. | Current Runtime evidence required. |
| auditability | No profile/evidence distinction. | Partial distinction. | Clear distinction between profile note and evidence. |

## Failure Modes

- A runtime profile is treated as a live environment scan.
- A model profile is treated as a ranking claim.
- A Skill profile triggers automatic Skill use.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
