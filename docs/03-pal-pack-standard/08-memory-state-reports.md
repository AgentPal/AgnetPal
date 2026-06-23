# Memory, State, And Reports

## Status

Current for AgentPal `v0.1.0-rc.1`.

`memory/`, `state/`, and `reports/` are sensitive areas. Public Pal Packs should ship placeholders, not real runtime data.

## Minimum Public Placeholders

Use one of these memory shapes:

```text
memory/README.md
```

or:

```text
memory/user/README.md
```

Also include:

```text
state/README.md
reports/README.md
```

## What Can Be Public

- README placeholders.
- Synthetic examples.
- Public-safe templates.
- Non-sensitive guidance for what belongs in each directory.

## What Must Stay Private

- private user memory
- private project state
- real task reports
- credentials, tokens, secrets, or keys
- customer data
- internal development notes
- local absolute paths

## Writeback Rule

Before writing memory, state, or reports, decide whether the target is public release content or runtime-private content. When in doubt, keep it private or use a placeholder.
