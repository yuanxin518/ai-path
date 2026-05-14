# 02 — Agent 编排层

**做什么**：让 AI 不只是聊天，而是自主执行多步任务、调用工具、分发子任务。

**位置**：在客户端之上，是 AI 从"对话"到"干活"的关键飞跃。

---

## 工具清单

| 工具 | 状态 | 核心能力 |
|------|------|---------|
| **[DeepSeek TUI Agent Mode](https://github.com/deepseek-ai/deepseek-tui)** | ✅ 主力在用 | 多步任务、子代理分发、MCP 集成、Checklist 跟踪 |
| **[Claude Code Agent](https://docs.anthropic.com/en/docs/claude-code/)** | ✅ 主力在用 | 端到端编码、Shell 执行、文件编辑、Lint/Test 门 |
| Codex CLI | 🔄 试用过 | OpenAI 开源，YOLO 模式 |
| OpenCode | 📌 待试用 | 开源 Codex 替代 |
| Cursor Agent | 🔄 试用过 | IDE 内 Agent 体验 |
| Windsurf Cascade | 🔄 试用过 | 自动多步操作，类 Agent 体验 |

---

## Agent 核心概念

### 子代理（Sub-agent）

现代 Agent 系统可以**分发子任务**给多个子 Agent 并行执行：

- DeepSeek TUI：`agent_open/per_agent_close`，支持批量并行子代理
- Claude Code：`/add-context-files`、`/init` 等内置命令
- Codex CLI：多 Task 管理

### 执行模式

| 模式 | 说明 | 适合场景 |
|------|------|---------|
| Agent（默认） | 自主思考 → 执行 → 验证循环 | 复杂多步任务 |
| Plan | 先规划再执行，审批后才动手 | 批量重构、敏感操作 |
| YOLO | 不审批直接执行 | 脚本化批量任务、信任区域 |

### 工具调用

Agent 的核心能力在于能调用外部工具来扩展能力：

- 文件读写、搜索
- Shell 执行
- MCP 服务（数据库、API、浏览器……）
- 自定义插件/Skills

---

## 实践笔记

### DeepSeek TUI Agent

```
特点:
  - 强子代理并行能力（最多 20 个并发）
  - RLM 持久化长上下文分析
  - Checklist / Plan 双轨跟踪
  - 多 Skills 支持

适用: 需要大量并行子任务、长上下文分析的场景
```

### Claude Code Agent

```
特点:
  - 代码理解最深（Claude 模型加成）
  - /review 自动代码审查
  - 原生 Shell + 文件编辑集成
  - 与 Claude Projects 无缝衔接

适用: 编码密集型任务、代码重构、复杂 debug
```

---

> **[← 返回根 README](../README.md)**
