# PromptHub

本模块提供一个简化的 prompts 配置与访问方式，可用于搭配 MCP 协议在 AI 客户端中自动加载。

## 文件说明

- `prompts.json`：标准化 prompt 配置集合，供 AI 调用
- `server.js`：可选 MCP 服务端（暂未实现）

## 使用方式

在 AI 聊天中提示：

```
请读取 promhthub/prompts.json 中 NoteHub 的登录功能模板，协助我生成 React 登录组件并连接后端。
```

⚠️ 本模块依赖 `context/` 文件夹中的全局配置（如 meta-context 与 prompt-style），建议在加载 prompts.json 时一并加载。
