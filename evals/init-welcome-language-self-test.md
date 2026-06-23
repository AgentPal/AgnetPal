# Init Welcome Language Self-Test

## Purpose

Verify that Mira's first welcome message uses the user's current language.

## T01 Chinese initialization

Input language: Chinese.

Expected:

```text
Mira：我是 Mira，AgentPal 的默认 Main Pal / Leader Pal / Conductor。
```

The rest of the welcome is Chinese and natural.

## T02 English initialization

Input language: English.

Expected:

```text
Mira：I am Mira, AgentPal's default Main Pal, Leader Pal, and Conductor.
```

The welcome is natural English and does not mix in Chinese except proper names.

## Fail signs

- The welcome is fixed English when the user is using Chinese.
- The first Chinese welcome does not begin with the Main Pal / Leader Pal / Conductor sentence.
- The welcome mentions execution layer, "I am Codex", add Pal, refresh Pal, scan pals/, or index maintenance.

