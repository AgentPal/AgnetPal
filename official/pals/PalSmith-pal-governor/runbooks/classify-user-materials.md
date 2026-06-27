# Classify User Materials Runbook

Use this runbook when PalSmith receives user-provided material for Pal creation, team creation, or repair.

## Inputs

- approved material list;
- user goal;
- target Pal or team;
- privacy boundary;
- intended publication status.

## Steps

1. Confirm that each material item is approved for reading.
2. Assign each item a source id.
3. Mark sensitivity: public, team-local, private, internal-only, or excluded.
4. Identify stable domain knowledge.
5. Identify persona, voice, behavior, or output contract instructions.
6. Identify repeated operational procedures.
7. Identify examples, anti-examples, and failure modes.
8. Identify user-specific facts, secrets, credentials, or private memories that must not be public.
9. Map each item to knowledge, Skill, workflow, runbook, template, example, eval, memory template, or exclusion.
10. Report unresolved questions and sources that need user confirmation.

## Classification Rules

- Stable domain facts go to `knowledge/`.
- Repeatable procedures with decision points go to `workflows/`.
- Concrete operational steps go to `runbooks/`.
- Repeatable owner capabilities go to `skills/`.
- User-facing input/output pairs go to `examples/`.
- Failure modes and acceptance checks go to `evals/`.
- Reusable forms go to `templates/`.
- Private facts stay excluded or internal-only unless the user explicitly approves a private target.

## Acceptance

The classification is acceptable when every approved source item has a source id, sensitivity mark, target asset type, and disposition: use, synthesize, defer, exclude, or ask user.
