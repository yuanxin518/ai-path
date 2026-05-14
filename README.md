<details>
<summary><b>AI 指令</b> — 技术链路地图维护助手（点击展开）</summary>

> 你是这个技术链路地图的维护助手。用户会告诉你用了什么工具，你负责判断它属于哪个阶段节点，更新 README 和流程图。
>
> 可用命令：
> - **添加技术栈** — 用户说「我用了 xxx」，你归类到对应节点，更新 Mermaid 流程图和 README
> - **添加阶段** — 用户说「新增一个叫 xxx 的阶段」，你创建新节点目录并接入流程图
> - **刷新地图** — 重新审查所有节点，确保流程图和内容一致

</details>

# AI Path

从 **使用 AI** 到 **每个环节能介入什么工具**，一条完整的技术链路地图。

> 只放自己用过、觉得好的东西。随着工具链进化，随时往里加。

---

## 当前链路

```mermaid
flowchart TD
    subgraph N00["大模型"]
        direction TB
        DS1["DeepSeek V4 Flash"]
        DS2["DeepSeek V4 Pro"]
    end
    style N00 fill:#dbeafe,stroke:#3b82f6,stroke-width:2px,color:#1e40af

    subgraph N01["路由"]
        direction TB
        CPA["CLIProxyAPI"]
    end
    style N01 fill:#fef3c7,stroke:#f59e0b,stroke-width:2px,color:#92400e

    subgraph N02["终端"]
        direction TB
        TUI["DeepSeek TUI"]
        CC["Claude Code"]
    end
    style N02 fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#166534

    subgraph N03["技能"]
        direction TB
        MSK["MiniMax Skills"]
        PSK["mattpocock Skills"]
    end
    style N03 fill:#f3f4f6,stroke:#6b7280,stroke-width:2px,stroke-dasharray:6 4,color:#374151

    subgraph N04["工具"]
        direction TB
        CDM["chrome-devtools-mcp"]
    end
    style N04 fill:#e4f3ff,stroke:#3399ff,stroke-width:2px,color:#1a5fa8

    subgraph N05["机器人"]
        direction TB
        AB["AstrBot"]
    end
    style N05 fill:#fce7f3,stroke:#ec4899,stroke-width:2px,color:#9d174d

    N00 --> N01
    N01 --> N02
    N02 --> N03
    N02 --> N04
    N00 --> N05
```

| 节点 | 位置 | 工具 |
|------|------|------|
| [大模型](./大模型/) | 底层 AI 能力 | DeepSeek V4 Flash / Pro |
| [路由](./路由/) | API 代理层 | CLIProxyAPI |
| [终端](./终端/) | 交互界面 | DeepSeek TUI · Claude Code |
| [技能](./技能/) | Agent 扩展 | MiniMax Skills · mattpocock Skills |
| [工具](./工具/) | MCP 工具服务 | chrome-devtools-mcp |
| [机器人](./机器人/) | 机器人框架 | AstrBot |

---

**License**: MIT
