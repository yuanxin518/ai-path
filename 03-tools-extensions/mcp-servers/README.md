# MCP 服务器

## 什么是 MCP

Model Context Protocol（MCP）是一个开放协议，标准化了 AI 应用如何与外部工具/数据源交互。

> 类比：MCP 之于 AI ≈ USB 之于电脑 — 统一的接口，接入各种外设。

## 我用的 MCP 服务器

| 服务 | 用途 | 状态 | 来源 |
|------|------|------|------|
| GitHub MCP | 仓库管理、Issue/PR 操作 | ✅ 在用 | 官方/社区 |
| Filesystem MCP | 文件系统读写 | ✅ 在用 | DeepSeek TUI 内置 |
| Database MCP | 数据库查询 | 📌 待配 | 社区 |

> 💡 **提示**：MCP 生态还在快速膨胀，这里只列了我实际配置过的。
> 更多可用服务参考 [MCP 官方市场](https://mcp.composio.dev/)。

---

## 配置示例

### DeepSeek TUI (`~/.deepseek/config.toml`)

```toml
[mcp_servers.github]
transport = "stdio"
command = "npx"
args = ["-y", "@modelcontextprotocol/server-github"]

[mcp_servers.filesystem]
transport = "stdio"
command = "npx"
args = ["-y", "@modelcontextprotocol/server-filesystem"]
```

> 详细配置参看 DeepSeek TUI 文档。

---

> **[← 返回扩展层](../README.md) / [← 返回根 README](../../README.md)**
