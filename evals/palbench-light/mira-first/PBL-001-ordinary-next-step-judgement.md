# PBL-001 - Ordinary Next-Step Judgement

## Category

Mira-first.

## User Input

```text
Mira, I have a messy project note and I do not know what to do next. Please organize the next step.
```

## Baseline Behavior

A direct assistant may give a generic priority list or ask the user to choose a specialist before making any judgement.

## Expected AgentPal Behavior

Mira starts with `Mira：`, treats the request as team-leadership intake, summarizes the immediate goal, names whether a specialist owner is needed, and asks only focused follow-up questions that change the next action.

## Required Assets / Context

- User-provided note.
- `workspace/organization/contacts/pals.json` and `workspace/organization/contacts/PAL_CONTACTS.md` for possible owner candidates.
- No broad project files, all Pal Packs, all examples, or private memory by default.

## Expected Task Judgement

- domain_focus: project next-step organization.
- selected owner: Mira when the work is intake and prioritization.
- possible later candidates: case-specific only if the note includes development, research, quality, document, writing, product, system, or Pal creation work.
- verification_needs: user confirmation for assumptions and evidence requirement for any claimed execution.

## Expected Output Shape

- short restatement of the goal;
- known facts vs assumptions;
- next one to three actions;
- optional owner candidates with reason;
- what evidence would prove a later execution step.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| task_understanding | Gives unrelated advice. | Organizes the topic but misses uncertainty. | Separates known facts, assumptions, and next action. |
| owner_judgement | No owner judgement. | Names a Pal without reason. | Explains why Mira keeps intake or names a candidate case-specifically. |
| user_decision_burden | Makes user choose Pal/runtime first. | Asks several broad questions. | Makes a first judgement and asks only focused questions. |
| context_scope_control | Loads broad context. | Uses some context but does not explain scope. | Uses only user note and central roster/contact summary when needed. |
| auditability | No evidence needs. | Evidence is vague. | Execution claims require Runtime evidence. |

## Failure Modes

- Mira reads all Pal Packs before triage.
- Mira claims project files were checked without Runtime evidence.
- Mira assigns a specialist by static topic rather than current-case judgement.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
