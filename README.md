# AI Path

从 **使用 AI** 到 **每个环节能介入什么工具**，一条完整的技术链路地图。

> 只放自己用过、觉得好的东西。随着工具链进化，随时往里加。

---

## 全链路总览

```
  00                 01               02                03                  04             05
┌─────────┐    ┌────────────┐    ┌──────────┐    ┌─────────────┐    ┌────────────┐    ┌──────────┐
│  LLM    │ →  │  客户端    │ →  │  Agent   │ →  │  工具/插件   │ →  │  上下文     │ →  │  工作流   │
│  后端    │    │  交互层    │    │  编排层   │    │  扩展层     │    │  知识管理   │    │  自动化   │
└─────────┘    └────────────┘    └──────────┘    └─────────────┘    └────────────┘    └──────────┘
```

| 节点 | 做什么 | 我在用的 |
|------|--------|---------|
| [00 — LLM 后端](./00-llm-backends/) | 选哪个大模型 | DeepSeek · Claude |
| [01 — 客户端](./01-clients/) | 用什么交互 | DeepSeek TUI · Claude Code |
| [02 — Agent](./02-agents/) | 怎么自主干活 | Agent 模式（两个客户端自带） |
| [03 — 工具/插件](./03-tools-extensions/) | 扩展 AI 能力 | MCP · Skills · Shell |
| [04 — 上下文](./04-context-knowledge/) | 喂什么给 AI | 项目指令 · Memory · RLM |
| [05 — 工作流](./05-workflows/) | 串起来自动化 | Git 钩子 · 子代理分发 |

---

## 我的工具栈（就这些）

[00 — LLM 后端](./00-llm-backends/)
- **DeepSeek** — V4 Flash / Pro
- **Claude** — Sonnet

[01 — 客户端](./01-clients/)
- **DeepSeek TUI** — 终端 AI 客户端
- **Claude Code** — 终端 AI 客户端

[02 — Agent](./02-agents/)
- **DeepSeek TUI Agent 模式** — 多步任务、子代理
- **Claude Code Agent** — 编码代理

[03 — 工具扩展](./03-tools-extensions/)
- **MCP 服务器** — AI 调外部服务
- **Skills** — 本地指令包
- **Shell 工具** — 终端命令

[04 — 上下文](./04-context-knowledge/)
- **AGENTS.md / CLAUDE.md** — 项目指令
- **Memory** — 跨会话记忆
- **RLM** — 长上下文分析

[05 — 工作流](./05-workflows/)
- **Git 钩子** — 提交前检查
- **子代理分发** — 并行任务

---

**License**: MIT
