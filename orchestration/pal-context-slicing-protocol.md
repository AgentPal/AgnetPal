# Pal Context Slicing Protocol

AgentPal v0.1 uses Simple Pal Mode only. Context slicing keeps Pal work useful without turning the Pal workspace into a token sink.

## Purpose

For every substantive task, load the smallest context slice that can support a valid answer, handoff, review, or task package. Do not load all Pals, all project files, all knowledge, all memory, all examples, or all evals by default.

## Short Initialization Default

Initialization uses the short path by default. It loads only root guardrails, workspace metadata, contacts / registry JSON, Mira minimum assets, and the Runtime Response Gate. Deep initialization is diagnostic only.

Do not load all Pals, Mira full identity, registry Markdown, resource maps, multiple orchestration protocols, templates, examples, evals, future design, or memory during ordinary initialization.

## Context Layers

1. User Goal
   - The user's current objective and requested output.
   - Always preserve this layer.

2. Task State
   - Current task status, active Pal, whether clarification is needed, and known safety or approval boundaries.

3. Project Slice
   - Only project files, directories, documents, or summaries directly relevant to the current task.
   - Do not read the whole project tree by default.

4. Pal Asset Slice
   - The selected owner Pal's minimum required assets:
     - `PAL.md`
     - `pal.json`
     - `SKILL.md`
     - `AGENTS.md`
     - `core/output-contract.md`
   - Then load only the most relevant skill, knowledge card, runbook, or workflow.

5. Memory Slice
   - Only task-relevant memory summaries or public-safe placeholders.
   - Do not read full memory directories by default.

6. Constraints Slice
   - User constraints, privacy limits, safety limits, no-runtime, no-subagent-active, no-hardcoded-routing, and current release boundary rules.

7. Output Contract Slice
   - The response shape required for this task, including whether a compressed Agent / Runtime task package is needed.

## Mira Reading Rules

Mira reads:

- user goal
- task state
- current runtime guardrails
- contacts / registry summary
- active project high-level summary when needed

Mira does not read:

- all Pal professional knowledge
- all `pals/`
- all project files
- all memory
- all examples or evals
- future design docs during ordinary task handling

When Mira selects an owner Pal, Mira passes a minimal Context Packet and stops. The owner Pal decides its own asset slice.

## Owner Pal Reading Rules

The owner Pal reads:

- its own `PAL.md`, `pal.json`, `SKILL.md`, `AGENTS.md`, and `core/output-contract.md`
- relevant local indexes
- one to three relevant skills, knowledge cards, runbooks, or workflows
- the task-relevant project slice
- zero to two relevant memory summaries

The owner Pal does not read other Pal professional assets unless AI judgement explicitly needs a consultant or reviewer and a Context Packet is created.

## Specialist Pal Rules

Specialist Pals only process their own context slice. They may output:

- professional judgement
- constraints
- acceptance criteria
- risks
- task package fragments
- evidence requirements

They must not expand into whole-workspace or whole-project analysis unless the user explicitly asks for that scope and the context budget is raised.

## Forbidden Default Loading

Do not default to:

- reading all `pals/`
- reading all `knowledge/`
- reading all `memory/`
- reading the whole external project directory
- reading every `AGENTS.md`, `README.md`, or docs file
- loading Mira with all specialist Pal materials
- loading examples, evals, reports, archives, imports, or future design docs for ordinary tasks
- silently widening a task to whole-repository review

## Escalating Context

If a task needs more context than the default slice:

1. Read an index first.
2. Name the missing context.
3. Load the next smallest relevant file set.
4. Ask the user when scope, privacy, or risk is unclear.
5. Record why the context budget was expanded.

## Index Exposure Versus Content Read

Context slicing must distinguish files known by index from files read as content.

- `index_known_count`: number of paths known through directory listing, registry, `RESOURCE_INDEX.md`, or Pal indexes
- `index_known_source`: where the path knowledge came from
- `index_known_paths`: optional short list or summary of known paths
- `content_read_count`: number of files actually opened and read
- `content_read_paths`: files actually read
- `index_only_paths_summary`: paths or groups known but not opened
- `index_only_not_content_read`: true when paths were known without content reads
- `not_content_read_note`: plain-language note that file names are not file contents

Knowing a file path exists does not allow the answer to claim that its content was used.

## Asset Usage Accountability

Normal user answers should stay concise. For complex or audited work, the active Pal should internally track:

- required assets read
- optional assets read
- skipped assets
- memory summaries used
- project files read
- fallback used
- index-known paths versus content-read paths

If the user asks "what did you use?", provide a simplified Asset Loading Report.
