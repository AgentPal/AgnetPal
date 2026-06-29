# Subthread / Subagent Decision Standard

Status: v0.5 no-code protocol

## Purpose

This standard defines when a Pal may recommend single-thread work, owner +
verifier, parallel review, subthreads, subagents, or external Agent handoff.

## Rules

- `subthread_support` and `subagent_support` must come from a Host Capability
  Snapshot or current runtime evidence.
- Without evidence, say `if supported, this could be parallelized`; do not claim
  subthreads or subagents were started.
- Subthreads and subagents need bounded Context Packets.
- Private or customer data needs a Context Access List before any split.
- Peer reviewer drafts and hidden reasoning must not be shared across isolated
  reviewers unless explicitly authorized.

## Decision Options

| decision | Use when |
| --- | --- |
| `single_thread` | Simple or tightly coupled task; shared context matters more than parallelism |
| `owner_verifier` | One owner can produce evidence and one verifier can independently review it |
| `parallel_review` | Independent reviews of artifacts/options add real value and privacy can be bounded |
| `subthread_candidate` | Host supports separate threads and the task has isolated packages |
| `subagent_candidate` | Host supports subagents and the task has isolated packages plus clear owner/verifier roles |
| `not_recommended` | Task is simple, sensitive, unclear, or would increase coordination risk |
| `unknown` | Host support is unknown |

## Prohibitions

- Do not split customer-private material by default.
- Do not create subagents to satisfy a buzzword.
- Do not treat `parallel_review` as automatic runtime execution.
- Do not hide missing capability evidence.

