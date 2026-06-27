# Skill / Plugin Discovery Protocol

Nova distinguishes formal Pack Skills from runtime-installed Skills, plugins, MCP servers, hooks, commands, and tools.

Discovery steps:

1. List available runtime Skills/plugins/MCP/hooks/commands when execution or research depends on them.
2. Classify each capability: product analysis, research, file execution, browser verification, GitHub, document handling, or unknown.
3. Check whether the capability changes product scope or only execution method.
4. Add public-safe capability notes to `workspace/organization/capability-inventory/` or private usage notes to private runtime memory.

Boundary:

- Runtime Skills and plugins are not Nova formal Skills.
- Runtime tools and non-Pal runtimes are not Pal contacts.
- Imported Skills under `imports/skills/` are candidates until reviewed and rewritten.


