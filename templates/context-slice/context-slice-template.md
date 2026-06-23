# Context Slice Template

```yaml
context_slice:
  task_goal:
  active_project:
  selected_pal:
  reason_for_slice:
  index_known_count:
  index_known_source: []
  index_only_paths_summary:
  index_only_not_content_read:
  not_content_read_note: "Some file paths were discovered through directory index or registry lookup. They were not opened or read as content."
  content_read_count:
  content_read_paths: []
  included_files: []
  included_assets: []
  excluded_context: []
  memory_summary_used: []
  token_budget_note:
  unresolved_context_gap: []
```

## Use

Use this to describe the minimum context loaded for a task. It is a navigation record, not a command to load all listed directories.
