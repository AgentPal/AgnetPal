# PalSmith E2E Creation Self-Test

This self-test checks whether PalSmith can guide a user from goal or material bundle to Pal or AI team draft, evidence review, repair, and first use while staying inside the no-code Pal layer boundary.

## Test Method

Run these as Markdown review cases. If a check cannot be performed in the current runtime, mark it `not-run` with the blocker. Do not treat missing evidence as pass.

## Required R40 Test Cases

| id | R40 requirement | expected result |
| --- | --- | --- |
| E2E-01 | Create Pal from user goal | PalSmith identifies a single professional Pal path and asks focused clarification questions. |
| E2E-02 | Create Pal from user materials | PalSmith classifies approved materials into identity, knowledge, Skills, workflows, runbooks, examples, evals, memory templates, or exclusion before proposing assets. |
| E2E-03 | Create AI team from user goal | PalSmith identifies an AI team path, capability domains, and a bounded roster. |
| E2E-04 | Generated Pal is not an empty shell | The Pal draft contains job-specific identity, output contract, knowledge, Skills, workflows or runbooks, examples, and evals. |
| E2E-05 | Generated team is not only names and roles | The team draft includes leader/Main Pal boundary, collaboration rules, context rules, task examples, member non-roles, and team evals. |
| E2E-06 | `pal.json` must be legal | Every created or edited `pal.json` is parseable JSON and matches the declared Pal identity. |
| E2E-07 | No fixed routing | The output contains no fixed collaborator, keyword trigger, or permanent domain route except as a prohibition or failure example. |
| E2E-08 | No Skill-as-Pal mistake | The output does not register or describe ordinary Skills, tools, models, repositories, or knowledge packs as Pals. |
| E2E-09 | No sensitive information leakage | Private, excluded, or internal-only material is not written into public assets or public examples. |
| E2E-10 | Must output health check | The result includes Pal or AI team health status with pass / risk / fail / not-run evidence. |
| E2E-11 | Must output repair package | The result includes issue list, risk level, suggested files, runtime repair task package, and acceptance criteria when gaps remain. |
| E2E-12 | Must give user next usage path | The result includes realistic `/pal <Name> ...` or team entry usage examples and expected output shape. |
| E2E-13 | Must state no-code boundary | The result states PalSmith plans and judges while the current runtime executes approved file operations with evidence. |
| E2E-14 | Must generate Runtime Task Package | The result includes allowed reads, allowed writes, forbidden writes, user confirmation, evidence, and acceptance criteria. |

## Additional Boundary Checks

| id | check | expected result |
| --- | --- | --- |
| B-01 | Release boundary | Public docs do not claim PalSmith is a CLI, scanner, validator, auto publisher, active Deep Conductor, active multi-agent runtime, or automatic capability probe. |
| B-02 | Source preservation | Source inventory, sensitivity marks, coverage, uncertainty, and excluded/private material handling are present. |
| B-03 | Repeated workflow conversion | Repeated operations become runbooks, workflows, or Skills according to asset purpose. |

## Failure Cases

PalSmith fails the self-test if it:

- skips clarification when essential scope is missing;
- creates a Pal with only headings and no job-specific content;
- creates a team with only names and role titles;
- treats private material as public;
- registers contacts or registry inside the first creation package;
- presents current v0.2 as active multi-agent execution;
- creates fixed dispatch rules;
- labels a draft publish-ready without evidence;
- says checks passed when they were not run.

## Required Evidence

- paths of reviewed task packages, workflows, runbooks, examples, and templates;
- explicit pass / fail / not-run result per case;
- JSON parse result when created or edited JSON is involved;
- no-code boundary review for changed files;
- hardcoded routing review with hits explained as prohibitions or failures;
- public path leakage review.

## Result Template

| case id | result | evidence | repair |
| --- | --- | --- | --- |
| E2E-01 | pass / fail / not-run |  |  |

Overall readiness:

- ready for first implementation:
- blocked by:
- repair package:
