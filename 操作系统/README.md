# 操作系统

底层运行环境。

| 层级 | 工具 | 说明 |
|------|------|------|
| 宿主机 | **Windows** | 基础操作系统，运行 GUI 应用和浏览器 |
| 虚拟化层 | **WSL 2** | Windows Subsystem for Linux 2 — 完整 Linux 内核，性能接近原生 |
| Linux 环境 | **openSUSE Tumbleweed** | 滚动发行版 Linux，始终保持最新软件包，适合开发环境 |

## 架构

```
Windows (宿主机)
  └─ WSL 2 (虚拟化层)
       └─ openSUSE Tumbleweed (开发环境)
```

## 为什么选这套组合

- **WSL 2** 提供完整的 Linux 内核，无需双系统或虚拟机即可在 Windows 上运行 Linux
- **openSUSE Tumbleweed** 滚动更新，工具链始终保持最新版本
- Windows 作为宿主机，保留 GUI 应用（浏览器、编辑器等）的原生体验
