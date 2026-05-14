# 00 — LLM 后端

**做什么**：选一个底层的语言模型或 API 服务作为 AI 能力的基座。

**位置**：全链路的起点。后面的客户端、Agent 都依赖这里的 API/SDK。

---

## 工具清单

| 工具 | 模型 | 状态 | 点评 |
|------|------|------|------|
| DeepSeek | V4 Flash / Pro / R1 | ✅ 主力在用 | 性价比高，长上下文（1M），Agent 模式支持好 |
| Anthropic Claude | Sonnet 4 / Opus 4 | ✅ 主力在用 | 代码能力强，Claude Code 深度集成 |
| OpenAI | GPT-4o / o3-mini | 🔄 偶尔用 | 生态最广，API 最成熟 |
| Google Gemini | Gemini 2.5 Pro | 🔄 偶尔用 | 多模态原生，超长上下文窗口 |

---

## 对比概要

| 方面 | DeepSeek | Claude | OpenAI | Gemini |
|------|----------|--------|--------|--------|
| 上下文窗口 | 1M tokens | 200K tokens | 128K tokens | 2M tokens |
| 定价（输入） | $0.07-0.27/M | $3-15/M | $2.5-10/M | $1.25-10/M |
| 代码能力 | 强 | 最强 | 强 | 中 |
| 中文能力 | 原生好 | 好 | 好 | 尚可 |
| 缓存支持 | ✅ 前缀缓存 | ✅ 项目缓存 | ✅ Prompt 缓存 | — |

> ⚡ **提示**：最新定价以官方为准，这里只是大致对比。

---

## 使用场景推荐

- **日常编码** → DeepSeek V4 Flash（低成本+快）
- **复杂架构/重构** → Claude Sonnet（代码理解最深）
- **高吞吐 API** → DeepSeek / OpenAI（生态兼容性好）
- **长文档分析** → DeepSeek V4 / Gemini（原生 1M+ 窗口）

---

> **[← 返回根 README](../README.md)**
