# Context Packet Usage Guide

Context Packet is the v0.3 no-code way to move bounded context between Pals without turning collaboration into a full-chat dump.

It is for users, Pal maintainers, and runtime adapters that need a copyable protocol for `/pal` direct calls, `@Pal` consults, reviews, handoffs, and owner transfers.

## What It Is

A Context Packet is a small structured handoff:

- who prepared it;
- who may receive it as a candidate;
- what mode is being used;
- what the user goal is;
- what the recipient may read;
- what the recipient must not read;
- what output is needed;
- what evidence or verification is required.

It is not a message bus, queue, sandbox, permission grant, runtime API, or automatic multi-agent scheduler.

## Why Not Full Chat History

Full history transfer creates four problems:

- privacy risk: unrelated private memory or credentials may be copied;
- context bloat: the recipient must sort noise before doing useful work;
- group-chat collapse: reviewers may anchor on earlier opinions instead of judging independently;
- false evidence: a path or claim in chat is not proof that the file was read or verified.

Use a safe summary plus explicit `can_read` and `cannot_read` fields instead.

## When To Use A Packet

Use a Context Packet when:

- the user calls `/pal Name` and the called Pal needs bounded context;
- the user mentions `@Pal` for consult or review;
- an owner Pal delegates a sub-output;
- Mira or an owner Pal transfers ownership;
- a verifier needs evidence context;
- independent reviewers must stay isolated;
- a runtime needs a Task Package under a Pal-layer owner.

Do not use a packet for a short ordinary answer that Mira can give directly.

## `/pal` Direct Call Vs `@Pal` Consult

`/pal Atlas ...` means the user explicitly named Atlas. Atlas becomes the current owner candidate and still applies the core gates. If the task is composite, Atlas names the stages it can own and the stages needing other candidates.

`@Quinn ...` means consult or review by default. Quinn receives a packet, reviews only the allowed context, writes a final report, and returns it to Mira or the current owner Pal. Ownership does not transfer unless the user explicitly asks for handoff or takeover.

## Collaboration Modes

| Mode | Use For | Ownership |
| --- | --- | --- |
| `direct_owner` | Explicit `/pal Name` call | named Pal is current owner candidate after gates |
| `consult` | Bounded perspective from `@Pal` | current owner remains responsible |
| `delegate` | Bounded sub-output | current owner remains responsible until accepted transfer |
| `handoff` | Active stage transfer | target Pal candidate after packet and gates |
| `review` | Evidence, risk, or acceptance review | reviewer does not own final synthesis by default |
| `owner_transfer` | Explicit ownership move | target Pal accepts after core gates |

## Required Fields

The current template requires:

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

`to_pal_candidate` is always a candidate, not a fixed route.

## Privacy Boundary

Default exclusions:

- full chat history;
- private user memory;
- private project memory;
- credentials, tokens, secrets, payment data, and raw private logs;
- unrelated Pal assets;
- all project files;
- other independent reviewer drafts.

Sensitive context should be `none`, `excluded`, or summarized only with explicit approval.

## Relationship To Context Access List

Context Packet is the envelope. Context Access List is the detailed access rule for a stage.

Small collaborations may only need `can_read` and `cannot_read`. Higher-risk work may point to a full Context Access List with content-read budgets, index-known paths, and verification rules.

## Runtime Use

Codex, Claude Code, and generic CLI agents can follow Context Packet as Markdown instructions. They do not need native slash-command or mention APIs.

If a runtime sees `/pal Name` or `@Pal`, it should:

1. read the current AgentPal core gates;
2. resolve the Pal through contacts / registry;
3. apply the mention and direct Pal protocol;
4. build or follow a Context Packet;
5. keep runtime execution separate from Pal ownership;
6. report evidence for any real file, command, tool, or publishing action.

v0.3 remains a no-code protocol prototype. It does not start background Pals, external Agents, Subagent Mode, Deep Conductor automation, or runtime parallelism.
