# Ptrade API 文档

欢迎使用 Ptrade 量化交易 API 文档！

本文档旨在为您提供全面、清晰的 Ptrade API 使用指南。无论您是量化新手还是经验丰富的开发者，都能在这里找到所需的信息。

> 如需了解与 Ptrade 接口相关的官方接入说明与流程，请私信，我会提供“仅含官方信息来源”的参考路径。
> Ptrade开发者圈QQ群590529320

---

## 🚀 快速上手

如果您是初次接触 Ptrade，建议从这里开始。

-   **[快速入门](getting-started/quick-start.md)**：从新建策略、回测到开启第一笔交易，带您完整体验平台。
-   **[核心概念](getting-started/usage.md)**：理解策略的业务流程框架，包括 `initialize`, `handle_data` 等核心函数。

## 📚 API 参考

这里包含了所有 API 接口的详细说明和示例。

-   **[📖 API 完整参考](api-reference/)**：按模块分类的完整API文档导航
-   **[📋 API 分类汇总](api-classification.md)**：按功能分类的所有 API 接口速查表

## 📈 数据资源

了解平台提供的数据类型和分类标准。

-   **[财务数据](api-reference/financial-data.md)**：详细的财务数据接口说明，包括估值、资产负债表、利润表等。
-   **[行业与概念](industry-concept-data.md)**：证监会行业、聚源行业、地域和概念板块的完整分类数据。

## 💡 策略示例

从简单到复杂，提供了多个可直接运行的策略示例。

-   **[策略示例库](examples.md)**：包含双均线、MACD、网格交易、可转债套利等多种策略。

## ⚙️ 高级主题

-   **[版本差异对比](version-differences.md)**：对比社区版、国盛版、东莞版、山西证券版等不同版本的 API 功能差异
-   **[版本详细信息](versions/)**：各版本的详细功能对比和财务数据差异
-   **[常见问题 (FAQ)](advanced/faq.md)**：汇总了平台使用、数据、回测、交易等方面的常见问题
-   **[支持的库](advanced/supported-libraries.md)**：查看平台内建支持的第三方 Python 库列表
-   **[版本变更记录](advanced/version-changes.md)**：各版本的更新历史和变更记录


---

> 💡 **建议**: 新用户从 **[快速入门](getting-started/quick-start.md)** 开始，逐步了解平台功能。有经验的用户可直接查阅 **[API 分类汇总](api-classification.md)** 或 **[策略示例库](examples.md)**。
