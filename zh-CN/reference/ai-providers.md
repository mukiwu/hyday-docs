---
locale: zh-CN
category: reference
slug: ai-providers
source: src/content/docs/zh-CN/reference/ai-providers.tsx
---
> * Hyday 支援多种 AI 服务供应商 (Providers)，可根据运算速度、逻辑能力或隐私需求选取最适合的模型。本页涵盖透过 **API Key (或本机端点 URL)** 设置的供应商；Claude Code、Gemini CLI、Codex CLI 等并未涵盖在内 *

## 支援的服务供应商对照表

   供应商 运作模式 工具呼叫 (Tool Calling) 必要条件    OpenAI云端服务支援API Key Anthropic Claude云端服务支援API Key Google Gemini云端服务支援API Key OpenRouter云端聚合视底层模型而定API Key Ollama本机执行视底层模型而定本机 Ollama 服务 Custom (OpenAI 兼容) 云端 / 自架视端点设置而定Base URL + API Key  

## OpenAI 模型清单

Hyday 设置页默认提供下列 OpenAI 模型 (按推荐顺序排列)：

- **GPT-5.5 / GPT-5.5 Pro** (2026-04)：最新旗舰，1M tokens 上下文窗口，agentic coding 与长任务代理能力大幅提升；Pro 版本针对复杂推理进一步加强
- **GPT-5.4**：上一代旗舰，可作为稳定备选
- **GPT-5-mini / GPT-5-nano**：轻量版本，分别针对中等与极低延迟 / 成本的任务
- **GPT-4.1**：tool calling 稳定度极高，需要严格 schema 控制时推荐使用
- **o4-mini**：reasoning 导向的轻量模型，适合需要逐步思考的数学、代码除错任务

## Anthropic Claude 模型清单

Hyday 设置页默认提供下列 Claude 模型 (按推荐顺序排列)：

- **Claude Opus 4.7** (2026-04)：当前最强的旗舰模型，agentic coding 相较 4.6 显著提升，视觉解析度达 3.75 MP，适合最复杂的推理与长文档分析
- **Claude Sonnet 4.6** (2026-02)：性价比最佳的综合型选择，Claude Code 内测中 59% 开发者偏好其胜过上一代 Opus 4.5
- **Claude Opus 4.5 / Sonnet 4.5** (2025-11)：稳定的上一代备选，遇到新版本不稳或费用考量时可回退使用
- **Claude Haiku 4.5** (2025-10)：小型快速模型，低延迟低成本，适合大量短任务与背景处理

## Google Gemini 模型清单

Hyday 设置页默认提供下列 Gemini 模型：

- **Gemini 3.1 Pro (Preview)**：最新的 reasoning-first 旗舰，adaptive thinking、1M tokens 上下文与整合式 grounding
- **Gemini 3.1 Flash Lite (Preview) / Gemini 3 Flash (Preview)**：3.x 系列的速度与成本导向版本，适合大量 chat 与即时互动
- **Gemini 2.5 Pro / 2.5 Flash**：稳定且广泛验证的上一代主力，超大上下文窗口，适合处理大型笔记库
- **Gemma 4 31B IT**：Google 开源权重模型，可在 Hyday API 模式下直接呼叫，也适合透过 Ollama 自架

> **ℹ️ Info**
>  Hyday 会自动将已停用的 `gemini-3-pro-preview` (Google 于 2026-03-09 退役) 重写成 `gemini-3.1-pro-preview`，使用者无需手动迁移。 

## 本机模型推荐 (透过 Ollama)

Hyday 设置页默认提供下列本机模型 (其余可透过 `customModel` 直接呼叫 Ollama 已 pull 的任意模型)：

- **Qwen 3 / Qwen 3-Coder**：阿里巴巴开源系列，中文支援与代码能力俱佳
- **Llama 3.1**：Meta 开源主流选择，生态支援最广
- **DeepSeek V3.1**：逻辑推理与中文语境下表现优异
- **Mistral Small 3.2**：欧洲开源代表，兼顾效率与品质
- **Granite 4**：IBM 开源系列，企业导向、商业授权友善

## 不同应用情境的推荐选择

   应用情境 建议模型 推荐理由    **日常 Chat 对话**Claude Haiku 4.5 / GPT-5-mini / Gemini 2.5 Flash回应速度与成本平衡，适合一般对话与轻量问答。 **Agent 代理模式**GPT-5.5 / Claude Sonnet 4.6Tool Calling 稳定度与长任务 agentic 表现最佳。 **人格蒸馏**Claude Sonnet 4.6 / Gemini 3.1 Pro (建议搭配 CLI 后端)支援六维网络调研与多阶段综合提炼，需要稳定的搜索工具与长上下文推理。 **隐私与离线处理**Ollama Qwen 3 / Llama 3.1 / DeepSeek V3.1资料完全不离开本机，确保最高隐私权。 **程序码协助**Claude Sonnet 4.6 / Claude Opus 4.7 / Qwen 3-CoderSonnet 4.6 性价比最佳；复杂重构或大型改动建议升级 Opus 4.7；离线代码可用 Qwen 3-Coder。 **深度推理**GPT-5.5 Pro / o4-mini / Claude Opus 4.7需要逐步思考的数学、逻辑谜题或除错任务，reasoning / Pro 系列模型表现最佳。  

> **ℹ️ Info**
>  模型市场发展迅速，若发现 Hyday 默认菜单中尚未包含某个新推出的模型，可以使用设置页面中的 `customModel` 栏位，手动输入该模型的 ID 进行呼叫
