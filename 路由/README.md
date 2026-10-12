# 路由

API 代理层，为终端 CLI 工具提供统一的供应商切换、路由和负载均衡能力。

---

## CLIProxyAPI

为 Claude Code 等 CLI 终端提供兼容的 API 代理接口，支持多账号轮询负载均衡。

- [GitHub](https://github.com/router-for-me/CLIProxyAPI)

---

## magpie

菜单栏一处切换所有 Agent 的模型：Claude Code 接 Kimi、Codex 接 DeepSeek、Gemini CLI 接 GLM。本地网关（127.0.0.1:3425）统一翻译 Anthropic / OpenAI / Gemini 协议，配额用完自动故障转移到下一个账号或模型。作为 cc-switch 的替代，还支持直接导入 CC Switch 的供应商配置。

- [GitHub](https://github.com/yetone/magpie)
- [官网与下载](https://usemagpie.ai)

---

> **[← 返回根 README](../README.md)**
