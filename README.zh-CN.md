# Macify Design

Macify Design 是一个面向 AI coding/design agents 的 skill 和通用指令集，用来把工具类 Web 产品设计成 Mac-like 的工作台界面：窗口化结构、皮肤质感、材质分层、日间/夜间模式、移动端 app shell，以及真实产品状态。

它不是 macOS 克隆工具，不模拟操作系统，也不使用 Apple 资产。

## 适合使用

- 工具类 Web 产品
- 管理后台和内部系统
- Dashboard 和数据分析台
- 编辑器和创作工具
- AI 工具、Agent 工作台
- CMS、CRM、教程管理、发布系统
- 开发者工具、监控平台、自动化编排工具
- 单文件 HTML 工具原型

不默认用于营销页、品牌官网、博客、纯阅读文档站、文章/视频浏览站、电商首页、作品集、游戏，或已经有更强设计系统要求的项目。

## 判断方式

不要按行业词判断，要按工作流判断。

触发：创建、编辑、管理、发布、配置、分析、监控、审核、自动化、批处理、调试、生成、预览、控制对象。

不默认触发：阅读、浏览、展示、介绍、营销、消费内容。

例如：

- “做一个教程系统 HTML，用来管理发布教程”：触发。
- “做一个教程阅读网站”：不默认触发。

## 仓库结构

```text
macify-design/
├── skills/
│   └── macify-design/          # Codex/OpenAI skill
├── adapters/                   # 给其他 AI 工具使用的指令
├── examples/                   # 触发和反触发案例
├── README.md
├── README.zh-CN.md
├── LICENSE
└── VERSION
```

## Codex 安装

把 skill 文件夹复制到 Codex skills 目录：

```bash
mkdir -p ~/.codex/skills
cp -R skills/macify-design ~/.codex/skills/macify-design
```

之后可以用 `$macify-design` 显式触发，也可以让它在合适的工具类 Web 产品需求中自动触发。

## 其他 AI 产品使用

使用 `adapters/` 里的文件：

- `generic-system-prompt.md`：ChatGPT Projects、Gemini、通用 AI 助手
- `editor-agent-instructions.md`：Cursor、Windsurf、Cline、Roo、Continue、编辑器 agent
- `claude-instructions.md`：Claude Projects、Claude Code
- `github-copilot-instructions.md`：VS Code / GitHub Copilot workspace instructions
- `app-builder-prompt.md`：v0、Lovable、Bolt、Replit Agent 等 prompt-to-app 工具

这些 adapter 是可复制的指令，不是自动安装器。核心规则以 `skills/macify-design/SKILL.md` 和 references 为准。

## 核心原则

先把工具产品收敛成可用的工作台，再应用 Mac-like 的皮肤和布局。桌面端是窗口化 workbench，移动端是响应式 app shell。必须支持日间/夜间模式、真实状态和可用交互。

## License

MIT.
