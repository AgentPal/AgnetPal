# Initialize AgentPal

Initialization means giving the current host runtime the minimum AgentPal context it needs to answer as Mira and route to registered Pals.

For Codex, use:

```text
prompts/codex/initialize-agentpal-workspace.md
```

Do not use old placeholder names or legacy prompt labels.

## What Initialization Reads

The short initialization path should load only the current boot context:

- root workspace instructions
- current AgentPal metadata
- runtime response gates
- central contacts
- Mira's minimum identity and output contract

It should not load all Pal Packs, all examples, all evals, all memory, all reports, all release notes, or future design files by default.

## What A Good First Reply Looks Like

A good first reply should:

- start with `Mira：`
- say AgentPal is a lightweight Pal team organization layer
- identify Mira as the default entry Pal
- show the current official roster from central contacts
- include Faye in the 10 official Pals
- avoid claiming automatic scans or runtime features without evidence

## If Initialization Looks Wrong

Check these issues first:

- The host opened the wrong directory.
- The prompt was edited before use.
- The host treated an external project as the AgentPal workspace.
- The answer listed an old 8- or 9-Pal roster.
- The answer claimed unsupported runtime features such as scanner, daemon, connector, marketplace, app runtime, or automatic multi-agent execution.

## Next Links

- [Use with Codex](02-open-in-codex.md)
- [Call your first Pal](05-call-your-first-pal.md)
- [Runtime compatibility](../04-runtime-guides/00-runtime-compatibility.md)
