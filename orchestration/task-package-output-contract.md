# Task Package Output Contract

Task Packages compress Pal judgement into a form that a bottom-layer Agent / Runtime can execute or verify.

## When To Use

Use a Task Package when:

- the user asks to hand work to an Agent / Runtime
- a Pal creates implementation, review, verification, file, system, or document work for execution
- a multi-Pal result needs a compact next action
- the user asks "make this actionable"
- the current Main Pal or owner Pal identifies a composite deliverable that needs staged work

## Required Shape

```text
Task Package
- Goal
- Domain focus
- Deliverables
  - Content deliverables
  - Final deliverables
- Context summary
- Relevant files / assets
- Asset loading note, including index-known versus content-read when relevant
- Owner Pal perspective
- Work stages
  - Stage goal
  - Capability needs
  - Pal / Runtime / Skill candidates
  - Context Access List summary
  - Verification needs
- Constraints
- Steps
- Output format
- Acceptance criteria
- Risks
- Do not do
- Evidence required
```

## Pal Contributions

Nova may provide:

- product goal
- user scenario
- scope
- Must / Should / Won't
- constraints

Atlas may provide:

- implementation plan
- file scope
- commands or checks
- technical steps
- acceptance criteria

Quinn may provide:

- quality gates
- tests
- failure conditions
- release risks

Rhea may provide:

- environment constraints
- read-only checks
- system risk
- evidence requirements

Morgan may provide:

- file/document scope
- naming and batch rules
- privacy constraints
- output artifacts

Harper may provide:

- audience and tone
- draft structure
- review criteria
- publication constraints

Vega may provide:

- research question
- source requirements
- evidence table needs
- uncertainty flags

Mira may provide:

- compression
- owner/consultant labels
- overall conductor framing
- user-facing next action
- final merged task package

Any current owner Pal may provide:

- deliverable-aware Task Judgement before accepting a composite task
- the stages it can own
- stage candidates for work outside its responsibility
- a recommendation to keep or return Mira as overall Conductor

Candidate labels are not routes. The package must not contain keyword-trigger rules or task/domain -> fixed Pal mappings.

## Evidence Rule

The Task Package must define what evidence would prove completion. A completion claim without evidence remains unverified.

If a Runtime will execute an implementation stage, the Task Package must describe the Pal-layer judgement that produced that implementation request. Do not state that the Runtime simply takes over the remaining stage after a content Pal finishes.
