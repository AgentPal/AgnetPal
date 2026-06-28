# R93-C Thin Binding Simulation Results

## Test Metadata

- test date: 2026-06-28
- test thread: R93-C
- test target: `templates/project-binding/`
- execution layer: Codex shell / PowerShell
- temp dirs:
  - generic: `<TEMP>/r93c-20260628-125207/agentpal-r93c-generic-project`
  - claude: `<TEMP>/r93c-20260628-125207/agentpal-r93c-claude-project`

## Scope

This test simulated local thin binding installation into two temporary external projects.

No temporary project was created inside the public AgentPal workspace. No remote Git operation was run. No template source file was modified.

## Generic Codex Result

Result: pass.

Created files:

- `.agentpal/AGENTPAL.md`
- `.agentpal/project.json`
- `AGENTS.md`

Checks:

| Check | Result |
| --- | --- |
| expected file surface only | pass |
| `.agentpal/project.json` JSON parse | pass |
| `binding_mode=thin` | pass |
| `binding_style=thin-binding` | pass |
| contains `agentpal_workspace_root` | pass |
| contains `central_pal_contacts` | pass |
| contains `agentpal_project_record` | pass |
| central contacts path exists in AgentPal workspace | pass |
| `keyword_routing_allowed=false` | pass |
| no copied Pal packs | pass |
| no copied contacts file | pass |
| no copied memory / reports / evals | pass |

## Claude Code Result

Result: pass with template-note.

Created files:

- `.agentpal/AGENTPAL.md`
- `.agentpal/project.json`
- `.claude/settings.local.json`
- `.gitignore`
- `CLAUDE.md`

Checks:

| Check | Result |
| --- | --- |
| expected file surface only | pass |
| `.agentpal/project.json` JSON parse | pass |
| `.claude/settings.local.json` JSON parse | pass |
| `binding_style=thin-binding` | pass |
| contains `agentpal_workspace_root` | pass |
| contains central contacts pointer | pass |
| `.gitignore` contains `.claude/settings.local.json` | pass |
| central contacts path exists in AgentPal workspace | pass |
| `keyword_routing_allowed=false` | pass |
| no copied Pal packs | pass |
| no copied contacts file | pass |
| no copied memory / reports / evals | pass |

Template note:

- Claude `.agentpal/project.json` does not currently include `agentpal_project_record`.
- This did not block the Claude-specific file-surface and forbidden-dir simulation, but it differs from the protected block and binding docs that describe `agentpal_project_record`.
- Recommended follow-up: add an `agentpal_project_record` pointer to the Claude project binding template in a separate template-fix thread.

## Forbidden Dirs

Forbidden directory list checked:

- `.agentpal/memory`
- `.agentpal/state`
- `.agentpal/reports`
- `.agentpal/context`
- `.agentpal/index`
- `.agentpal/pals`
- `.agentpal/workflows`
- `.agentpal/evals`
- `.agentpal/capability-inventory`
- `.agentpal/business-systems`
- `.agentpal/reviews`
- `.agentpal/evidence`
- `.agentpal/replay`
- `.agentpal/rollback`
- `.agentpal/verification`
- `.agentpal/audit-trail`
- `.agentpal/governance-decisions`
- `.agentpal/change-ledger`

Result:

| Project | forbidden dirs present | count |
| --- | ---: | ---: |
| Generic Codex | none | 0 |
| Claude Code | none | 0 |
| total | none | 0 |

## Keyword Routing Check

Search target: `keyword_map|domain_map|role_map`

Result:

- occurrence count: 3
- all occurrences are negative prohibition text in generated instruction files
- positive JSON map keys found: 0
- `routing_policy=ai_judgement_only` present where provided
- `keyword_routing_allowed=false` in both generated `project.json` files

Observed prohibition references:

- Generic `AGENTS.md`: forbids `keyword_map`, `domain_map`, and `role_map`
- Generic `.agentpal/AGENTPAL.md`: forbids `keyword_map`, `domain_map`, and `role_map`
- Claude `CLAUDE.md`: forbids `keyword_map`, `domain_map`, and `role_map`

Conclusion: no keyword routing map was generated; the only matches are explicit ban text.

## Copy Boundary Checks

| Check | Generic | Claude |
| --- | --- | --- |
| no `official/pals` directory copied | pass | pass |
| no `workspace/organization/contacts/pals.json` copied | pass | pass |
| no `.agentpal/memory` copied | pass | pass |
| no `.agentpal/reports` copied | pass | pass |
| no `.agentpal/evals` copied | pass | pass |
| no unresolved `REPLACE_WITH_` / `<absolute ...>` placeholders | pass | pass |
| no secret / credential placeholder matches | pass | pass |

## Conclusion

R93-C local thin binding simulation passed for the intended temporary-project file surface and cleanliness boundary.

The only follow-up is a non-applied template note: Claude `project.json` should likely add `agentpal_project_record` for parity with the docs and protected block language. This report records the issue without modifying shared templates.
