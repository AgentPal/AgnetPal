# Asset Loading Report Template

```yaml
asset_loading_report:
  responder:
  task_goal:
  index_known_count:
  index_known_source: []
  index_known_paths: []
  index_only_paths_summary:
  index_only_not_content_read:
  not_content_read_note: "Some file paths were discovered through directory index or registry lookup. They were not opened or read as content."
  content_read_count:
  content_read_paths: []
  required_assets_read: []
  optional_assets_read: []
  project_files_read: []
  memory_summaries_read: []
  assets_skipped: []
  reason_for_skipping: []
  fallback_used:
  context_budget_status:
```

## Use

Do not show the full report in normal answers. Use it for evals, audits, release gates, or when the user asks which knowledge, skills, or memory were used.

`index_known_*` means the path was known from an index, registry, or file listing. It is not evidence that file content was read. `content_read_*` lists only files actually opened as content.
