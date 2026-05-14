# 01 — 客户端交互层

**做什么**：选好 LLM 后端后，用什么客户端/界面跟它交互。

**位置**：在 LLM 之上，直接面对用户。决定你的日常操作体验。

---

## 工具清单

### 终端客户端

| 工具 | 状态 | 点评 |
|------|------|------|
| [DeepSeek TUI](https://github.com/deepseek-ai/deepseek-tui) | ✅ 主力在用 | 终端原生，支持 Agent、MCP、Skills，DeepSeek 官方出品 |
| [Claude Code](https://docs.anthropic.com/en/docs/claude-code/) | ✅ 主力在用 | Anthropic 官方终端客户端，深度绑定 Claude |
| [Codex CLI](https://github.com/openai/codex) | 🔄 试用过 | OpenAI 开源终端 agent |
| [aider](https://github.com/paul-gauthier/aider) | 🔄 试用过 | 开源，支持多模型，pair programming 模式 |

### Web 客户端

| 工具 | 状态 | 点评 |
|------|------|------|
| [Claude.ai](https://claude.ai) | ✅ 在用 | 官方网页版，Projects 功能好用 |
| [ChatGPT](https://chatgpt.com) | 🔄 偶尔用 | GPT-4o/o3，生态集成最好 |
| [DeepSeek Chat](https://chat.deepseek.com) | 🔄 偶尔用 | 免费，长上下文流畅 |
| [Gemini](https://gemini.google.com) | 🔄 偶尔用 | 多模态体验好 |

### IDE 客户端

| 工具 | 状态 | 点评 |
|------|------|------|
| [Cursor](https://cursor.sh) | 🔄 试用过 | VS Code fork，Agent 模式好用 |
| [GitHub Copilot](https://github.com/features/copilot) | ✅ 在用 | 代码补全最成熟，Agent 模式也在迭代 |
| [Windsurf](https://codeium.com/windsurf) | 🔄 试用过 | 类 Cursor 体验，Cascade 模式不错 |

### API 直接调用

| 工具 | 状态 | 点评 |
|------|------|------|
| DeepSeek API | ✅ 在用 | OpenAI 兼容接口，灵活 |
| OpenAI API | 🔄 偶尔用 | 生态最完善，SDK 丰富 |
| Anthropic API | 🔄 偶尔用 | Message API，Claude 独有能力 |

---

## 我的工作流

```
日常编码
  ├── 复杂任务 → Claude Code（代码理解最强）
  └── 快速任务 → DeepSeek TUI（响应快、成本低）

聊天/研究
  ├── 技术讨论 → Claude.ai（Projects + 上下文管理好）
  └── 日常查询 → DeepSeek Chat / ChatGPT

IDE 内
  └── Copilot → 补全 + 简单 Agent 任务
```

---

> **[← 返回根 README](../README.md)**
