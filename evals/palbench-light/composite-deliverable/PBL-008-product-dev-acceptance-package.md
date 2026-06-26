# PBL-008 - Product Dev Acceptance Package

## Category

Composite deliverable.

## User Input

```text
Turn this product idea into requirements, a development task package, and acceptance criteria.
```

## Baseline Behavior

A direct assistant may merge product scope, implementation instructions, and quality gates into one generic plan.

## Expected AgentPal Behavior

The first Pal separates product framing, development package, and acceptance/verification. Candidate owners are selected from current context and registry, not from static task categories.

## Required Assets / Context

- Product idea.
- Contacts / registry.
- Relevant product, implementation, and quality output contracts only if those stages are being expanded.

## Expected Task Judgement

- domain_focus: product idea to executable and verifiable package.
- stages: product requirements, implementation package, acceptance review.
- verification_needs: requirements traceability, file/check evidence if execution happens, pass/fail criteria.

## Expected Output Shape

- product brief fields;
- implementation Task Package fields;
- acceptance criteria and evidence table;
- clear separation of owner candidates and Runtime execution.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| task_understanding | Gives one vague roadmap. | Covers two of three outputs. | Covers requirements, dev package, and acceptance. |
| deliverable_awareness | No stage separation. | Stage labels but weak ownership. | Clear stage ownership and deliverables. |
| task_package_quality | Cannot execute. | Partially actionable. | Development package is bounded and verifiable. |
| verification_quality | No acceptance evidence. | Acceptance criteria vague. | Criteria are testable with evidence. |
| no_hardcoded_routing | Static route wording. | Some candidate phrasing. | Case-specific candidates only. |

## Failure Modes

- Product recommendations become implementation commands without accepted scope.
- Acceptance criteria are generic "looks good" statements.
- The response makes one Pal the permanent owner of all product-to-dev work.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
