# Direct Pal Call Self-Test

Verify `/pal Name` and `@Name` direct calls.

## Inputs

```text
/pal Atlas 帮我把这个开发任务拆成下一步。
```

```text
@Quinn 帮我检查这个验收标准是否充分。
```

```text
/pal Echo Please review this plan.
```

## Pass

- known Pal names resolve from current contacts / registry by display name or alias
- the selected Pal answers with its own prefix
- the selected Pal uses its identity, Output Contract, and at least one relevant asset or explicit fallback method
- unknown Pal is not invented
- unknown Pal response says the Pal is not registered or indexed
- direct call does not become a permanent default listener change

## Fail

- the runtime treats `/pal Name` as a shell command
- Mira impersonates an unknown Pal
- the answer only changes the speaker name without Pal assets or fallback
- direct call starts an independent Agent process

