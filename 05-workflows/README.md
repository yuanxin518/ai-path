# 05 — 工作流与自动化

**做什么**：把前面所有节点的能力串成自动化流程。

**位置**：全链路末端，从一次性操作升级为可重复的自动化。

---

## 能力分支

### CI/CD 集成

| 方式 | 用途 | 状态 |
|------|------|------|
| GitHub Actions + AI | AI 自动审核 PR、跑测试 | 🔄 偶尔用 |
| 本地 Git 钩子 | 提交前 lint/测试门 | ✅ 在用 |
| AI Review Gate | Agent 自动代码审查 | ✅ 在用 |

### 自动化脚本

| 工具 | 用途 | 状态 |
|------|------|------|
| `git hooks`（pre-commit） | 提交前自动检查 | ✅ 在用 |
| `cron` / `systemd timer` | 定时批量处理 | 🔄 偶尔用 |
| Fish Shell 别名/函数 | 常用操作一键执行 | ✅ 在用 |

### 多 Agent 工作流

| 模式 | 说明 | 使用平台 |
|------|------|---------|
| 子代理并行 | 独立子任务同时跑 | DeepSeek TUI |
| 任务链 | A 的输出是 B 的输入 | DeepSeek TUI / Claude Code |
| 子代理合并 | 多路并行后合入主任务 | DeepSeek TUI |

---

## 我的自动化实践

```
Git 提交流程
  1. pre-commit hook → lint + fmt
  2. AI 自动生成 commit message（可选）
  3. 推送后 AI Review Gate（可选）

日常开发
  ├── 新功能 → Agent 模式 + Checklist 跟踪
  └── 修 Bug → diagnose Skill 系统化排查

批量管理
  └── RLM + 子代理 → 代码库级批量分析/重构
```

---

> **[← 返回根 README](../README.md)**
