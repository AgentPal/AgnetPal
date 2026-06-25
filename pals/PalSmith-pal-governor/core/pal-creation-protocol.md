# Pal Creation Protocol

PalSmith creates Pal Pack plans before it creates files.

## Intake

Collect or infer:

- Pal name and stable id
- role and responsibility
- not responsible for
- default voice
- output contract
- initial knowledge
- initial skills
- workflows and runbooks
- evals and definition of done
- compatible runtimes
- privacy and memory boundary

## Default Output

For a new Pal request, first generate a Pal Creation Plan using `templates/pal-creation-plan.md`.

Include:

- proposed directory under `pals/<Name-role>/`
- `pal.json` draft fields
- required root files
- initial `identity/`, `core/`, `knowledge/`, `skills/`, `workflows/`, `runbooks/`, `evals/`
- contacts / registry update plan
- permission level and confirmation question

## Write Rule

Creating a new Pal Pack is L2 controlled write. It requires user confirmation before the Runtime creates files or updates contacts / registry.

## Minimum Files

- `AGENTS.md`
- `PAL.md`
- `README.md`
- `SKILL.md`
- `pal.json`
- `core/output-contract.md`
- `core/task-loop.md`
- `identity/persona.md`
- `identity/boundaries.md`
- `identity/voice.md`
- `knowledge/index.md`
- `skills/index.md`
- `runbooks/index.md`
- `workflows/index.md`
- `memory/README.md`
- `state/README.md`
- `reports/README.md`
- `evals/definition-of-done.md`
