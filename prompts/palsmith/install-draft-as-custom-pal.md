# Install A Draft Pal Pack As A User Custom Pal

Copy this prompt into AgentPal when you want PalSmith to plan a no-code installation from a reviewed draft Pal Pack to a user custom Pal.

```text
/pal PalSmith 请把这个草稿 Pal Pack 安装为我的用户自定义 Pal。

草稿 Pal Pack 路径：
<paste-draft-pal-pack-path>

目标用途：
- 私有使用 / 团队内部使用 / 某个项目中临时可用：

请先做安装前检查，不要直接写文件。

请先输出：
1. 草稿路径是否存在，以及你会读取哪些文件；
2. 已有质量 / 使用回归证据是否足够；
3. 建议的用户自定义 Pal 目标路径；
4. 会复制哪些文件；
5. 会排除哪些文件；
6. copied pal.json 需要改哪些字段；
7. 用户自定义索引是否需要更新；
8. 明确不会写 official/pals；
9. 明确不会改 workspace/organization/contacts；
10. 明确不会启用 discovery；
11. 明确不会生成 public Marketplace listing；
12. 回滚 / 撤销建议；
13. 安装后如何调用；
14. 需要我确认的精确写入范围。

在我明确确认前，不要创建目录、不要复制文件、不要修改 JSON、不要写报告。
```

Boundary:

- This prompt does not make the Pal official.
- This prompt does not add the Pal to central contacts.
- This prompt does not build an installer, scanner, CLI, connector, daemon, backend service, or Marketplace backend.
- Host runtime writes require explicit confirmation and evidence.
