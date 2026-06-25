# Use PalSmith

## Status

Current for AgentPal `v0.1.0-rc.1`.

PalSmith is the official Pal asset governance Pal. Use it when you want AgentPal to help create, inspect, import, export, version, or publish Pal Packs.

## Direct Call

```text
/pal PalSmith
```

Examples:

```text
/pal PalSmith 创建一个小红书运营 Pal
/pal PalSmith 创建一个跨境电商运营团队
/pal PalSmith 体检所有 Pal
/pal PalSmith 从 GitHub 导入这个 Pal Pack
/pal PalSmith 从本地目录导入 Pal
/pal PalSmith 导出 Research Pal，不含记忆
```

## What PalSmith Does First

PalSmith does not immediately write files. It first decides the permission level:

- L0 read-only inspection
- L1 suggested change
- L2 controlled write
- L3 high-risk write
- L4 core governance

For L2 or higher, PalSmith asks for confirmation before the Runtime changes files.

## Creating A Pal

PalSmith generates a Pal creation plan with proposed name, id, directory, role, direct call, aliases, responsibilities, root files, identity files, output contract, initial indexes, evals, and contacts / registry update plan.

Creating files is a controlled write.

## Importing A Pal

PalSmith stages imports first. GitHub and local imports are not trusted by default.

It checks core files, schema, version, memory/state/reports, sensitive files, executable risk, license, and ID conflicts before asking how to install.

## Exporting A Pal

PalSmith asks which export type to use: Clean Pack Export, With Memory Export, Template Export, Team Export, or Backup Export.

Clean Pack Export is recommended for public sharing. With Memory Export requires strong confirmation.

## Boundary

PalSmith is not a Runtime. The host Runtime performs real file edits, archive creation, downloads, deletion, publishing, or command execution and must provide evidence.
