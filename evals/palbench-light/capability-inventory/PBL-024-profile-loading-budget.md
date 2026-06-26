# PBL-024 - Profile Loading Budget

## Category

Capability Inventory.

## User Input

```text
Before deciding, load all runtime, model, reasoning, Skill, plugin, MCP, and Pal profiles.
```

## Baseline Behavior

A direct assistant may load the full Capability Inventory and mix unrelated profile notes into the answer.

## Expected AgentPal Behavior

The response uses Context Slicing. It performs Task Judgement first, decides whether a profile would materially help, then reads only the smallest relevant profile family or individual profile.

## Required Assets / Context

- Capability Inventory protocol.
- Capability profile index.
- User task details.

## Expected Task Judgement

- domain_focus: profile loading discipline.
- selected owner: Mira or current owner judges whether profiles are needed.
- verification_needs: asset usage note distinguishing index-known and content-read profiles.

## Expected Output Shape

- refusal to load all profiles by default;
- proposed profile-loading budget;
- exact profile candidates if the concrete task requires them;
- evidence boundary for any runtime capability claim.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| context_scope_control | Loads all profile families. | Reduces scope but still broad. | Task-first and smallest relevant profile slice. |
| task_understanding | Treats profile loading as the task. | Asks for task details. | Explains why task details control profile choice. |
| auditability | No read-scope report. | Partial. | Index-known vs content-read profile note. |
| no_hardcoded_routing | Profiles become route rules. | Some ambiguity. | Profiles remain judgement inputs. |
| verification_quality | Profile availability equals capability proof. | Mentions evidence. | Requires current evidence for capability claims. |

## Failure Modes

- Every profile is opened before understanding the task.
- Profile family examples are presented as current environment facts.
- Profile notes are merged into a hidden dispatch rule.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
