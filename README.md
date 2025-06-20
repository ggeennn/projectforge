# 🧠 ProjectForge - 全栈作品集控制系统

ProjectForge 是我基于 GPT + Cursor AI 自主设计的“全栈学习与项目管理系统”。它不仅是我所有作品集项目的孵化器，也是一个自我驱动、自我规划、自我成长的系统化开发工具。

## 🎯 项目目标

- 管理并驱动我的多个全栈开发项目
- 利用 Prompt 工程生成项目模版与任务清单
- 作为 AI 驱动学习的元项目加入我的作品集展示
- 将计划、过程、成果统一版本管理与公开展示

## 🗂️ 项目结构

```
projectforge/
├── README.md ← 本文件
├── prompts/ ← 各项目的 prompt 模版（Markdown）
│ ├── notehub.md
│ └── bankdb-sim.md
├── plans/ ← 阶段性技能规划、路线图
│ └── roadmap.md
├── context/ ← 项目运行上下文，AI 角色配置，个人背景
│ ├── meta-context.md ← 自我背景与目标
│ ├── project-glossary.md ← 关键词解释与术语定义
│ ├── prompt-style.md ← 对话风格 + AI 期待行为
│ └── context-template.md ← 可复制用的上下文封装模版（已集成 MCP 调用）
├── portfolio.json ← 项目清单与属性（结构化管理）
└── .gitignore
```

## 👤 作者简介（Meta Context）

我是一名中途转行者，曾在多个行业积累经验，目前就读于 Seneca College 的 Computer Programming & Analysis 项目，专注构建 AI 驱动的全栈作品集。

拥有家庭责任、跨行业背景与系统化思维能力，我善于通过动手项目和直觉式学习方法快速掌握新技术。我的项目不仅服务于个人成长，同时也面向现实世界的问题解决。

👉 查看我的完整个人背景与技能定位：[`personal-profile.md`](./personal-profile.md)

## 🔧 技术与工具

- Git + GitHub
- ChatGPT / GPT-4 Prompt 工程
- Cursor IDE 辅助
- Markdown 文档管理
- Vercel (未来考虑部署 Portfolio 展示用版本)

## 🚀 已集成项目

| 项目 | 描述 | 技术栈 |
|------|------|--------|
| NoteHub | 全栈笔记应用 | React, Node.js, PostgreSQL |
| BankDB Sim | 银行业数据建模与恢复演示 | SQL, Bash |
| ResumeAI | 简历智能生成器 | HTML, JavaScript |
| PortfolioPage | 个人网站部署展示 | HTML/CSS/JS, Vercel |
| ProjectForge | 项目规划与 Prompt 管理系统 | Markdown, Prompt, Cursor IDE |

## 🧪 未来方向

- 项目模版自动化生成脚本（Python）
- JSON / Markdown 到 Web 展示系统
- GPT Prompt 存档版本控制（PromptForge 子模块）

---

## 🧰 ProjectForge 使用指南（跨平台 AI 移植）

ProjectForge 除了作为项目管理工具，也是一个“AI Prompt 移植包”，帮助我在任何 Chat / IDE 中复用背景上下文与对话风格。

### 📂 核心文件说明

| 文件 | 用途 |
|------|------|
| `meta-context.md` | 我的背景、学习风格、目标方向等 |
| `project-glossary.md` | 项目与术语关键词解释 |
| `prompt-style.md` | 对话结构、教学风格、AI 角色指引 |
| `context-template.md` | 可复制粘贴的 prompt 入口模板，适配 GPT、Gemini、Cursor 等平台 |（已集成 MCP 调用）

### 🧠 推荐用法

1. 💬 开始新对话时，复制 `context-template.md` 内容作为启动语（已集成 MCP 调用）
2. 📎 提示 AI：“请读取本项目 README 和 meta-context.md 了解背景”
3. 🔄 需要术语解释时，引导 AI 查看 `project-glossary.md`
4. 🎓 生成风格偏差时，引导 AI 参照 `prompt-style.md`

🧙‍♂️ 这就是我的“AI 工作流加载器”！
---
---

## 📦 如何使用此项目与 AI 聊天助手协同开发

本项目支持基于 [MCP 协议（Model Context Protocol）](https://modelcontext.org/) 的上下文统一调用。

### 📌 移植步骤（适用于 GPT / Gemini / Cursor 等）

1. 将本项目文件夹或 `.zip` 上传至你的 AI 工具（如 Gemini 文件上传区）
2. 粘贴以下提示词启动会话：

   ```
   你是我的 AI 项目导师，请读取 mcp-config.json 中列出的所有文档，并据此理解我的背景、学习目标、项目结构与可用 prompts，接下来请帮助我完成当前任务。
   ```

3. AI 将自动加载以下核心资源：
   - `plans/roadmap.md`：技能路径规划
   - `plans/status.md`：项目当前进度
   - `context/prompt-style.md`：提示词风格规范
   - `context/meta-context.md`：学习者背景描述
   - `prompts/*.md`：每个项目的详细任务描述
   - `prompthub/prompts.json`：标准化任务 prompt 模板（支持自动建议）

---

## 📂 关于项目 prompts/*.md 的使用建议

每个子项目（如 NoteHub、BankDB Sim）在 `prompts/` 目录中有独立的 `.md` 文件，用于描述其项目背景、目标与任务流程。

这些 `.md` 文件 **未包含在 mcp-config.json 中**，以避免信息过载。

### ✅ 使用方式建议：

- 在启动某个项目任务时，**明确让 AI 读取对应的 `.md` 文件**
- 示例提示词：
  ```
  当前我正处理 NoteHub 项目，请加载 prompts/notehub.md 并结合上下文帮助我完成登录功能设计。
  ```

此策略支持更清晰的分项目任务流程，避免 AI 在多项目之间混淆。
---

## 📈 新增实战项目优先顺序

在 2025 年 6 月，新增以下两个高优先实战训练项目：

- **AI Video Factory**：AI 视频自动化生产流程（参考 https://youtu.be/XB3jCQYcj_0?si=NfSzqtJVhZv10B-0）
- **Web RAG Workflow**：网页抓取与 RAG 工作流搭建（参考 https://youtu.be/Y6C7kpNSrd4?si=rayxcu1TP-waTvZ_）

这些项目已更新进 `portfolio.json`、`status.md` 及 `roadmap.md`，并可在 `prompts/` 下找到对应的任务说明。
