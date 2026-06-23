# AgentPal

AgentPal is a Pal Workspace and Pal Pack standard practice for agent runtimes.

AgentPal gives every agent a Pal.

AgentPal v0.1.0-rc.1 is a Markdown / JSON / protocol workspace for runtimes such as Codex, Claude Code, and other CLI agents that can read structured workspace files. It is not an Agent runtime, not a multi-agent runtime, not an execution layer, not a desktop app, not a web app, and not an installer.

## Current Release Candidate

- Version: `v0.1.0-rc.1`
- Active path: `Simple Pal Mode only`
- Default Main Pal / Leader / Conductor: `Mira`
- Official bundled Pals: `Mira`, `Atlas`, `Vega`, `Rhea`, `Quinn`, `Morgan`, `Harper`, `Nova`
- Direct specialist call: `/pal Name`

## What Works Today

- AgentPal works as an AgentPal Workspace and a Pal Pack standard practice for agent runtimes.
- It gives runtimes a Pal layer for identity, knowledge, skills, context, memory boundaries, output contracts, coordination, review, summary, and learning rules.
- Mira is the default entry Pal for ordinary messages.
- Mira can use Fast Route to hand off substantive work to an owner Pal in the same response.
- The current runtime path supports Task Package, Context Slicing, and Asset Loading Budget rules.
- Contacts and registry support `/pal Name` direct calls for the current registered Pal set.
- You can use AgentPal today with Codex, Claude Code, or a generic CLI agent that can read Markdown / JSON instructions and maintain context.

## What Is Not Active In v0.1

- AgentPal is not an Agent runtime or execution engine.
- AgentPal is not a multi-agent runtime, Subagent Mode, or parallel child workflow system in `v0.1.0-rc.1`.
- Deep Conductor is future design only.
- External Agent orchestration is future design only.
- AgentPal is not a desktop app, web app, hosted service, marketplace, daemon, scanner, validator, or automatic installer.
- PalBench in this release is small-sample validation, not a statistically significant benchmark.

## Quick Start

### Codex

1. Open the AgentPal Workspace in Codex.
2. Copy the contents of [`INIT_PROMPT.md`](INIT_PROMPT.md).
3. Let Codex initialize AgentPal with Mira as the default entry.
4. Start with Mira, or call a specialist directly with `/pal Name`.
5. Use AgentPal in `Simple Pal Mode only`.

More: [`docs/04-runtime-guides/01-use-with-codex.md`](docs/04-runtime-guides/01-use-with-codex.md)

### Claude Code

1. Open your real user project first:

   ```text
   cd <your-project>
   claude
   ```

2. Paste the one-prompt install from [`prompts/claude-code/install-agentpal-current-project.md`](prompts/claude-code/install-agentpal-current-project.md).
3. Keep the current project directory as task context. Do not treat the AgentPal Workspace as the user project.
4. `.claude/settings.local.json` is local machine configuration and should not be committed.
5. This path is a lightweight project binding, not a deep Claude Code plugin or automatic installer.

More: [`docs/04-runtime-guides/02-use-with-claude-code.md`](docs/04-runtime-guides/02-use-with-claude-code.md)

### Generic CLI Agent

1. Open your real user project first:

   ```text
   cd <your-project>
   <your-cli-agent>
   ```

2. Paste the generic install prompt from [`prompts/cli-agent/install-agentpal-current-project.md`](prompts/cli-agent/install-agentpal-current-project.md).
3. Use this path only if the CLI agent can read directories, follow Markdown / JSON instructions, and maintain task context.
4. This is a generic compatibility path. Not every CLI agent has been validated.

More: [`docs/04-runtime-guides/03-use-with-generic-cli-agent.md`](docs/04-runtime-guides/03-use-with-generic-cli-agent.md)

## Official Pals

| Pal | Role | Direct call |
| --- | --- | --- |
| Mira | Main Pal / Leader / Conductor | `/pal Mira` |
| Atlas | Development | `/pal Atlas` |
| Vega | Research | `/pal Vega` |
| Rhea | System | `/pal Rhea` |
| Quinn | Quality | `/pal Quinn` |
| Morgan | Document | `/pal Morgan` |
| Harper | Writing | `/pal Harper` |
| Nova | Product | `/pal Nova` |

Mira is the default entry Pal. Specialist Pals do not listen by default.

## How Simple Pal Mode Works

In `v0.1.0-rc.1`, ordinary messages start with Mira. Mira judges ownership case by case. If a registered specialist Pal should own the request, Mira gives a short handoff and stops. The owner Pal answers immediately in the same response by using its own Pal assets and output contract.

`/pal Name` does not start a separate agent process. It tells the current runtime to enter that Pal's working mode.

## Fast Route, Task Package, Context Slicing

- Fast Route is the active clear-task handoff pattern in `v0.1.0-rc.1`.
- Task Package helps compress goals, context, constraints, evidence requirements, and acceptance criteria for the current runtime.
- Context Slicing means AgentPal loads only the files needed for the current task.
- Asset Loading Budget limits how much Pal context should be loaded by default.
- Deep Conductor is documented as future design only, not an active runtime path.

## PalBench Small-Sample Validation

AgentPal includes PalBench material as small-sample validation for the current release candidate. It is useful as cautious evidence for the RC, but it is not a statistically significant benchmark and it does not claim model superiority.

## Repository Structure

| Path | Purpose |
| --- | --- |
| `pals/` | Official and user-added Pal Packs |
| `contacts/` | Pal contacts and aliases |
| `registry/` | Pal indexes and discovery records |
| `orchestration/` | Runtime rules and protocol documents |
| `prompts/` | Copy-and-paste prompts for setup and maintenance |
| `docs/` | User-facing documentation |
| `projects/` | External project binding templates |
| `templates/` | Reusable templates |

## Documentation

- Documentation home: [`docs/README.md`](docs/README.md)
- Overview: [`docs/00-overview/`](docs/00-overview/)
- Pal Pack standard: [`docs/03-pal-pack-standard/`](docs/03-pal-pack-standard/)
- Runtime guides: [`docs/04-runtime-guides/`](docs/04-runtime-guides/)
- Authoring Pals: [`docs/07-authoring-pals/`](docs/07-authoring-pals/)
- Orchestration methodology: [`docs/05-orchestration-methodology/`](docs/05-orchestration-methodology/)
- Validation and evidence: [`docs/06-validation-and-evidence/`](docs/06-validation-and-evidence/)
- Release candidate notes: [`docs/08-release-candidate/`](docs/08-release-candidate/)
- Current status: [`docs/00-overview/01-current-status.md`](docs/00-overview/01-current-status.md)
- Current capabilities: [`docs/00-overview/02-current-capabilities.md`](docs/00-overview/02-current-capabilities.md)
- What AgentPal is not: [`docs/00-overview/04-what-agentpal-is-not.md`](docs/00-overview/04-what-agentpal-is-not.md)
- Release candidate summary: [`docs/00-overview/05-release-candidate-summary.md`](docs/00-overview/05-release-candidate-summary.md)
- Project-first connection: [`docs/04-runtime-guides/04-project-first-connection.md`](docs/04-runtime-guides/04-project-first-connection.md)

## Contributing

Contributions should preserve the `v0.1.0-rc.1` boundary: AgentPal is a Pal Workspace and Pal Pack standard practice for agent runtimes, with `Simple Pal Mode only` as the active path. Do not describe future design material as active runtime behavior.

See [`CONTRIBUTING.md`](CONTRIBUTING.md).

## License

MIT. See [`LICENSE`](LICENSE).
