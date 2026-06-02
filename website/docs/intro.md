---
sidebar_position: 1
---

# 快速开始

DreamCoder 是 **Claude Desktop 的开源桌面版工作台**，面向国内开发者设计，让你可以用自然语言完成编程任务，无需科学上网。

## 环境要求

| 工具 | 版本要求 | 备注 |
|------|---------|------|
| [Bun](https://bun.sh/) | >= 1.0 | 本地运行时 |
| [Rust](https://www.rust-lang.org/tools/install) | 最新稳定版 | 桌面端编译 |
| Node.js | >= 18 | 部分依赖需要 |

## 安装步骤

```bash
# 1. 克隆仓库
git clone https://github.com/GoDiao/dreamcoder.git
cd dreamcoder

# 2. 安装依赖
bun install

# 3. 启动桌面端开发模式
cd desktop && bun run dev
```

首次启动时，应用会引导你配置 AI Provider。

## 配置 AI 模型

1. 打开 DreamCoder，进入 **设置 → Provider (模型供应商)**
2. 添加你的 API Key（支持 Anthropic、OpenAI、DeepSeek、通义千问、Kimi、Claude 等）
3. 选择默认模型，即可开始编程

## 核心功能

### 🖥️ 原生桌面体验
- 多标签页会话管理，每个会话绑定独立项目目录
- 内置 PTY 终端（PowerShell / bash / zsh）
- 窗口位置和大小自动记忆

### 🤖 Computer Use 模式
- 支持截图视觉模式
- 全新 UIA Tree 文本模式，成本更低、速度更快

### 🔌 全模型支持
- 一键切换 8+ 模型供应商
- 首创延迟可视化测试

### 🛡️ 安全审批流
- 危险操作（文件删除、终端命令）逐条确认
- API Key 本地加密存储
- 多级权限模式：自动批准 / 逐条确认 / 计划模式