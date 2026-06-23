# Context Packet Minimalism Protocol

Context Packets are handoff packets, not full conversation dumps.

## Required Principle

Each Context Packet must include the minimum context needed for the receiving Pal to start work safely and accurately.

## Default Packet Fields

- `from_pal`
- `to_pal`
- `mode`
- `user_goal`
- `task_state`
- `active_project`
- `relevant_project_slice`
- `constraints`
- `required_pal_files`
- `output_contract`
- `fallback_if_missing`
- `excluded_context`
- `index_known_summary`
- `content_read_paths`

## What To Include

Include:

- concise user goal
- current active project identity
- case-specific reason for selecting the Pal
- explicit constraints and safety boundaries
- relevant file paths or summaries
- required output shape
- known evidence or missing evidence
- a compact distinction between paths known by index and files actually read as content

## What To Exclude

Exclude by default:

- full chat history
- full project tree
- unrelated user memory
- private logs
- credentials or secrets
- all Pal lists beyond contact summary
- unrelated examples/evals
- future design docs

## Receiving Pal Responsibility

The receiving Pal should inspect its own required assets and relevant indexes after handoff. Mira should not pre-load the receiving Pal's entire professional library.

If context is insufficient, the receiving Pal asks for a narrower additional slice instead of reading everything.

Index-known paths in a packet are navigation hints only. They must not be treated as content already read.
