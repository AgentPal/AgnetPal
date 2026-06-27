# Pal Health Check Runbook

Use this runbook after creating, importing, repairing, or preparing to publish a Pal.

## Inputs

- target Pal path;
- user goal or declared job;
- files changed or inspected;
- runtime evidence;
- privacy and publication boundary.

## Checks

1. `PAL.md` states a clear job, target user, responsibility boundary, and non-responsibility boundary.
2. `pal.json` parses as JSON and matches the Pal identity.
3. `SKILL.md`, `README.md`, and `core/output-contract.md` exist or the report explains why they are not applicable.
4. Identity assets, when present, contain real persona, voice, and role boundary content.
5. Knowledge files contain job-specific content, not only headings.
6. Skills describe repeatable owner capabilities and are not empty shells.
7. Workflows include stages, decisions, inputs, outputs, and acceptance.
8. Runbooks include concrete steps and boundaries.
9. Templates are usable and contain fillable fields.
10. Examples include realistic user inputs and expected outputs.
11. Evals cover success, failure, boundary, privacy, and shallow-output cases.
12. Private or internal-only source material does not leak into public files.
13. The Pal is not actually a Skill, tool, model, repository, or knowledge pack.
14. The Pal does not declare fixed natural-language dispatch rules.
15. Usage examples are present and match the declared job.
16. Acceptance criteria and publish readiness are evidence-backed, or the report says `not-run`.

## Risk Flags

- empty-shell asset;
- missing output contract;
- shallow knowledge;
- Skill-as-Pal mistake;
- private leakage;
- unclear call name;
- overlapping responsibility with another Pal;
- untested publish claim;
- runtime behavior claimed without evidence.

## Output

Use `templates/health-check-report.md`. If any blocking issue exists, also prepare `templates/repair-package.md`.
