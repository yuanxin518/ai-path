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
    style N00 fill:#ffffff,stroke:#cccccc,stroke-width:1px,color:#333333

    subgraph N01["路由"]
        direction TB
        CPA["CLIProxyAPI"]
    end
    style N01 fill:#ffffff,stroke:#cccccc,stroke-width:1px,color:#333333

    subgraph N02["终端"]
        direction TB
        TUI["DeepSeek TUI"]
        CC["Claude Code"]
        RX["Reasonix Code"]
    end
    style TUI fill:#f0f0f0,stroke:#cccccc,stroke-width:1px,stroke-dasharray:4 4,color:#999999
    style RX fill:#fff3cd,stroke:#f59e0b,stroke-width:3px,color:#92400e
    style N02 fill:#ffffff,stroke:#cccccc,stroke-width:1px,color:#333333

    subgraph N03["技能"]
        direction TB
        MSK["MiniMax Skills"]
        PSK["mattpocock Skills"]
    end
    style N03 fill:#ffffff,stroke:#cccccc,stroke-width:1px,color:#333333

    subgraph N04["工具"]
        direction TB
        CDM["chrome-devtools-mcp"]
    end
    style N04 fill:#ffffff,stroke:#cccccc,stroke-width:1px,color:#333333

    subgraph N05["机器人"]
        direction TB
        AB["AstrBot"]
    end
    style N05 fill:#ffffff,stroke:#cccccc,stroke-width:1px,color:#333333

    N00 --> N02
    N00 -.-> N01
    N01 -.-> N02
    N02 --> N03
    N02 --> N04
    N00 --> N05

    subgraph N06["操作系统"]
        direction TB
        WIN["Windows"]
        WSL2_["WSL 2"]
        SUSE["openSUSE Tumbleweed"]
    end
    style N06 fill:#e8f5e9,stroke:#66bb6a,stroke-width:2px,color:#2e7d32

    N06 -.-> N02
    N06 -.-> N07
    N06 -.-> N08
    N06 -.-> N09

    subgraph N07["浏览器"]
        direction TB
        ZB["Zen Browser"]
        subgraph N07_P["插件"]
            direction TB
            FP["FoxyProxy"]
        end
        style N07_P fill:#e3f2fd,stroke:#90caf9,stroke-width:1px,color:#1565c0
    end
    style N07 fill:#e3f2fd,stroke:#42a5f5,stroke-width:2px,color:#1565c0

    subgraph N08["知识库"]
        direction TB
        LOGSEQ["Logseq"]
    end
    style N08 fill:#fce4ec,stroke:#ef5350,stroke-width:2px,color:#c62828

    N00 -.-> N08

    subgraph N09["阅读"]
        direction TB
        FOLO["Folo"]
    end
    style N09 fill:#f3e5f5,stroke:#ab47bc,stroke-width:2px,color:#6a1b9a
```

| 节点 | 位置 | 工具 |
|------|------|------|
| [大模型](./大模型/) | 底层 AI 能力 | **DeepSeek V4 Flash / Pro** — 性价比高，长上下文（1M tokens），Agent 模式支持好 |
| [路由](./路由/) | API 代理层 | **CLIProxyAPI** — 为终端 CLI 提供兼容 API 代理接口，支持多账号轮询负载均衡 |
| [终端](./终端/) | 交互界面 | **AI 终端**<br>~~DeepSeek TUI~~ — 已停用<br>**Claude Code** — Anthropic 官方终端 AI 客户端<br>**⭐ Reasonix Code** — 编码助手，Agent/Subagent/MCP<br><br>**系统终端**<br>**WindTerm** — 持久化终端，SSH/本地会话<br>**Windows PowerShell** — 原生命令行 |
| [技能](./技能/) | Agent 扩展 | **MiniMax Skills** — 工程化技能仓库<br>**mattpocock Skills** — 实用技能集合，含 grill-me 方案测试 |
| [工具](./工具/) | MCP 工具服务 | **chrome-devtools-mcp** — Chrome 官方 MCP 服务，让 AI 控制浏览器 DevTools |
| [机器人](./机器人/) | AI 接入 | **AstrBot** — AI 聊天机器人框架，接入大模型到多聊天平台（QQ/微信/Telegram 等） |
| [操作系统](./操作系统/) | 底层运行环境 | **Windows** — 宿主机<br>**WSL 2** — Linux 内核虚拟化层<br>**openSUSE Tumbleweed** — 滚动发行版 Linux 开发环境 |
| [浏览器](./浏览器/) | 网页浏览与代理 | **Zen Browser** — 基于 Firefox 内核，隐私优先<br>├ **FoxyProxy** — 动态代理规则控制扩展（插件） |
| [知识库](./知识库/) | 个人知识管理 | **Logseq** — 本地优先知识管理，双向链接，通过 GitHub 仓库同步 |
| [阅读](./阅读/) | RSS 新闻阅读 | **Folo** — 现代化 RSS 阅读器，订阅管理与内容聚合 |

---

**License**: MIT
