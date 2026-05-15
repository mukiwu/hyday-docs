---
locale: zh-CN
category: concepts
slug: ai-agent
source: src/content/docs/zh-CN/concepts/ai-agent.tsx
---
> * AI Agent 是 Hyday 内建的高级助手。除了具备一般对话能力外，更强大的地方在于能主动执行**工具**：包括读取笔记、建立新文件、进行脉络分析与整理待办任务。 *

## 对话模式 (Chat) vs. 代理模式 (Agent)

- **对话模式 (Chat)**：纯粹的文字交流。AI 根据问题进行回复，但不会存取或修改文件夹中的任何文件
- **代理模式 (Agent)**：具备**行动力**。AI 可以根据需求呼叫各类工具，执行读取笔记、撰写内容、查询标签或深度分析等操作

## AI Agent 的工具箱 (Capabilities)

- **读取内容**：深入阅读指定的笔记篇章或特定日期的日记内容
- **内容创作**：自动建立新笔记，或将重点摘要附加至当前日记中
- **结构化检索**：查找符合特定标签、时间范围或有人事物标记的笔记
- **脉络深度分析**：调用 Lineage 演算法，分析特定主题的发展趋势
- **任务扫描汇整**：从杂乱的笔记中提取待办事项
- **互动组件渲染 (Widgets)**：生成视觉化图表、选项对比表或其他互动式小组件

## 对话纪录与可追溯性

所有 Agent 对话会集中储存在笔记文件夹的 `.hyday/agent-conversations/v1.json` 单一 JSON 档中，可随时回顾对话脉络，或将其纳入版本控制管理

## 支援的服务供应商

由于 Agent 模式需要模型原生支援**工具呼叫**功能，建议使用以下供应商：

- **OpenAI**：推荐 GPT-4o 或更新版本
- **Anthropic Claude**：推荐 Claude Sonnet 或 Opus
- **Google Gemini**：推荐 Gemini 2.5 或 3.0 等系列
- **OpenRouter**：需视选取的底层模型而定
- **本机 Ollama**：需选取支援 Function Calling 的模型，且处理效能视硬件而异

## 延伸阅读

- [设置 AI Provider](https://hyday.tw/docs/guides/configure-ai-provider)：了解更详细的 AI 与 Hyday 对应关系
- [AI Agent 实战指南](https://hyday.tw/docs/guides/use-ai-agent)：掌握高效率的对话技巧。
- [Agent 工具完整清单](https://hyday.tw/docs/reference/agent-tools)：深入了解各项工具的功能与限制。
