# Create First Professional Pal Task Package

task_name: Create First Professional Pal
owner_pal: PalSmith
executing_runtime: current Agent Runtime
status: copyable template

## User Fill Area

```text
Requested Pal job:
Problem the Pal should solve:
Target users:
Professional domain:
3-5 example tasks:
Tasks this Pal must not do:
Output language:
Preferred tone:
Source materials approved for reading:
Sensitive or private materials:
Collaboration needed: none / consult existing Pals / future team candidate
Target write path:
Public, team-local, or private use:
Preparing for publish: yes / no / later
Optional external research allowed: yes / no
May the runtime write files after showing the path list: yes / no
```

## Goal

Create a first professional Pal Pack draft from a user goal and approved materials. The result must be useful enough for a first `/pal <Name> ...` call, but it does not automatically register the Pal in contacts or registry.

## Required Inputs

- user goal and target job;
- problem to solve and professional domain;
- target users and recurring scenarios;
- output language and tone;
- collaboration expectation;
- responsibility and non-responsibility boundaries;
- user-approved source materials;
- privacy and publication boundary;
- target write path;
- explicit confirmation before writes.

## Allowed Reads

- current Pal Pack standard docs;
- PalSmith Pal creation, material ingestion, and health-check assets;
- approved user materials only;
- approved reference Pal Packs when the user wants style or structure alignment.

## Allowed Writes

- approved new Pal directory;
- draft root files such as `PAL.md`, `pal.json`, `SKILL.md`, `README.md`;
- owner Pal `core/`, `knowledge/`, `skills/`, `workflows/`, `runbooks/`, `templates/`, `examples/`, and `evals/` assets as needed;
- creation report inside the approved target directory.

## Forbidden Writes

- `contacts/`;
- `registry/`;
- unrelated Pal directories;
- runtime source code, scripts, installers, scanners, validators, or package manifests;
- private memory, credentials, personal notes, or unapproved source files.

## PalSmith Steps

1. Restate the user goal, expected deliverable, and privacy boundary.
2. Ask only missing high-impact clarification questions.
3. Propose a Pal name, id, directory, and call example.
4. Define job scope, non-scope, target users, and first use cases.
5. Classify user materials into identity, knowledge, skills, workflows, runbooks, templates, examples, evals, and private or excluded material.
6. Draft the root Pal files and output contract plan.
7. Draft job-specific knowledge, Skills, workflows, runbooks, examples, and evals with real content, not placeholders.
8. Prepare the runtime write list and forbidden write list for confirmation.
9. Review runtime evidence after execution: changed files, parse results, skipped files, and not-run checks.
10. Produce health status, repair package when needed, and first usage examples.

## Prohibitions

- Do not register the Pal in contacts or registry inside this package.
- Do not claim PalSmith executed file operations.
- Do not create a CLI, UI, scanner, validator, importer, exporter, daemon, or installer.
- Do not turn a Skill, tool, model, raw repo, or knowledge bundle into a Pal.
- Do not include private source material in public examples.
- Do not create permanent route rules or fixed natural-language dispatch.

## Expected Evidence

- approved target path;
- files created, changed, skipped, and not found;
- `pal.json` parse result;
- list of source materials used and excluded;
- sensitivity marks for generated assets;
- not-run checks;
- final health-check result;
- repair package when the health check is not clean.

## Acceptance Criteria

- The Pal has a clear job, target user, responsibility boundary, and non-responsibility boundary.
- `pal.json` is parseable and matches the draft identity.
- Root files and output contract are present.
- Knowledge, Skills, workflows, runbooks, examples, and evals contain scenario-specific content.
- User material is traceable to generated assets.
- Private and internal-only material is not leaked into public files.
- The result includes at least three realistic `/pal <Name> ...` usage examples.
- The result is labeled `idea`, `draft`, `testing`, `stable`, `publish-ready`, or `not ready` with evidence.
