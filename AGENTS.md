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

This project is indexed by GitNexus as **ptradeAPI** (4773 symbols, 4970 relationships, 0 execution flows).

> Index stale? Run `node .gitnexus/run.cjs analyze --index-only` from the project root — it auto-selects an available runner. No `.gitnexus/run.cjs` yet? Bootstrap with `npx`, `bunx`, or `pnpm dlx` — e.g. `bunx gitnexus@latest analyze` (npm 11 npx crash; #1939).

## Always Do

- **MUST run impact before editing.** Use `impact({target: "symbolName", direction: "upstream"})` or `node .gitnexus/run.cjs impact "symbolName" --direction upstream --repo .`; report callers, processes, and risk. Never substitute grep for graph analysis.
- **MUST analyze graph changes before committing.** Use `detect_changes({scope: "all"})` (MCP) or `node .gitnexus/run.cjs detect-changes --scope all --repo .` (CLI fallback). `partial: true` or `truncated: true` is not a clean check — a zero means unseen, not unaffected; re-run it. For regression review: `detect_changes({scope: "compare", base_ref: "main"})` or `node .gitnexus/run.cjs detect-changes --scope compare --base-ref "main" --repo .`.
- MUST warn on HIGH/CRITICAL `risk` pre-edit; never use `riskSharedAxes` to waive a HIGH/CRITICAL `risk` warning. Compare File/symbol: MCP File omits axes; Graph-RAG expands File.
- **MUST treat `risk: UNKNOWN` as unresolved, not as low.** An empty caller set is not evidence the symbol is unused — it can also mean the callers are not resolvable by the index (plain-object property access, dynamic dispatch, cross-language calls). `impact` pairs `UNKNOWN` with a `riskNote` saying so. Confirm with a text search before treating the symbol as safe to change or delete; do not proceed on the strength of a zero.
- **MUST use `query({search_query: "concept"})` for concepts/flows, `context({name: "symbolName"})` for a named symbol, or `impact` for blast radius, on read-only callers, dependencies, imports, or execution flow.** Graph first; text search only for empty/`UNKNOWN`/literals.
- For security review, `explain({target: "fileOrSymbol"})` lists taint findings (source→sink flows; needs `analyze --pdg`).

## Never Do

- NEVER edit a function, class, or method before MCP/CLI impact analysis.
- NEVER ignore HIGH or CRITICAL risk warnings from impact analysis, and never read `UNKNOWN` as an all-clear — it means the walk could not answer, which is the one verdict that requires confirming by other means.
- NEVER rename symbols with find-and-replace — use `rename` which understands the call graph.
- NEVER commit before MCP/CLI graph change analysis.

## Resources

| Resource | Use for |
| --- | --- |
| `gitnexus://repo/ptradeAPI/context` | Codebase overview, check index freshness |
| `gitnexus://repo/ptradeAPI/clusters` | All functional areas |
| `gitnexus://repo/ptradeAPI/processes` | All execution flows |
| `gitnexus://repo/ptradeAPI/process/{name}` | Step-by-step execution trace |

## CLI

| Task | Read this skill file |
| --- | --- |
| Understand architecture / "How does X work?" | `.claude/skills/gitnexus-exploring/SKILL.md` |
| Blast radius / "What breaks if I change X?" | `.claude/skills/gitnexus-impact-analysis/SKILL.md` |
| Trace bugs / "Why is X failing?" | `.claude/skills/gitnexus-debugging/SKILL.md` |
| Rename / extract / split / refactor | `.claude/skills/gitnexus-refactoring/SKILL.md` |
| Tools, resources, schema reference | `.claude/skills/gitnexus-guide/SKILL.md` |
| Index, status, clean, wiki CLI commands | `.claude/skills/gitnexus-cli/SKILL.md` |

<!-- gitnexus:end -->
