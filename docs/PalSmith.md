# PalSmith

PalSmith is AgentPal's official Pal asset governance Pal.

Registered id/path: `palsmith-pal-governor` at `official/pals/PalSmith-pal-governor`.

## What PalSmith Does

PalSmith helps users and maintainers design, review, repair, and govern Pals and Pal Teams.

It can help with:

- creating a draft Pal
- creating a draft Pal Team
- classifying source material into identity, knowledge, Skill, workflow, runbook, example, eval, memory candidate, or report
- preparing bounded Runtime Task Packages for approved file creation
- checking Pal health, privacy, job fitness, and release readiness
- detecting responsibility conflicts
- reviewing imports, exports, snapshots, rollbacks, and version upgrades as no-code governance tasks

## How To Call PalSmith

```text
/pal PalSmith Help me design a Pal for customer onboarding QA.
Keep it as a draft and do not modify central contacts.
```

```text
/pal PalSmith Design a small Pal Team for a sales operations workflow.
Separate candidate Pal roles, runtime capability candidates, privacy risks, and the first Task Package.
```

## How PalSmith Works

PalSmith prepares judgement and Task Packages. The host runtime performs any approved file reads, writes, archive creation, downloads, copies, or JSON updates and must return evidence.

PalSmith should:

- preserve user source intent
- mark missing information
- classify privacy sensitivity
- separate Pal-owned Skills from host runtime Skills
- keep candidate Pals as judgement inputs, not fixed routes
- ask for explicit approval before controlled writes
- report `missing`, `partial`, `not-run`, `blocked`, or `unknown` honestly

## What PalSmith Is Not

PalSmith is not:

- a CLI
- a scanner
- a validator program
- an importer/exporter program
- an installer
- a daemon
- a UI
- a connector
- a marketplace
- an app runtime
- an automatic central roster mutator

AgentPal does not require users to install Python, Node.js, Rust, or another package runtime to use PalSmith in ordinary no-code mode.

## Registration Boundary

Drafting a Pal does not register it.

Updating `workspace/organization/contacts/` is a separate governance task. A draft Pal, Skill, tool, model, plugin, MCP server, raw repository, knowledge pack, or persona pack must not become a central Pal contact automatically.

For v0.5, the official bundled roster remains 10 Pals and includes Faye.

## Faye To PalSmith To Quinn

A common v0.5 chain is:

1. Faye turns a business goal into a delivery package and `FAYE_BUILD_REQUEST`.
2. PalSmith turns the request into a Pal or Pal Team design.
3. Quinn reviews evidence, acceptance criteria, and risk before the result is treated as ready.

This is a no-code collaboration chain inside the current host runtime. It is not automatic multi-Agent execution.

## Next Reading

- [PalSmith index](06-palsmith/README.md)
- [PalSmith end-to-end productization](06-palsmith/palsmith-end-to-end-productization.md)
- [PalSmith v0.5 Pal creation and upgrade](03-user-guides/palsmith-v0.5-pal-creation-and-upgrade.md)
- [Create your first Pal](02-getting-started/06-create-your-first-pal-in-5-minutes.md)
- [Runtime Task Package standard](03-pal-pack-standard/14-runtime-task-package.md)
