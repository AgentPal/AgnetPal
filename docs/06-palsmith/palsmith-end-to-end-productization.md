# PalSmith End-To-End Productization

This page describes the current v0.5 user path for using PalSmith to create or improve a Pal or Pal Team.

PalSmith remains a no-code Pal asset governor. It plans, classifies, reviews, and prepares Task Packages. The host runtime performs approved file reads or writes and must return evidence.

## End-To-End Loop

1. User gives a natural-language goal, source material, or repeated-work pattern.
2. PalSmith asks only high-impact missing questions.
3. PalSmith classifies the request as single Pal, Pal Team, material ingestion, health check, repair, or upgrade.
4. PalSmith marks privacy and source boundaries.
5. PalSmith drafts the Pal or Pal Team design.
6. PalSmith prepares a Runtime Task Package with allowed reads, allowed writes, forbidden writes, evidence requirements, and acceptance criteria.
7. The host runtime executes only approved work.
8. PalSmith reviews returned evidence.
9. Quinn or another reviewer may verify readiness when acceptance risk is high.
10. PalSmith records public-safe learning candidates only when privacy allows.

## Single Pal Flow

Use this when the user needs one callable working partner.

Required inputs:

- target job and user group
- examples of work the Pal should handle
- work the Pal must not handle
- source material and sensitivity
- desired language, tone, and output shape
- whether the result is private, team-local, or public-shareable

PalSmith output:

- Pal name and short id proposal
- role statement and not-responsible-for boundary
- first-call examples
- required root files and output contract
- knowledge, Skill, workflow, runbook, example, and eval plan
- material ingestion map
- Runtime Task Package for approved creation
- health-check checklist and repair template

## Pal Team Flow

Use this when the user goal needs several professional perspectives.

PalSmith output:

- team purpose and success criteria
- candidate Pal roles
- entry Pal recommendation
- collaboration boundaries
- context-sharing rules
- Task Package for approved team asset creation
- team health check and repair plan

Candidate Pals are not fixed routes. Mira remains the default entry Pal unless a separately approved project or team setup says otherwise.

## Faye Build Request Flow

Faye may produce a `FAYE_BUILD_REQUEST` after shaping a business delivery scenario.

PalSmith can convert that request into:

- candidate Pal Team design
- missing capabilities list
- reusable Pal asset candidates
- runtime capability candidates
- privacy boundaries
- first Task Package

PalSmith must not treat the request as permission to edit central contacts or create official Pal Packs automatically.

## Health And Repair

A PalSmith review should check:

- clear job ownership
- parseable `pal.json`
- required root files
- useful output contract
- real role-specific content
- Pal-owned Skill vs runtime Skill separation
- no private data leakage
- no fixed routing table
- no unsupported execution claims
- first usage examples
- readiness status: ready, partial, blocked, not-run, or draft

## Not-Do List

PalSmith must not:

- execute local file operations itself
- create or require a CLI, scanner, validator, importer, exporter, installer, daemon, UI, database, connector, or marketplace
- write contacts or registry entries in the first creation package
- run imported scripts or untrusted files
- turn ordinary Skills, tools, repositories, models, or knowledge bundles into Pal contacts
- expose private memory or source material in public examples
- claim automatic Deep Conductor, multi-Agent execution, or runtime capability probing

## Next Links

- [PalSmith](README.md)
- [PalSmith v0.5 creation and upgrade](../03-user-guides/palsmith-v0.5-pal-creation-and-upgrade.md)
- [Runtime-installed Skill orchestration](../05-orchestration-methodology/runtime-installed-skill-orchestration-guide.md)
