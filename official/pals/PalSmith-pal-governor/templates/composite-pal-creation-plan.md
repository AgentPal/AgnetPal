# Composite Pal Creation Plan Template

Use this template when PalSmith creates a Pal from role, human thinking, voice, knowledge, Skill, plugin, Agent capability, or a combination of these sources.

## 1. Request Summary

- user goal:
- creation mode(s):
- direct creation requested: yes / no
- publication target: private draft / team-local / public example / official candidate / Marketplace candidate
- assumptions:
- minimum follow-up questions:
- follow-up question count:

## 2. Proposed Pal Identity

- Pal name:
- Pal id:
- role:
- served users:
- one-line description:
- not the real person / not rights-holder representative boundary:

## 3. Role Architecture / 岗位职责

- role goal:
- core responsibilities:
- non-responsibilities:
- input materials:
- output deliverables:
- high-risk matters:
- user-confirmation matters:
- daily workflows:
- acceptance criteria:

## 4. Cognitive Distillation / 思维方式

- source type: public figure / authorized expert / book / team material / user document / other
- source scope:
- research cutoff:
- mental models:
- decision heuristics:
- value floor:
- anti-patterns:
- judgement boundaries:
- uncertainty notes:
- target files:
  - `knowledge/mental-models.md`
  - `knowledge/decision-heuristics.md`
  - `knowledge/anti-patterns.md`
  - `identity/source-boundary.md`
  - `evals/cognitive-distillation-tests.md`

## 5. Voice And Personality / 性格与语气

- source type:
- style-inspired boundary:
- personality base:
- emotion style:
- caution level:
- risk preference:
- speech rhythm:
- sentence length:
- common transitions:
- common address forms:
- common words:
- forbidden expressions:
- scenario tone shifts:
- sample dialogue plan:
- target files:
  - `identity/personality.md`
  - `identity/tone.md`
  - `identity/speech-patterns.md`
  - `identity/voice-boundary.md`
  - `evals/voice-consistency-tests.md`

## 6. Knowledge Curation / 岗位知识

- user-provided materials:
- public research needed:
- domain overview:
- base concepts:
- common tasks:
- workflows:
- terms:
- cases:
- error cases:
- risk list:
- sources:
- update time:
- confidence:
- target files:
  - `knowledge/index.md`
  - `knowledge/<topic>.md`
  - `imports/<source-type>/`

## 7. Skill / Plugin / Agent Mapping

- Pal-owned Skills:
- host Runtime Skill candidates:
- plugin candidates:
- external software candidates:
- Agent Runtime candidates:
- strong-model tasks:
- weak-model tasks and prompt-shaping needs:
- evidence required before capability claim:
- target files:
  - `skills/skill-map.md`
  - `plugins/plugin-map.md`
  - `runtime/agent-usage-policy.md`
  - `capabilities/task-routing-matrix.md`
  - `workflows/agent-dispatch-workflows.md`

## 8. Memory Design / 记忆模板

- user preference memory:
- project background memory:
- task history memory:
- decision record memory:
- Skill usage memory:
- Agent dispatch memory:
- retrospective memory:
- privacy confirmation required:
- target files:
  - `memory/README.md`
  - `memory/user-preferences-template.md`
  - `memory/project-memory-template.md`
  - `memory/task-history-template.md`
  - `memory/routing-decisions-template.md`

## 9. Collaboration Boundary / 协作边界

- consult candidates:
- delegation candidates:
- allowed shared information:
- blocked shared information:
- discoverable: yes / no / later
- central contacts candidate: yes / no / later
- consult / delegate / handoff modes:
- target files:
  - `contacts/collaboration-policy.md`
  - `identity/collaboration-boundary.md`

## 10. Evaluation Plan / 质量验证

- role task tests:
- cognitive consistency tests:
- voice consistency tests:
- boundary tests:
- uncertainty tests:
- Skill / Agent recommendation tests:
- Marketplace claim tests:
- target files:
  - `evals/pal-creation-quality-gate.md`
  - `evals/cognitive-consistency-tests.md`
  - `evals/voice-consistency-tests.md`
  - `evals/role-task-tests.md`
  - `evals/boundary-tests.md`

## 11. Marketplace Metadata / Marketplace 元数据

- Pal name:
- one-line introduction:
- target users:
- scenarios:
- included assets:
- capability boundaries:
- source type:
- authorization status:
- public-source inspiration status:
- update plan:
- maintainer:
- version:
- license suggestion:
- risk statement:
- source-type Marketplace boundary:
- public listing allowed: yes / no / requires review
- target files:
  - `marketplace/listing.md`
  - `marketplace/metadata.json`
  - `marketplace/source-disclosure.md`
  - `marketplace/maintenance-plan.md`

## 12. Runtime Task Package Boundary

- allowed write paths:
- forbidden write paths:
- required evidence:
- checks to run:
- not-run items:
- user confirmation needed before writes:

## 13. Completion Decision

- readiness: draft / testing / blocked
- missing information:
- risks:
- next step:
