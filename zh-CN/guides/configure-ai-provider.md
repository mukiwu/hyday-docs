---
locale: zh-CN
category: guides
slug: configure-ai-provider
source: src/content/docs/zh-CN/guides/configure-ai-provider.tsx
---
> * Hyday 支援三种接入 AI 的方式：**云端 API 服务**、**CLI 订阅** (Claude Code / Gemini CLI / Codex CLI)、以及**本机模型** (Ollama)。所有设置都在**设置 → AI** 页面中管理 *

## 三种接入方式的差异

   类型 需要什么 计费方式 支援工具呼叫     云端 API 服务 各家供应商的 API Key 依 API 用量计价 取决于模型   CLI 订阅 本机已安装并登录Claude Code / Gemini CLI / Codex CLI 沿用既有订阅方案，**不另外计费** 沿用 CLI 内建工具(含网络搜索)   本机模型 本机已安装并启动 Ollama 完全免费 / 离线 视模型而定，多数较弱   

## 支援的 AI 供应商

### 云端 API 服务

- **OpenAI**：GPT-4o 系列、GPT-5 系列等
- **Anthropic Claude**：Claude Opus / Sonnet / Haiku 系列
- **Google Gemini**：Gemini Pro / Flash 系列
- **OpenRouter**：聚合多家模型的单一入口
- **Custom (OpenAI 兼容)**：适用于 Groq、Together AI、Fireworks 等自架或第三方相容端点

### CLI 订阅 (推荐给已有订阅的使用者)

若已有以下任一服务的订阅，可直接让 Hyday 透过 CLI 接到既有订阅，**不会再消耗 API 额度**：

- **Claude Code**
- **Gemini CLI**
- **Codex CLI**

CLI 后端本身内建网络搜索与文件操作工具，因此**人格蒸馏、脉络分析等需要即时调研的功能在 CLI 后端上可直接使用**，云端 API 后端则需要模型本身支援这些工具

### 本机模型

- **Ollama**：本机执行的开源模型，所有运算在装置内完成，离线可用

## 1. 设置云端 API 供应商

按下 `⌘` + `,` 打开设置页面，切换至 AI 分页，依序选择供应商和模型，再输入 API 金钥即可完成设置，点击「测试连线」可即时验证 API Key 连线是否正常

常见错误：`401` = Key 错误、`429` = 超过频率限制

![设置 → AI 分页，展示 Provider 列表与 API Key 输入](https://hyday.tw/docs/screenshots/guides-configure-ai-provider-1.png)

> **ℹ️ Info**
>  **Base URL**：填入服务端 Endpoint (Hyday 会自动处理结尾 `/v1`) **Model**：填入该服务商提供的精确模型 ID，例如：`llama3.1:8b`、`gemini-flash-lite-latest` 等 

## 2. 设置并选择 CLI 订阅

> **⚠️ Warning**
>  请确认本机已安装对应的 CLI 并完成登录，Hyday 会自动侦测登录情况，已就绪的 CLI 会在设置页中显示为「已验证」 

- **Claude Code**：依照 [Anthropic 官方文件](https://docs.anthropic.com/en/docs/claude-code) 安装 `Claude Code` 并完成登录
- **Gemini CLI**：依照 [Google 官方文件](https://geminicli.com/) 安装 `Gemini CLI` 并完成登录
- **Codex CLI**：依照 [OpenAI 官方文件](https://platform.openai.com/docs/plugins/introduction) 安装 `Codex CLI` 并完成登录

![设置 → AI 分页，展示 CLI 订阅设置](https://hyday.tw/docs/screenshots/guides-configure-ai-provider-2.png)

## 3. 设置本机 Ollama

先确保电脑已执行 Ollama：

```
``
```

回到 Hyday 设置页，启用 **Ollama**。默认连线位址为 `http://localhost:11434`

## 4. 给每个功能指定不同的模型

如果你手上有多个订阅服务或 API 供应商，可以给每个功能指定不同的模型

![设置 → AI 分页，展示 Functions 分流设置](https://hyday.tw/docs/screenshots/guides-configure-ai-provider-3.png)

> **⚠️ Warning**
>  云端 API 与 CLI 订阅都会把传送的笔记片段送到对应服务的伺服器，受该供应商隐私政策规范。若笔记内容涉及高度敏感资料，请改用本机 Ollama 

> **ℹ️ Info**
>  如果已经有 Claude / ChatGPT / Gemini 订阅，**CLI 订阅是最划算的选择**，不会额外计费还能用到较好的模型；若没有订阅、想随用随付，云端 API 较简单；对隐私要求极高就选 Ollama 

## 延伸阅读

- [AI Provider 详细对照表](https://hyday.tw/docs/reference/ai-providers)：完整模型清单与 Tool Calling 支援度
- [Hyday Agent](https://hyday.tw/docs/guides/use-ai-agent)：Agent 模式的完整功能说明
- [Hyday Channel](https://hyday.tw/docs/guides/hyday-channel)：把 Claude Code 接成你的即时协作伙伴
