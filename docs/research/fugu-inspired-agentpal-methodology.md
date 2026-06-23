# Fugu-Inspired AgentPal Methodology

AgentPal learns from Fugu-style orchestration as a method, not as a model benchmark target.

The useful idea is that a scheduling layer can create capability gain by selecting participants, controlling context, isolating intermediate judgement, verifying results, and using shared memory across workflows. AgentPal translates that idea into the world of practical Agent runtimes.

AgentPal does not claim to exceed GPT, Claude, Fable, or any model family.

AgentPal does not compete with foundation models. It studies how to use existing Agent runtimes better.

Inspired by orchestration methods such as Fugu, AgentPal separates:

- Fast Route: use one suitable Pal / Runtime / Skill for clear tasks.
- Deep Conductor: future orchestration for complex tasks using workflow topology, Context Access Lists, isolation, verification, and routing memory.

AgentPal v0.1 keeps the active path simple: Mira as the default Main Pal, Leader Pal, and Conductor; Simple Pal Mode; Context Slicing; Task Package; and one-prompt project install. Deep Conductor remains future design.

## Method Transfer

| Fugu-style idea | AgentPal translation |
| --- | --- |
| Single model interface | Mira / Main Pal as the single user entry |
| Worker selection | Pal, runtime, model profile, reasoning profile, Skill, plugin, MCP candidate selection |
| Workflow step | Task Package or workflow plan step |
| Access list | Context Access List |
| Intra-workflow isolation | Pal Isolation during independent judgement stages |
| Persistent shared memory | Routing Reward Memory and verification memory |
| Orchestrator learning | AI Judgement informed by previous routing outcomes |

## What AgentPal Adopts

AgentPal adopts:

- single entry for ordinary users
- capability inventory instead of manual tool hunting
- task judgement before execution
- context access boundaries
- independent review stages when useful
- verification records
- routing memory for future judgement
- transparent explanations

## What AgentPal Does Not Adopt

AgentPal does not adopt:

- black-box model competition language
- hidden multi-Agent execution in v0.1
- automatic external Agent calls
- default all-context loading
- fixed task-to-worker routing
- claims that more workers always improve results

## Worker Analogy

In AgentPal, a "worker" candidate can mean:

- a Pal Pack
- an Agent runtime
- a model profile
- a reasoning strength
- a Skill
- a plugin
- an MCP server
- a verification method

These are capability candidates. They do not become hard-coded routes.

## Access List Analogy

Fugu-style access control maps to AgentPal's Context Access List:

- `can_read_paths`
- `can_read_summaries`
- `can_receive_outputs_from`
- `cannot_read`
- content-read budget
- sensitive context boundary
- output contract
- verification requirement

This extends AgentPal's existing Context Slicing and Task Package protocols.

## Isolation Analogy

If future AgentPal workflows use multiple Pal perspectives, independent judgement should happen before cross-reading other drafts. Otherwise the workflow collapses into group-chat agreement.

Isolation prevents:

- first-answer anchoring
- copied mistakes
- redundant opinions
- noisy context expansion
- false consensus

## Shared Memory Analogy

AgentPal should share only cleaned, task-safe learning across workflows:

- routing success and failure
- runtime fit
- model/reasoning fit
- Skill usefulness
- verification outcome
- user acceptance
- rework reason

It should not share raw private content, credentials, unrelated user memory, or full project files by default.

## Transparency Difference

AgentPal should remain transparent and inspectable:

- users can ask why a route was selected
- maintainers can review routing records
- capability profiles are readable files
- Context Access Lists are explicit
- PalBench records measurements instead of slogans

The goal is not hidden orchestration. The goal is better practical Agent use.
