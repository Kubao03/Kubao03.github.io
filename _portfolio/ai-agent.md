---
title: "多模型 AI 问答 Agent"
excerpt: "支持 PDF-RAG、多模型切换、流式输出，已部署上线"
collection: portfolio
date: 2026-02-01
---

**技术栈**：LangChain · FastAPI · pgvector · Next.js · RAG · SSE

基于 LangChain ReAct 构建对话 Agent，注册 Tavily 搜索、Wikipedia、时间查询、文档检索四类工具，支持 DeepSeek / Gemini / Qwen 多模型动态切换。

- PDF 上传与 RAG 问答：文档向量化存入 **PostgreSQL + pgvector**，以 thread_id 过滤实现用户间数据隔离
- 使用 **AsyncPostgresSaver Checkpointer** 持久化对话线程，实现多轮记忆与历史恢复
- 前端经 **SSE** 实时推送流式输出，展示工具调用过程

[GitHub →](https://github.com/Kubao03/Agent) · [Live Demo →](https://cry-ai-agent.vercel.app)
