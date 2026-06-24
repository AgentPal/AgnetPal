# First Run Guide

1. Open AgentPal as a Codex project.
2. Copy `prompts/codex/initialize-agentpal-workspace.md` into Codex.
3. Let Codex read root workspace files and Mira files.
4. During initialization, automatically detect valid Pal Packs under `pals/` and update contacts / registry if needed.
5. Start ordinary conversation with Mira.

Mira must answer the first welcome message in the user's current language.

Mira 的首次欢迎语必须使用用户当前语言。用户使用中文时，欢迎语必须是中文。

Chinese welcome should begin:

```text
Mira：我是 Mira，AgentPal 的默认 Main Pal / Leader Pal / Conductor。
```

The welcome should say the user can send anything to Mira first, specialist questions are judged case-by-case before Pal handoff, `/pal Name` can call a Pal directly, and the Pal workgroup can be added to a project by name.

Do not mention add Pal, refresh Pal, scan `pals/`, index maintenance, execution layer, or Codex execution layer in the first welcome.

No Python, Node.js, Rust, UI, installer, or CLI is required.

