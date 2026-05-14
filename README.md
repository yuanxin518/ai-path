# AI Path

从 **使用 AI** 到 **每个环节能介入什么工具**，一条完整的技术链路地图。

> 这是一个个人工具清单仓库。每个节点不追求大而全，只放自己用过、觉得好的东西。
> 随着工具链进化，随时往里加。

---

## 全链路总览

```
  00                 01               02                03                  04             05
┌─────────┐    ┌────────────┐    ┌──────────┐    ┌─────────────┐    ┌────────────┐    ┌──────────┐
│  LLM    │ →  │  客户端    │ →  │  Agent   │ →  │  工具/插件   │ →  │  上下文     │ →  │  工作流   │
│  后端    │    │  交互层    │    │  编排层   │    │  扩展层     │    │  知识管理   │    │  自动化   │
└─────────┘    └────────────┘    └──────────┘    └─────────────┘    └────────────┘    └──────────┘
```

| 节点 | 做什么 | 你在这里选什么 |
|------|--------|---------------|
| [00 — LLM 后端](./00-llm-backends/) | 选哪个大模型 | DeepSeek / Claude / OpenAI / Gemini |
| [01 — 客户端交互层](./01-clients/) | 用什么聊/调 AI | TUI / Web / IDE 插件 / API |
| [02 — Agent 编排层](./02-agents/) | 怎么让 AI 自主干活 | Agent 模式 / 子代理 / 多步任务 |
| [03 — 工具/插件扩展](./03-tools-extensions/) | AI 能调用什么 | MCP 服务 / Skills / Shell 工具 |
| [04 — 上下文与知识管理](./04-context-knowledge/) | 怎么喂上下文 | 项目上下文 / RLM / 记忆 / RAG |
| [05 — 工作流与自动化](./05-workflows/) | 怎么串起来跑 | CI 集成 / Git 钩子 / 定时任务 |

---

## 节点与工具映射

### [00 — LLM 后端](./00-llm-backends/)

使用 AI 的第一步：选一个底层的语言模型或 API 服务。

- **DeepSeek** — V4 系列（Flash / Pro），性价比高，长上下文
- **Anthropic Claude** — Sonnet / Opus，代码能力强
- **OpenAI** — GPT-4o / o3，生态最广
- **Google Gemini** — 多模态原生

每个后端有各自的 API 风格、定价、缓存策略。

### [01 — 客户端交互层](./01-clients/)

选好模型后，怎么跟它交互。

- **DeepSeek TUI** — 终端界面，支持 Agent 模式、MCP、Skills
- **Claude Code** — Anthropic 官方终端客户端
- **Claude.ai / ChatGPT Web** — 官方网页版
- **Cursor / Copilot** — IDE 内 AI 增强
- **OpenAI API / DeepSeek API** — 直接调 API

### [02 — Agent 编排层](./02-agents/)

AI 不只是聊天——让它自主执行任务。

- **DeepSeek TUI Agent Mode** — 多步任务执行、子代理分发
- **Claude Code Agent** — 端到端编码代理
- **Codex CLI / OpenCode** — 开源替代方案
- **Windsurf / Cursor Agent** — IDE 内 Agent

### [03 — 工具/插件扩展层](./03-tools-extensions/)

AI 能调用什么外部工具来丰富能力。

- **MCP 服务器** — Model Context Protocol 服务，让 AI 访问文件、数据库、API
- **Skills** — DeepSeek 本地指令技能包，可复用的小块能力
- **Shell 工具** — 终端命令、脚本、管道集成

### [04 — 上下文与知识管理](./04-context-knowledge/)

AI 知道的取决于你喂了什么。

- **项目上下文** — AGENTS.md / CLAUDE.md 等工作区指令
- **RLM（长上下文）** — 递归大窗口处理，1M tokens
- **Memory** — 持久化记忆（memory.md）
- **RAG** — 检索增强生成

### [05 — 工作流与自动化](./05-workflows/)

把以上所有节点串成自动化流程。

- **CI/CD 集成** — 测试门、代码审查
- **Git 钩子** — 提交前自动检查
- **定时任务** — 批量处理/报告
- **多 Agent 协议** — 任务链、子代理协调

---

## 使用方式

1. 从 [00 节点](./00-llm-backends/) 开始，顺着链路往下走
2. 每个节点 README 里列出了具体的工具/插件和我的使用评价
3. 看到你感兴趣的，点进去看详情
4. 如果你也有好的工具推荐，欢迎提 Issue 或 PR

## 为什么做这个

市面上有很多 AI 工具清单，但缺一个**从使用视角出发、按链路节点组织的个人地图**。
这个仓库就是我自己用的——好记性不如烂笔头。

---

**License**: MIT
