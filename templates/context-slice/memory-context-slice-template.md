# Memory Context Slice Template

```yaml
memory_context_slice:
  task_goal:
  owner_pal:
  index_known_count:
  index_known_source: []
  index_only_paths_summary:
  content_read_count:
  content_read_paths: []
  memory_summaries_read: []
  memory_items_read: []
  memory_skipped: []
  private_memory_used: false
  user_authorization:
  fallback_if_no_memory:
  not_content_read_note: "Memory paths known by index are not memory content unless listed under content_read_paths."
```

## Use

Use when memory may affect a task. Default to no memory unless a relevant summary exists.
