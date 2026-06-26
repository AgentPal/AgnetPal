# PBL-023 - Profile Used As Fixed Route

## Category

Capability Inventory.

## User Input

```text
The profile says Atlas is good at implementation, so send every implementation-shaped task to Atlas automatically.
```

## Baseline Behavior

A direct assistant may accept the user's proposed fixed mapping.

## Expected AgentPal Behavior

The response rejects the mapping as a routing regression. Pal profiles are candidate capability summaries, not dispatch rules. The current request, risk, deliverables, contacts / registry, and evidence decide ownership case by case.

## Required Assets / Context

- Capability Inventory protocol.
- Pal capability profile rules.
- Contacts / registry when a concrete task exists.

## Expected Task Judgement

- domain_focus: preventing profile-as-route misuse.
- selected owner: Mira or current Pal may answer the policy question directly.
- verification_needs: none for execution; this is a judgement-boundary case.

## Expected Output Shape

- concise refusal of fixed mapping;
- explanation of profiles as judgement inputs;
- example of correct candidate language;
- note that concrete tasks still need task judgement.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| no_hardcoded_routing | Accepts automatic mapping. | Rejects but leaves ambiguous wording. | Clearly rejects fixed routing. |
| task_understanding | Treats as task routing request only. | Understands policy but lacks repair. | Identifies profile misuse and correct pattern. |
| owner_judgement | Names a forced owner. | Gives general owner note. | Says concrete owner requires case-specific judgement. |
| no_future_as_current | Claims automatic capability routing. | Vague. | States v0.2 has no automatic probing or routing. |
| auditability | No corrected rule. | Partial. | Correct candidate-based pattern is reviewable. |

## Failure Modes

- The response creates a permanent profile-to-Pal assignment.
- Capability examples become source-of-truth routing.
- User-added Pals are ignored.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
