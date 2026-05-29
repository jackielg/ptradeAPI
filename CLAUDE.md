# CLAUDE.md — ptradeAPI

## Project
PTrade 平台 API 参考文档，包含中英文版本及券商版本差异。手动维护，非可执行代码。

## Rules
- 本目录为参考文档，不自动修改
- 策略开发时参考此目录和 SimTradeLab/docs/PTrade_API_Complete_Reference.md

## Out of Scope
- 不自动生成或修改任何文档内容
- IMPORTANT: 永远不要推送到 upstream (kay-ou) 仓库，只允许 push origin (jackielg)
- 不自动推送到远程仓库（需用户确认后才能 push origin）

<!-- gitnexus:start -->
# GitNexus — Code Intelligence

索引: **ptradeAPI** (4775 symbols, 4970 relationships, 0 execution flows)。参考文档项目。

## Always Do
- 修改符号前: `gitnexus_impact({target: "symbolName", direction: "upstream"})` 并报告影响范围
- 提交前: `gitnexus_detect_changes()` 验证影响范围
- HIGH/CRITICAL 风险警告必须报告给用户

## Never Do
- 不运行 impact 分析就编辑符号
- 忽略 HIGH/CRITICAL 风险警告
- 用 find-replace 重命名符号 → 用 `gitnexus_rename`

> 索引过期时: `npx gitnexus analyze`
<!-- gitnexus:end -->
