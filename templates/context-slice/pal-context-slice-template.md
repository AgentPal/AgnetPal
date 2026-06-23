# Pal Context Slice Template

```yaml
pal_context_slice:
  pal_name:
  task_goal:
  index_known_count:
  index_known_source: []
  index_only_paths_summary:
  content_read_count:
  content_read_paths: []
  required_pal_files:
    - PAL.md
    - AGENTS.md
    - SKILL.md
    - pal.json
    - core/output-contract.md
  selected_skills: []
  selected_knowledge: []
  selected_runbooks: []
  project_files_needed: []
  memory_needed: []
  output_contract:
  fallback_if_missing:
  not_content_read_note: "Paths known from Pal indexes or registry are not content reads unless listed under content_read_paths."
```

## Use

Use after Mira selects an owner Pal or when the user directly calls `/pal Name`.
