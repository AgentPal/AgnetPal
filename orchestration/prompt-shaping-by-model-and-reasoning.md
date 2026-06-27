# Prompt Shaping By Model And Reasoning

This no-code guide helps a Conductor shape task packages for model and reasoning candidates.

It is prompt shaping, not an automatic model selector. Model and reasoning entries are candidates. The host Runtime or user selects the actual model, reasoning strength, budget, and permissions.

## Strong / High Reasoning Candidate

Suitable for:

- ambiguous goals;
- multi-stage Deep Conductor planning;
- release readiness;
- failure repair;
- conflict synthesis;
- privacy or safety sensitive work;
- verification design;
- cross-runtime continuation with stale or partial memory.

Prompt features:

- include goal, constraints, stage owners, alternatives rejected, and risk;
- include exact evidence requirements;
- include Context Budget Plan and max read tier;
- include forbidden context;
- include verification plan and stop conditions;
- request explicit uncertainty, blockers, and not-run items.

## Medium / Medium Reasoning Candidate

Suitable for:

- bounded documentation changes;
- ordinary Context Packet or Runtime Task Package generation;
- source summaries with clear scope;
- straightforward multi-file consistency checks;
- normal Project Conductor next-round packages.

Prompt features:

- provide selected files or summaries;
- name expected output fields;
- include acceptance criteria;
- include moderate verification requirements;
- ask for a Context Usage Report.

## Economy / Weak / Low Reasoning Candidate

Suitable for:

- narrow edits;
- checklist completion;
- structured extraction from known files;
- low-risk formatting;
- execution of a highly specified package.

Prompt features:

- provide exact file boundaries;
- provide step-by-step instructions;
- forbid unrelated reads and edits;
- include concrete acceptance criteria;
- include final report fields;
- include examples of pass / fail / not-run wording;
- avoid vague open-ended strategy questions.

Weak or low reasoning candidates should not receive vague, high-risk, multi-stage, or under-specified tasks. If the task remains ambiguous, increase reasoning candidate or improve the package first.

## Verification

Prompt shaping must not remove verification. If verification is costly, write the verification cost reason and select the smallest sufficient evidence path.

## Boundary

This guide does not call models, change runtime settings, calculate cost, or meter tokens. It only prepares better no-code instructions for a host Runtime.
