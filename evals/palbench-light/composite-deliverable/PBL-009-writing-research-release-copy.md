# PBL-009 - Writing Research Release Copy

## Category

Composite deliverable.

## User Input

```text
Check the source facts, rewrite the announcement, and prepare release copy that does not overclaim.
```

## Baseline Behavior

A direct assistant may write polished copy first and soften or remove uncertainties.

## Expected AgentPal Behavior

The first Pal separates source review, writing/editing, and release claim verification. The response preserves uncertainty and makes unsupported claims visible.

## Required Assets / Context

- Source facts or source list.
- Announcement draft.
- Release claim boundaries.
- No unrelated release files unless explicitly needed.

## Expected Task Judgement

- domain_focus: source-grounded release writing.
- stages: evidence review, copy rewrite, claim-safety verification.
- verification_needs: source-to-claim mapping and blocked/unsupported claims.

## Expected Output Shape

- stage candidates;
- source-safe rewrite package;
- claim table: supported / cautious / unsupported;
- final copy only after source boundaries are clear.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| task_understanding | Writes copy without checking facts. | Checks facts but weakly preserves uncertainty. | Makes source facts and claim safety central. |
| deliverable_awareness | No stage separation. | Two stages only. | Source, writing, and verification stages are explicit. |
| verification_quality | Unsupported claims remain. | Some claims flagged. | Claim support is mapped and unsafe claims are blocked. |
| context_scope_control | Reads broad release assets. | Uses some relevant docs. | Reads only provided sources/draft unless expanded. |
| auditability | No source trace. | Partial trace. | Clear source-to-claim table. |

## Failure Modes

- Polished copy invents metrics or removes limitations.
- The writer owns source verification without evidence.
- Release readiness is claimed from copy quality alone.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
