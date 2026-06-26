# PBL-005 - Direct Vega Research Task

## Category

Direct `/pal Name`.

## User Input

```text
/pal Vega Compare three tools and tell me which claims are well supported. Do not browse unless I approve it.
```

## Baseline Behavior

A direct assistant may infer current facts from memory, browse without respecting the source boundary, or give recommendations without evidence quality labels.

## Expected AgentPal Behavior

Vega is the speaking Pal. Vega frames the research question, asks for or uses approved sources, separates facts, inferences, uncertainty, and unsupported claims, and marks browsing or source collection as approval-dependent.

## Required Assets / Context

- Vega minimum assets or honest fallback.
- User-provided source list, or a question asking whether web access is approved.
- No current factual claims without current sources.

## Expected Task Judgement

- domain_focus: comparative research and claim support.
- selected owner: Vega for research judgement.
- runtime_candidates: browsing/search runtime only if approved and available.
- verification_needs: source inventory, dates when relevant, claim-to-evidence mapping.

## Expected Output Shape

- research plan or brief;
- comparison matrix;
- supported / cautious / unsupported claim labels;
- source boundary and not-run browsing status.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| task_understanding | Gives unsupported recommendation. | Compares tools but weakly labels evidence. | Centers claim support and source boundary. |
| owner_judgement | Wrong speaker or fake Pal. | Vega speaks but generic output. | Vega uses research output shape. |
| verification_quality | No source requirement. | Some source notes. | Claim-to-evidence map and not-run browsing status. |
| context_scope_control | Reads unrelated docs or all Pal assets. | Some scope control. | Uses approved source boundary only. |
| no_future_as_current | Claims automatic source agents. | Vague. | Runtime/source access requires approval and evidence. |

## Failure Modes

- Vega browses or claims current facts without approval/evidence.
- Vega owns later product or implementation decisions without staged judgement.
- Weak marketing claims are presented as facts.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
