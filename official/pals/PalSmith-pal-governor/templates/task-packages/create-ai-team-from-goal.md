# Create AI Team From Goal Task Package

task_name: Create AI Team From Goal
owner_pal: PalSmith
executing_runtime: current Agent Runtime
status: copyable template

## User Fill Area

```text
Team goal:
Target users:
Business goal:
Main task types:
Recurring work situations:
Preferred team size or maximum:
Need Mira as main entry: yes / no / unsure
Existing Pals to reuse:
Pals or domains to avoid:
Existing materials:
Expected user-facing entry Pal:
Sensitive or private materials:
Target write path:
Public, team-local, or private use:
May the runtime write files after showing the path list: yes / no
```

## Goal

Create a small, bounded AI team design and optional draft Pal assets from a plain-language user goal. Team members are candidate capability holders. Mira or another explicitly selected leader remains the Conductor according to the current contacts, registry, and user-confirmed team design.

## Required Inputs

- user goal and target audience;
- business goal and main task types;
- recurring scenarios and success criteria;
- preferred team size;
- whether Mira should remain the main entry for ordinary use;
- candidate existing Pals to reuse or avoid;
- existing user materials;
- approved source materials;
- target write path;
- privacy and publication boundary;
- explicit confirmation before writes.

## Allowed Reads

- PalSmith AI team design and team creation protocols;
- current contacts and registry for existing Pal candidates;
- approved reference Pal Packs;
- approved user materials only.

## Allowed Writes

- approved team design directory;
- approved new member Pal directories when explicitly confirmed;
- team-level README, context rules, examples, evals, and health report;
- creation report inside the approved target directory.

## Forbidden Writes

- `contacts/`;
- `registry/`;
- unrelated Pal directories;
- runtime source code, scripts, package manifests, scanners, validators, installers, or UI files;
- private memory, credentials, or unapproved material.

## PalSmith Steps

1. Restate the team goal, target users, privacy boundary, and allowed write scope.
2. Ask focused clarification questions only for missing role, material, or boundary information.
3. Identify capability domains needed for the goal.
4. Check current contacts and registry for reusable Pal candidates.
5. Propose a small team with each member's job, non-job, evidence needs, and collaboration boundary.
6. Identify the Main Pal / leader / Conductor candidate and explain why it fits this case.
7. Define context-sharing rules, escalation rules, and handoff examples without permanent dispatch rules.
8. Define typical team tasks and user-facing team usage instructions.
9. Draft team asset structure and member Pal asset structure, including health-check expectations.
10. Review runtime evidence after execution and produce team health status, repair package when needed, and first usage examples.

## Prohibitions

- Do not create fixed collaborator rules or permanent domain routes.
- Do not claim Deep Conductor or multi-agent execution is active in the current release.
- Do not make team members automatic route targets.
- Do not register Pals in contacts or registry inside this package.
- Do not create runtime code, scanners, validators, importers, exporters, installers, or UI.
- Do not expose private user material in public examples.

## Expected Evidence

- approved target path;
- team member list and candidate capability domains;
- files created, changed, skipped, and not found;
- `pal.json` parse result for every created member Pal;
- current contacts / registry read evidence when existing Pal reuse is considered;
- context-sharing and privacy boundary report;
- not-run checks;
- team health-check result;
- repair package when health status is not clean.

## Acceptance Criteria

- The team has a clear purpose, success criteria, and Main Pal / leader / Conductor boundary.
- Every member has a job, non-job, source evidence needs, and first usage example.
- Existing Pals are reused only when current evidence supports the choice.
- No member is presented as a permanent route target.
- Context-sharing rules protect private and internal-only material.
- The team includes evals for collaboration, overlap, missing owner, and unsafe private leakage.
- The result is labeled `idea`, `draft`, `testing`, `stable`, `publish-ready`, or `not ready` with evidence.
