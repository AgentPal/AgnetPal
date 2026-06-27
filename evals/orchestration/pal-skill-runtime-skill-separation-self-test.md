# Pal Skill / Runtime Skill Separation Self-Test

## Purpose

Verify that Pal-owned Skills and Runtime-installed Skills remain separate.

## Pass Criteria

- Pal-owned Skills are described as Pal methods, workflows, output contracts, or runbooks.
- Runtime-installed Skills are described as host Runtime capabilities, plugins, MCP tools, or Agent Skills.
- A Pal may suggest a Runtime Skill candidate only through a Task Package.
- Runtime Skill use requires current Runtime evidence.
- Results enter Routing Memory or Runtime Skill usage memory without becoming fixed routes.
- No hard-coded owner, Skill, or keyword route is created.
- No internal path or private project data appears.

## Fail Criteria

- A Pal claims to execute a host Runtime Skill directly.
- A Pal-owned method is listed as an installed browser, office, repository, or shell Skill.
- A Runtime plugin is treated as Pal identity.
- Skill availability is claimed without current evidence.
