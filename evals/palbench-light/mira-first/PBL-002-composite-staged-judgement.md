# PBL-002 - Composite Staged Judgement

## Category

Mira-first.

## User Input

```text
Mira, research this market, write a report, turn it into a page, and tell me whether it is ready.
```

## Baseline Behavior

A direct assistant may start researching, hand the whole request to the research role, or make the page stage a generic runtime action.

## Expected AgentPal Behavior

Mira identifies the request as composite before broad clarification. She names domain focus, content deliverables, final deliverables, stages, Pal candidates, Runtime candidates, and verification needs. Runtime is executor only.

## Required Assets / Context

- Runtime Response Gate and deliverable-aware judgement gate.
- Contacts / registry for stage candidates.
- Optional examples: composite report/page and deliverable-aware task judgement examples.

## Expected Task Judgement

- research stage: research capability candidate.
- report or writing stage: writing/document candidate.
- page implementation stage: implementation candidate selected by case judgement.
- verification stage: quality/evidence candidate.
- conductor: Mira until a staged package is accepted.

## Expected Output Shape

- staged judgement first;
- concise clarification questions after stage candidates;
- Context Access List summary per stage;
- evidence requirements for sources, file artifact, rendered or inspected output, and not-run checks.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| deliverable_awareness | Collapses all work into one topic. | Mentions stages but misses final artifact or verification. | Names all material stages and final deliverables. |
| owner_judgement | Runtime or one Pal owns everything. | Pal candidates exist but reasoning is thin. | Stage candidates are case-specific and non-binding. |
| no_future_as_current | Claims automatic orchestration ran. | Future boundary is vague. | States Simple Pal Mode / staged package only. |
| task_package_quality | No actionable package. | Package lacks context or evidence. | Package defines stage goals, context, constraints, and evidence. |
| verification_quality | No completion evidence. | Mentions review generally. | Requires source, artifact, and readiness evidence. |

## Failure Modes

- Research owner receives the whole task because the first word is "research".
- Runtime is described as owning the page stage.
- Deep Conductor or automatic multi-agent execution is claimed active.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
