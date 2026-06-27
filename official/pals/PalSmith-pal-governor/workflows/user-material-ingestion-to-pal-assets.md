# User Material Ingestion To Pal Assets Workflow

PalSmith uses this workflow when a user provides raw material for creating or repairing a Pal or AI team.

## Objective

Transform approved user material into traceable Pal assets without losing source intent, hiding uncertainty, or leaking private content into public files.

## Material Types

| Material type | Asset candidates | Notes |
| --- | --- | --- |
| Persona, role notes, voice samples | `PAL.md`, output contract, examples | Preserve voice examples separately from stable facts. |
| Company introduction | `knowledge/`, `PAL.md`, examples | Keep public company facts separate from internal strategy. |
| Job responsibilities | `PAL.md`, Skills, workflows, runbooks | Convert responsibilities into owned and non-owned work. |
| Historical copy | examples, output contract, evals | Preserve tone and claim boundaries. |
| Product materials | `knowledge/`, templates, evals | Mark draft, confidential, or public product claims. |
| Customer support Q&A | `knowledge/`, runbooks, examples, evals | Remove customer identifiers unless explicitly private. |
| Industry reports | `knowledge/`, research inventory, evals | Preserve source, date, and uncertainty. |
| Process documents | runbooks, workflows, Skills | Repeated processes become operational assets. |
| Personal experience | knowledge, examples, private notes | Mark private, internal-only, or synthetic before public use. |
| Domain notes, guides, FAQs | `knowledge/` | Keep source coverage and uncertainty. |
| Repeated procedures | `runbooks/`, `workflows/`, Skills | Use a runbook for operational steps, a workflow for multi-stage judgement, and a Skill for repeatable owner capability. |
| Example prompts and replies | `examples/`, eval fixtures | Keep representative before/after pairs. |
| Failure reports and complaints | `evals/`, repair package | Convert into negative tests and acceptance criteria. |
| Team process notes | team README, context rules, workflows | Mark owner, verifier, and escalation boundaries. |
| Private user facts or credentials | excluded, private, or internal-only | Never place in public docs. |

## Workflow

1. Confirm the material scope and whether each source can be read.
2. Build a source inventory with title, origin, sensitivity, and intended use.
3. Mark each item as public, team-local, private, internal-only, or excluded.
4. Classify content into identity, knowledge, Skill, workflow, runbook, template, example, eval, or memory-template candidate.
5. Preserve source excerpts only when permitted and necessary; otherwise summarize with source pointers.
6. Detect repeated operations that deserve runbooks, workflows, or Skills.
7. Detect examples that should become eval cases or usage examples.
8. Detect private facts that must stay out of public assets.
9. Draft a material ingestion map before any runtime write.
10. After execution, compare generated assets against the source inventory and report missing or compressed content.

## Source Preservation Rules

- Keep a source inventory for every approved material item.
- Do not collapse contradictory material into one confident rule.
- Mark uncertainty and missing context.
- Keep sensitive examples synthetic when publishing is possible.
- Preserve user language and domain terms unless the user asks for translation.

## Output

The workflow produces:

- user material ingestion map;
- source coverage summary;
- proposed generated assets;
- private or excluded material list;
- repair notes for underused or over-compressed sources.
