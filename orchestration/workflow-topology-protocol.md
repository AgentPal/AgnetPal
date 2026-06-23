# Workflow Topology Protocol

Workflow Topology describes possible shapes for organizing Pal, runtime, Skill, and verification work.

AgentPal v0.1.0-rc.1 only uses Simple Pal Mode. The active shapes are Fast Route, Single Owner, and Task Package. Deep Conductor topologies are future design only.

See also:

- `orchestration/fast-route-protocol.md`
- `orchestration/deep-conductor-protocol.md`

## Topologies

| Topology | v0.1 Active | Summary |
| --- | --- | --- |
| Fast Route | Yes | Mira chooses an owner or answers secretary work quickly |
| Single Owner | Yes | One owner Pal answers in the same response |
| Task Package | Yes | Pal compresses work for an execution runtime |
| Owner + Verifier | Future | Owner produces, verifier reviews evidence |
| Plan -> Execute -> Verify | Future | Planner prepares, runtime executes, verifier checks |
| Parallel Independent Review | Future | reviewers work independently before summary |
| Sequential Chain | Future | staged handoff from research to product to development to QA |
| Best-of-N Runtime | Future | multiple runtimes produce candidates, verifier compares |
| Secretary Summary | Yes | Mira summarizes completed or provided results |

## Fast Route

Suitable when:

- task is clear
- risk is low
- one Pal can own it
- no extra verification workflow is needed

Inputs:

- user goal
- contacts / registry
- selected owner assets

Outputs:

- direct answer, short handoff, or compact task package

Isolation:

- no other Pal drafts are loaded by default

Verification:

- evidence requested only when task claims execution or completion

## Single Owner

Suitable when:

- one registered Pal can reasonably own the output
- the user expects a professional answer
- the context slice is bounded

Not suitable when:

- independent verification is required
- multiple conflicting perspectives are materially useful

v0.1 active: yes.

## Owner + Verifier

Suitable when:

- acceptance evidence matters
- false completion risk is meaningful
- release, safety, or quality gate review is needed

v0.1 active: no. It can be described as a future workflow or represented manually in a Task Package.

## Plan -> Execute -> Verify

Suitable when:

- work requires file edits, commands, or external execution
- planning and execution evidence should be separated

v0.1 active: no automated topology. The plan can be written as a Task Package.

## Parallel Independent Review

Suitable when:

- disagreement is useful
- anchoring risk is high
- product, implementation, quality, or research perspectives should be independently assessed

Context isolation:

- each reviewer receives its own Context Access List
- reviewers do not read each other's drafts before submission

v0.1 active: no.

## Sequential Chain

Suitable when:

- output naturally moves through staged judgement
- each stage consumes only the previous stage's accepted output

v0.1 active: no.

## Best-of-N Runtime

Suitable when:

- high-risk tasks justify extra cost
- multiple runtimes are available
- a verifier can compare evidence

v0.1 active: no. Do not call external runtimes from AgentPal v0.1.

## Secretary Summary

Suitable when:

- multiple results are already provided
- user asks for a digest, status, next actions, or final report

v0.1 active: yes, as Mira-owned secretary work.
