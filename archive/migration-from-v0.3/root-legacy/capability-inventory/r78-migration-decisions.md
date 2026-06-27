# R78 Migration Decisions

Generated: 2026-06-28 00:54:36 +08:00

This table records the R78 staged decision before moving files. Low-risk standard, example, organization-record, and usage-memory files are migrated now. Root README files remain as compatibility pointers.

| source_path | target_path | classification | migrate_now | reason | reference_update_required | risk |
| --- | --- | --- | --- | --- | --- | --- |
| `capabilities/agent-capability-matrix.md` | `standards/capability-inventory/agent-capability-matrix.md` | standard | yes | capability matrix is a standard judgement input, not an active runtime record | yes | low |
| `capabilities/mcp-profiles/README.md` | `examples/capability-inventory/mcp-profiles/README.md` | example | yes | profile directory README describes example profile shape | yes | low |
| `capabilities/model-capability-matrix.md` | `standards/capability-inventory/model-capability-matrix.md` | standard | yes | capability matrix is a standard judgement input, not an active runtime record | yes | low |
| `capabilities/model-profiles/generic-economy-model.example.json` | `examples/capability-inventory/model-profiles/generic-economy-model.example.json` | example | yes | sample profile JSON belongs under examples | yes | low |
| `capabilities/model-profiles/generic-strong-model.example.json` | `examples/capability-inventory/model-profiles/generic-strong-model.example.json` | example | yes | sample profile JSON belongs under examples | yes | low |
| `capabilities/model-profiles/README.md` | `examples/capability-inventory/model-profiles/README.md` | example | yes | profile directory README describes example profile shape | yes | low |
| `capabilities/pal-capability-matrix.md` | `standards/capability-inventory/pal-capability-matrix.md` | standard | yes | capability matrix is a standard judgement input, not an active runtime record | yes | low |
| `capabilities/pal-profiles/atlas-developer.example.json` | `examples/capability-inventory/pal-profiles/atlas-developer.example.json` | example | yes | sample profile JSON belongs under examples | yes | low |
| `capabilities/pal-profiles/mira-main.example.json` | `examples/capability-inventory/pal-profiles/mira-main.example.json` | example | yes | sample profile JSON belongs under examples | yes | low |
| `capabilities/pal-profiles/palsmith-pal-governor.example.json` | `examples/capability-inventory/pal-profiles/palsmith-pal-governor.example.json` | example | yes | sample profile JSON belongs under examples | yes | low |
| `capabilities/pal-profiles/quinn-quality.example.json` | `examples/capability-inventory/pal-profiles/quinn-quality.example.json` | example | yes | sample profile JSON belongs under examples | yes | low |
| `capabilities/pal-profiles/README.md` | `examples/capability-inventory/pal-profiles/README.md` | example | yes | profile directory README describes example profile shape | yes | low |
| `capabilities/pal-profiles/vega-research.example.json` | `examples/capability-inventory/pal-profiles/vega-research.example.json` | example | yes | sample profile JSON belongs under examples | yes | low |
| `capabilities/plugin-capability-matrix.md` | `standards/capability-inventory/plugin-capability-matrix.md` | standard | yes | capability matrix is a standard judgement input, not an active runtime record | yes | low |
| `capabilities/plugin-profiles/README.md` | `examples/capability-inventory/plugin-profiles/README.md` | example | yes | profile directory README describes example profile shape | yes | low |
| `capabilities/README.md` | `archive/migration-from-v0.3/root-legacy/capability-inventory/root-pointers/capabilities/README.md` | pointer | R79 | root compatibility pointer was archived after active references moved to new sources | archived | low |
| `capabilities/reasoning-profiles/README.md` | `examples/capability-inventory/reasoning-profiles/README.md` | example | yes | profile directory README describes example profile shape | yes | low |
| `capabilities/reasoning-profiles/reasoning-strengths.example.json` | `examples/capability-inventory/reasoning-profiles/reasoning-strengths.example.json` | example | yes | sample profile JSON belongs under examples | yes | low |
| `capabilities/runtime-profiles/claude-code.example.json` | `examples/capability-inventory/runtime-profiles/claude-code.example.json` | example | yes | sample profile JSON belongs under examples | yes | low |
| `capabilities/runtime-profiles/codex.example.json` | `examples/capability-inventory/runtime-profiles/codex.example.json` | example | yes | sample profile JSON belongs under examples | yes | low |
| `capabilities/runtime-profiles/generic-cli.example.json` | `examples/capability-inventory/runtime-profiles/generic-cli.example.json` | example | yes | sample profile JSON belongs under examples | yes | low |
| `capabilities/runtime-profiles/README.md` | `examples/capability-inventory/runtime-profiles/README.md` | example | yes | profile directory README describes example profile shape | yes | low |
| `capabilities/skill-capability-matrix.md` | `standards/capability-inventory/skill-capability-matrix.md` | standard | yes | capability matrix is a standard judgement input, not an active runtime record | yes | low |
| `capabilities/skill-profiles/generic-document-skill.example.json` | `examples/capability-inventory/skill-profiles/generic-document-skill.example.json` | example | yes | sample profile JSON belongs under examples | yes | low |
| `capabilities/skill-profiles/generic-web-research-skill.example.json` | `examples/capability-inventory/skill-profiles/generic-web-research-skill.example.json` | example | yes | sample profile JSON belongs under examples | yes | low |
| `capabilities/skill-profiles/README.md` | `examples/capability-inventory/skill-profiles/README.md` | example | yes | profile directory README describes example profile shape | yes | low |
| `capabilities/task-routing-matrix.md` | `standards/capability-inventory/task-routing-matrix-standard.md` | standard | yes | routing matrix must be reframed as AI judgement input standard | yes | medium |
| `runtime/current-runtime.md` | `workspace/organization/capability-inventory/runtimes/current-runtime.md` | current-organization-record | yes | current runtime placeholder belongs to central organization capability inventory | yes | low |
| `runtime/README.md` | `archive/migration-from-v0.3/root-legacy/capability-inventory/root-pointers/runtime/README.md` | pointer | R79 | root compatibility pointer was archived after active references moved to new sources | archived | low |
| `runtime/runtime-detection-protocol.md` | `standards/capability-inventory/runtime-detection-protocol.md` | standard | yes | manual/no-code runtime detection protocol is a standard | yes | medium |
| `runtime/runtime-refresh-log.md` | `workspace/organization/capability-inventory/runtimes/runtime-refresh-log.md` | usage-memory | yes | runtime refresh log is central usage/update record, not root standard | yes | low |
| `runtime/runtime-registry.md` | `workspace/organization/capability-inventory/runtimes/runtime-registry.md` | current-organization-record | yes | runtime registry placeholder belongs to central organization capability inventory | yes | low |
| `models/available-models.md` | `workspace/organization/capability-inventory/models/available-models.md` | current-organization-record | yes | available model placeholder is central organization record | yes | low |
| `models/model-profiles.md` | `standards/capability-inventory/model-profile-standard.md` | standard | yes | model profile fields are standard material | yes | low |
| `models/model-routing-policy.md` | `standards/capability-inventory/model-routing-policy.md` | standard | yes | policy is standard material and must preserve no keyword routing | yes | medium |
| `models/model-selection-memory.md` | `workspace/organization/capability-inventory/usage-memory/model-selection-memory.md` | usage-memory | yes | model selection memory is central usage memory | yes | low |
| `models/README.md` | `archive/migration-from-v0.3/root-legacy/capability-inventory/root-pointers/models/README.md` | pointer | R79 | root compatibility pointer was archived after active references moved to new sources | archived | low |
| `models/reasoning-strengths.md` | `standards/capability-inventory/reasoning-profile-standard.md` | standard | yes | reasoning profile language is standard material | yes | low |
| `plugins/installed-mcp.md` | `workspace/organization/capability-inventory/mcp/installed-mcp.md` | current-organization-record | yes | installed MCP placeholder belongs to central organization record | yes | low |
| `plugins/installed-plugins.md` | `workspace/organization/capability-inventory/plugins/installed-plugins.md` | current-organization-record | yes | installed plugin placeholder belongs to central organization record | yes | low |
| `plugins/installed-skills.md` | `workspace/organization/capability-inventory/skills/installed-skills.md` | current-organization-record | yes | installed skill placeholder belongs to central organization record | yes | low |
| `plugins/plugin-scan-protocol.md` | `standards/capability-inventory/plugin-scan-protocol.md` | standard | yes | manual plugin discovery protocol is standard material | yes | medium |
| `plugins/plugin-usage-memory.md` | `workspace/organization/capability-inventory/usage-memory/plugin-usage-memory.md` | usage-memory | yes | plugin usage memory is central usage memory | yes | low |
| `plugins/README.md` | `archive/migration-from-v0.3/root-legacy/capability-inventory/root-pointers/plugins/README.md` | pointer | R79 | root compatibility pointer was archived after active references moved to new sources | archived | low |
