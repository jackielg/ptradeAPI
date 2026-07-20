# AGENTS.md — ptradeAPI

## 定位
PTrade 平台 API 参考文档（手动维护），是 SimTradeLab 沙箱实现和策略开发的"金标准"。
包含中英文版本、券商版本差异、行业概念数据说明。

## 项目类型
**参考文档项目** — 本目录以 Markdown 文档为主，**没有可执行 Python 代码**。
仅 `check_links.py`（链接检查）和 `example.py`（最小示例）两个工具脚本。

## 关键命令
- 检查链接: `python check_links.py`

## 内容结构
- `docs/README.md` — 文档入口
- `docs/getting-started/` — 新手入门
- `docs/api-reference/` — API 参考（中文）
- `docs/api-reference-en/` — API 参考（英文）
- `docs/api-classification.md` — API 分类
- `docs/industry-concept-data.md` — 行业/概念数据
- `docs/version-differences.md` — 券商版本差异
- `docs/advanced/` — 高级主题
- `docs/original/` — 原始抓取的官方文档
- `docs/versions/` — 历次抓取版本快照
- `docs/examples.md` — 使用示例
- `example.py` — 最小 Python 示例
- `README.md` / `README_CN.md` / `README_DE.md` — 项目说明

## 规则

### 文档维护
- 本目录为**参考文档**，**不自动修改**
- 新增/更新 API 必须基于 PTrade 官方最新发布
- 策略开发时参考本目录 + `SimTradeLab/docs/PTrade_API_Complete_Reference.md`
- 官方文档原文保留在 `docs/original/`，编辑过的版本在 `docs/api-reference/`

### 跨项目角色
- 本目录是 PTrade API 的"事实标准"
- SimTradeLab 的 ptrade/ 沙箱实现必须与本文档**对齐**
- SimTradeData 的 `field_mappings.py` 必须映射到本文档定义的 PTrade 列名
- 三项目对 PTrade API 的理解必须**统一**

### 工具脚本
- `check_links.py` 用于检查文档内链完整性
- `example.py` 是最小调用示例，运行前需先安装 SimTradeLab

## Out of Scope
- 🚫 永远不要推送到 upstream (kay-ou) 仓库
- 🚫 不自动生成或修改任何文档内容（除非用户明确要求）
- 不自动推送到远程仓库（需用户确认后才能 push origin）


<!-- gitnexus:start -->
# GitNexus — Code Intelligence

This project is indexed by GitNexus as **ptradeAPI** (4771 symbols, 4968 relationships, 0 execution flows). Use the GitNexus MCP tools to understand code, assess impact, and navigate safely.

> Index stale? Run `node .gitnexus/run.cjs analyze` from the project root — it auto-selects an available runner. No `.gitnexus/run.cjs` yet? `npx gitnexus analyze` (npm 11 crash → `npm i -g gitnexus`; #1939).

## Always Do

- **MUST run impact analysis before editing any symbol.** Before modifying a function, class, or method, run `impact({target: "symbolName", direction: "upstream"})` and report the blast radius (direct callers, affected processes, risk level) to the user.
- **MUST run `detect_changes()` before committing** to verify your changes only affect expected symbols and execution flows. For regression review, compare against the default branch: `detect_changes({scope: "compare", base_ref: "main"})`.
- **MUST warn the user** if impact analysis returns HIGH or CRITICAL risk before proceeding with edits.
- When exploring unfamiliar code, use `query({search_query: "concept"})` to find execution flows instead of grepping. It returns process-grouped results ranked by relevance.
- When you need full context on a specific symbol — callers, callees, which execution flows it participates in — use `context({name: "symbolName"})`.
- For security review, `explain({target: "fileOrSymbol"})` lists taint findings (source→sink flows; needs `analyze --pdg`).

## Never Do

- NEVER edit a function, class, or method without first running `impact` on it.
- NEVER ignore HIGH or CRITICAL risk warnings from impact analysis.
- NEVER rename symbols with find-and-replace — use `rename` which understands the call graph.
- NEVER commit changes without running `detect_changes()` to check affected scope.

## Resources

| Resource | Use for |
|----------|---------|
| `gitnexus://repo/ptradeAPI/context` | Codebase overview, check index freshness |
| `gitnexus://repo/ptradeAPI/clusters` | All functional areas |
| `gitnexus://repo/ptradeAPI/processes` | All execution flows |
| `gitnexus://repo/ptradeAPI/process/{name}` | Step-by-step execution trace |

## CLI

| Task | Read this skill file |
|------|---------------------|
| Understand architecture / "How does X work?" | `.claude/skills/gitnexus/gitnexus-exploring/SKILL.md` |
| Blast radius / "What breaks if I change X?" | `.claude/skills/gitnexus/gitnexus-impact-analysis/SKILL.md` |
| Trace bugs / "Why is X failing?" | `.claude/skills/gitnexus/gitnexus-debugging/SKILL.md` |
| Rename / extract / split / refactor | `.claude/skills/gitnexus/gitnexus-refactoring/SKILL.md` |
| Tools, resources, schema reference | `.claude/skills/gitnexus/gitnexus-guide/SKILL.md` |
| Index, status, clean, wiki CLI commands | `.claude/skills/gitnexus/gitnexus-cli/SKILL.md` |

<!-- gitnexus:end -->
