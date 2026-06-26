# PBL-007 - Research Report HTML Page

## Category

Composite deliverable.

## User Input

```text
Research 2026 agent trends, write a detailed analysis report, and turn it into a polished HTML page.
```

## Baseline Behavior

A direct assistant may start with research, skip stage ownership, or create a page without source and rendering evidence.

## Expected AgentPal Behavior

The first Pal identifies research, report writing, implementation-shaped page delivery, and verification as separate stages. It names provisional stage owner candidates before broad questions and keeps Runtime as execution layer only.

## Required Assets / Context

- Deliverable-aware judgement gate.
- Contacts / registry.
- Accepted sources or explicit browsing permission.
- Target output path only when execution is authorized.

## Expected Task Judgement

- domain_focus: agent trend research and page delivery.
- content_deliverables: evidence-based report.
- final_deliverables: HTML page.
- stages: research, report structure/copy, page implementation, verification.
- verification_needs: citations, source dates, artifact path, rendered/inspected page evidence, public-safe check.

## Expected Output Shape

- staged judgement;
- stage-level Context Access List sketch;
- focused questions about sources, audience, output language, and write location;
- no execution claim before evidence.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| deliverable_awareness | Treats as only research. | Mentions page but no owner/evidence. | Separates report and HTML artifact stages. |
| owner_judgement | One owner or Runtime owns all. | Candidates lack reason. | Stage candidates are current-case judgements. |
| context_scope_control | Reads all examples or docs. | Some scoped reads. | Uses approved sources and target files only. |
| verification_quality | No citations or page evidence. | Mentions review. | Requires source and rendered/inspected artifact evidence. |
| no_future_as_current | Claims automatic Deep Conductor. | Ambiguous. | Written staged package only. |

## Failure Modes

- A research Pal is assigned the full HTML deliverable.
- Runtime is told to make the page with no Pal-layer implementation judgement.
- The final says "done" without citations or page evidence.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
