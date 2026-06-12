# Contributing to DreamCoder

感谢你对 DreamCoder 的关注！无论是报告 bug、提出功能建议，还是提交代码，都非常欢迎。

## 行为准则

- 尊重每一位贡献者。
- 建设性的讨论，避免人身攻击。
- 如果你发现安全漏洞，请私下联系维护者，不要公开提交 Issue。

## 如何贡献

### 报告 Bug

1. 在 [Issues](https://github.com/GoDiao/dreamcoder/issues) 中搜索，确认是否已有相同问题。
2. 如果没有，新建 Issue，包含以下信息：
   - **环境**：操作系统版本、DreamCoder 版本（设置 → 关于）。
   - **复现步骤**：清晰描述触发 bug 的操作。
   - **期望行为 vs 实际行为**。
   - **截图或日志**（如有）。

### 功能建议

1. 先在 Issues 中搜索，避免重复。
2. 新建 Issue，描述：
   - 你希望解决什么问题。
   - 你期望的功能是什么样的。
   - 为什么这对你有价值。

### 提交代码

1. **Fork 仓库**，从 `dev` 分支创建你的功能分支：
   ```bash
   git checkout dev
   git checkout -b feat/your-feature-name
   ```

2. **开发**。请遵循项目现有的代码风格：
   - TypeScript 严格模式，避免 `any`。
   - React 函数组件 + Hooks。
   - 状态管理使用 Zustand。
   - 样式使用 Tailwind CSS v4。

3. **提交**。使用语义化 commit message：
   ```
   feat: 添加 XXX 功能
   fix: 修复 XXX 问题
   refactor: 重构 XXX
   docs: 更新 XXX 文档
   chore: 杂项变更
   ```

4. **测试**。确保你的改动不会破坏现有功能：
   ```bash
   cd desktop
   bun run lint    # TypeScript 类型检查
   bun run test    # 运行测试
   ```

5. **提交 PR**。PR 目标分支为 `dev`，描述清楚改了什么、为什么改。

## 项目结构

```
dreamcoder/
├── desktop/               # Tauri 桌面应用
│   ├── src/
│   │   ├── components/    # React 组件
│   │   ├── stores/        # Zustand 状态管理
│   │   ├── lib/           # 工具函数 & 运行时
│   │   ├── hooks/         # React Hooks
│   │   ├── pages/         # 页面组件
│   │   └── i18n/          # 国际化
│   └── src-tauri/         # Rust 后端
├── sidecar/               # Bun 后端服务
├── website/               # 项目官网
├── docs/                  # 文档
└── adapters/              # 第三方平台适配器
```

## 开发环境

```bash
# 环境要求
# - Bun >= 1.0
# - Rust (用于编译 Tauri)
# - Node.js >= 18

git clone https://github.com/GoDiao/dreamcoder.git
cd dreamcoder/desktop
bun install
bun run tauri dev
```

## 许可证

贡献即表示你同意将你的代码以 [MIT License](LICENSE) 授权。
