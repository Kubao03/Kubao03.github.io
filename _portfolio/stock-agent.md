---
title: "股票深度研究助手"
excerpt: "基于 LangGraph 的多 Agent 投研系统，支持 A股/港股/美股，Token 消耗优化 60%"
collection: portfolio
date: 2026-03-01
---

**技术栈**：LangGraph · LangChain · FastAPI · Claude Code · MCP · HiTL

基于 LangGraph StateGraph 构建 Planner → Executor → Reporter 三阶段 Agent 流水线，输入股票代码后自动生成带来源标注的结构化投研报告，支持 A 股 / 港股 / 美股三个市场。

- Executor 使用 **Send API** 实现并行 Sub-Agent 调度，每个 Sub-Agent 基于 ReAct 自主调用 AKShare MCP 与 Tavily 工具
- 引入两处 **Human-in-the-Loop**，分别在任务规划后与子任务完成后暂停审核
- 通过 **LangSmith** 追踪优化并行工具调用策略，Token 消耗从 183.8k 降至 74.3k（**-60%**）

[GitHub →](https://github.com/Kubao03/deepresearch)
