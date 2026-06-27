# Context Packet Protocol

Context Packet is the v0.3 no-code structure for transferring bounded context between Mira, owner Pals, reviewer Pals, verifier Pals, and runtime execution candidates.

It is a controlled handoff packet. It is not full chat history, not a full project dump, not a permission grant, and not an automatic message bus.

## Purpose

Use a Context Packet when:

- `/pal Name` starts a direct Pal request;
- `@Pal` asks for consult, delegate, handoff, review, or owner transfer;
- a verifier needs evidence context;
- parallel independent reviewers need isolated context;
- a Runtime candidate needs a Pal-layer execution package.

## Required Fields

```yaml
schema:
packet_id:
created_at:
from_pal:
to_pal_candidate:
mode:
explicit_user_call:
owner_status:
user_goal:
task_summary:
current_state:
constraints:
relevant_files:
can_read:
cannot_read:
can_receive_outputs_from:
needed_output:
output_contract:
verification_requirements:
privacy_policy:
sensitive_context:
expiration:
handoff_notes:
return_to:
final_report_required:
```

## Field Rules

- `schema` names the packet schema, for example `agentpal.context-packet.v0.3`.
- `packet_id` is unique within the workflow.
- `from_pal` names the Pal preparing the packet.
- `to_pal_candidate` is a candidate recipient, not a fixed route.
- `mode` is one of `consult`, `delegate`, `handoff`, `review`, `owner_transfer`, or `direct_owner`.
- `explicit_user_call` records whether the user explicitly used `/pal Name`, `@Pal`, a handoff phrase, or no explicit call.
- `owner_status` records whether the recipient is a current owner candidate, reviewer candidate, consultant candidate, delegated sub-output candidate, or accepted owner after transfer.
- `relevant_files` are path references or source summaries, not proof that content was read.
- `can_read` lists allowed files, summaries, or evidence.
- `cannot_read` lists excluded context such as private memory, secrets, unrelated Pal assets, all project files, and other independent reviewer drafts.
- `can_receive_outputs_from` names prior accepted outputs the recipient may read.
- `needed_output` states the exact deliverable expected.
- `output_contract` names the required output shape.
- `verification_requirements` names evidence needed before completion.
- `privacy_policy` states whether sensitive context is excluded, summarized, or requires approval.
- `sensitive_context` should usually be `none` or `excluded` in public examples.
- `expiration` says when the packet should no longer be reused.
- `return_to` states where the response returns: Mira, the current owner Pal, or the user.
- `final_report_required` defaults to `true` unless the packet is only a narrow clarification.

## Mode Rules

Use the smallest mode that matches the user intent:

- `direct_owner`: user explicitly called `/pal Name`; the named Pal is the current owner candidate and still runs core gates.
- `consult`: user or owner mentioned `@Pal` for perspective; ownership stays with the current owner.
- `delegate`: current owner asks another Pal for a bounded sub-output; ownership returns to the current owner unless accepted transfer happens.
- `handoff`: current owner transfers active stage ownership to another Pal candidate with a packet boundary.
- `review`: reviewer or verifier evaluates evidence, risk, or acceptance criteria without taking over by default.
- `owner_transfer`: user or current owner explicitly moves ownership; target Pal accepts only after core gates.

Do not use `mode` values such as `runtime_execution` to make a runtime look like a Pal. Runtime execution belongs in a Task Package or Context Access List under a Pal-layer owner.

## What Context Packet Must Not Contain

Do not include:

- full chat history;
- full AgentPal workspace contents;
- all Pal Packs;
- all project files;
- private user memory;
- private project memory;
- credentials, tokens, secrets, raw private logs, payment data, or unrelated personal data;
- other independent reviewers' drafts before the summary stage.

## Relationship To Context Access List

Context Packet is the transfer envelope. Context Access List is the detailed access rule for one workflow step.

A packet may contain a compact `can_read` and `cannot_read` list, or it may point to a full Context Access List when the step needs more detail.

## Candidate Boundary

`to_pal_candidate` and any runtime, Skill, plugin, or MCP names inside a packet are candidates. They are selected by current AI judgement from the user goal, deliverable, context, risk, contacts, registry, and current evidence.

A Context Packet must not encode:

- keyword triggers;
- task/domain -> Pal maps;
- required fixed collaborators;
- "must route" rules.

## v0.3 Boundary

In v0.3, Context Packet is a no-code protocol and template. It does not create automatic multi-Pal execution, a queue, a message bus, a sandbox, or a runtime permission system.

Codex, Claude Code, or a generic CLI agent may read the packet and execute the staged instructions only within the host runtime's normal permissions and evidence rules.

`/pal` and `@Pal` are plain-text AgentPal protocols in v0.3. They are not native CLI commands unless a host runtime separately implements them. If the host runtime does not have native slash-command support, it should still parse them as user text and follow this protocol.
