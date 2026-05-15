---
locale: zh-TW
category: concepts
slug: ai-agent
source: src/content/docs/zh-TW/concepts/ai-agent.tsx
---
> *AI Agent 是 Hyday 內建的高級助手。除了具備一般對話能力外，更強大的地方在於能主動執行**工具**：包括讀取筆記、建立新檔案、進行脈絡分析與整理待辦任務。*

## 對話模式 (Chat) vs. 代理模式 (Agent)

- **對話模式 (Chat)**：純粹的文字交流。AI 根據問題進行回覆，但不會存取或修改資料夾中的任何檔案
- **代理模式 (Agent)**：具備**行動力**。AI 可以根據需求呼叫各類工具，執行讀取筆記、撰寫內容、查詢標籤或深度分析等操作

## AI Agent 的工具箱 (Capabilities)

- **讀取內容**：深入閱讀指定的筆記篇章或特定日期的日記內容
- **內容創作**：自動建立新筆記，或將重點摘要附加至當前日記中
- **結構化檢索**：查找符合特定標籤、時間範圍或有人事物標記的筆記
- **脈絡深度分析**：調用 Lineage 演算法，分析特定主題的發展趨勢
- **任務掃描彙整**：從雜亂的筆記中提取待辦事項
- **互動組件渲染 (Widgets)**：生成視覺化圖表、選項對比表或其他互動式小元件

## 對話紀錄與可追溯性

所有 Agent 對話會集中儲存在筆記資料夾的`.hyday/agent-conversations/v1.json`單一 JSON 檔中，可隨時回顧對話脈絡，或將其納入版本控制管理

## 支援的服務供應商

由於 Agent 模式需要模型原生支援**工具呼叫**功能，建議使用以下供應商：

- **OpenAI**：推薦 GPT-4o 或更新版本
- **Anthropic Claude**：推薦 Claude Sonnet 或 Opus
- **Google Gemini**：推薦 Gemini 2.5 或 3.0 等系列
- **OpenRouter**：需視選取的底層模型而定
- **本機 Ollama**：需選取支援 Function Calling 的模型，且處理效能視硬體而異

## 延伸閱讀

- [設定 AI Provider](https://hyday.tw/docs/guides/configure-ai-provider)：了解更詳細的 AI 與 Hyday 對應關係
- [AI Agent 實戰指南](https://hyday.tw/docs/guides/use-ai-agent)：掌握高效率的對話技巧。
- [Agent 工具完整清單](https://hyday.tw/docs/reference/agent-tools)：深入了解各項工具的功能與限制。
