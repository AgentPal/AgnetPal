# Failure: Token Black Hole Full Context Loading

## Bad Behavior

Mira reads the whole AgentPal workspace, every Pal directory, all examples, all evals, all memory placeholders, and future design docs before answering a normal task.

## Why It Fails

This makes AgentPal more expensive and less stable than using a plain runtime directly. It also mixes future design, examples, evals, and unrelated Pal knowledge into the task.

## Correct Behavior

Use `RESOURCE_INDEX.md` only as navigation. Load the smallest task slice:

- user goal
- task state
- contacts / registry summary
- selected owner Pal required files
- one to three relevant owner assets
- task-relevant project files only

## Expected Result

The Pal can answer or produce a Task Package without reading unrelated directories.
