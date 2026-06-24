# Project JSON Template

```json
{
  "schema": "agentpal.project.v0.1",
  "binding_version": "0.1.0-rc.1",
  "binding_created_at": "REPLACE_WITH_ISO_TIMESTAMP",
  "project_name": "REPLACE_WITH_EXTERNAL_PROJECT_NAME",
  "active_project_root": "REPLACE_WITH_EXTERNAL_PROJECT_ROOT",
  "active_project_role": "user_project",
  "agentpal_workspace_root": "REPLACE_WITH_AGENTPAL_WORKSPACE_PATH",
  "agentpal_workspace_role": "pal_workspace_reference",
  "runtime_hint": "REPLACE_WITH_RUNTIME_HINT",
  "active_mode": "simple-pal-mode-only",
  "agentpal_enabled": true,
  "project_bound_mode": true,
  "read_core_from_agentpal_workspace": true,
  "core_gate_paths": [
    "core/agentpal-core-gate.md",
    "core/first-pal-gate.md",
    "core/simple-pal-mode-runtime-contract.md",
    "core/deliverable-aware-task-judgement-gate.md",
    "core/main-pal-conductor-gate.md",
    "core/runtime-adapter-shared-contract.md",
    "core/project-binding-thin-contract.md",
    "core/runtime-response-gate.md"
  ],
  "pal_source_of_truth": [
    "contacts/pals.json",
    "registry/pal.index.json"
  ],
  "default_main_pal": {
    "id": "mira-main",
    "display_name": "Mira",
    "paths": [
      "pals/Mira-main/PAL.md",
      "pals/Mira-main/core/output-contract.md"
    ]
  },
  "root_instruction_blocks": {
    "begin_marker": "<!-- BEGIN AGENTPAL WORKGROUP -->",
    "end_marker": "<!-- END AGENTPAL WORKGROUP -->"
  },
  "claude_code_binding": {
    "project_instruction_file": "CLAUDE.md",
    "local_settings_file": ".claude/settings.local.json",
    "additional_directories_setting": "permissions.additionalDirectories"
  },
  "remove_policy": {
    "delete_agentpal_dir": true,
    "remove_root_instruction_blocks_only": true,
    "remove_claude_additional_directory_entry": true,
    "do_not_delete_agentpal_workspace": true,
    "do_not_delete_project_source": true
  }
}
```

This file is binding metadata only. It is not a copied Pal roster or a copied protocol bundle.

Pal source of truth remains in the AgentPal workspace:

- `contacts/pals.json`
- `registry/pal.index.json`

Runtime adapters should read current core gates from `agentpal_workspace_root`.
