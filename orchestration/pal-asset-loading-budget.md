# Pal Asset Loading Budget

AgentPal v0.1 uses file-level context budgets instead of exact token metering. The goal is predictable, small, auditable Pal asset loading.

## Default Budget In Simple Pal Mode

### Initialization Default Budget

Default initialization uses the short path.

Target:

- `content_read_count`: 10-15 files
- external project binding files: up to 5, only when the session is already bound to an external project
- AgentPal workspace minimum files: up to 9
- no examples, evals, future design, reports, imports, all memory, all project files, or all Pal directories

The default initialization reply should stay short. Do not show a long Asset Loading Report unless the user asks for diagnostics or asset evidence.

### Diagnostic Initialization Budget

Deep or wide initialization is allowed only when needed for diagnostics, release checks, registry/contact repair, failed initialization, or explicit user request.

Requirements:

- state why the budget expanded
- read indexes before content expansion
- separate `index_known_count` from `content_read_count`
- avoid all-Pal, all-project, and all-memory reads unless the user explicitly requested that scope

### Mira Initial Judgement

Default maximum:

- current user goal
- current task state
- root guardrail summary
- contacts / registry summary
- zero to two project summary files when needed

Mira must not load all specialist Pal assets to decide routing.

### Owner Pal Takeover

Default maximum:

- required owner files: 4-5 files
  - `PAL.md`
  - `pal.json`
  - `SKILL.md`
  - `AGENTS.md`
  - `core/output-contract.md`
- local indexes: up to 4 index files
  - `skills/index.md`
  - `knowledge/index.md`
  - `runbooks/index.md`
  - `workflows/index.md`
- relevant owner assets: 1-3 files
- project slice: 1-5 files, based on task scope
- memory summaries: 0-2 files

If the owner Pal needs more context, it must ask for or justify a narrower additional slice. More context must be selected index-first. Do not silently expand to whole directories.

### Default Exclusions

Do not load by default:

- all Pals
- all docs
- all examples
- all evals
- all reports
- all memory
- future design documents
- archived or imported large materials
- whole project trees

## Over-Budget Handling

When the task needs more context:

1. Say what context is missing.
2. Read an index or file list first.
3. Load the smallest next relevant slice.
4. Ask the user when privacy, scope, or cost is unclear.
5. Do not silently escalate to whole-repository loading.

## Budget Status Labels

Use these labels in internal notes or asset loading reports:

- `within_default_budget`
- `expanded_with_reason`
- `needs_user_scope`
- `blocked_by_privacy`
- `fallback_used`

## Reporting

Do not print a long asset list in every answer. Provide a compact report only when:

- the user asks what assets were used
- the task is an eval, release gate, or audit
- the Pal used fallback because a relevant asset was missing

Compact reports must distinguish:

- `index_known_count`
- `index_known_source`
- `index_known_paths` or `index_only_paths_summary`
- `content_read_count`
- `content_read_paths`
- `index_only_not_content_read`
- `not_content_read_note`
