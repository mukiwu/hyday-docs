---
locale: zh-TW
category: reference
slug: ai-providers
source: src/content/docs/zh-TW/reference/ai-providers.tsx
---
> *Hyday 支援多種 AI 服務供應商 (Providers)，可根據運算速度、邏輯能力或隱私需求選取最適合的模型。本頁涵蓋透過**API Key (或本機端點 URL)**設定的供應商；Claude Code、Gemini CLI、Codex CLI 等並未涵蓋在內*

## 支援的服務供應商對照表

供應商運作模式工具呼叫 (Tool Calling)必要條件OpenAI雲端服務支援API KeyAnthropic Claude雲端服務支援API KeyGoogle Gemini雲端服務支援API KeyOpenRouter雲端聚合視底層模型而定API KeyOllama本機執行視底層模型而定本機 Ollama 服務Custom (OpenAI 兼容)雲端 / 自架視端點設定而定Base URL + API Key

## OpenAI 模型清單

Hyday 設定頁預設提供下列 OpenAI 模型 (按推薦順序排列)：

- **GPT-5.5 / GPT-5.5 Pro**(2026-04)：最新旗艦，1M tokens 上下文視窗，agentic coding 與長任務代理能力大幅提升；Pro 版本針對複雜推理進一步加強
- **GPT-5.4**：上一代旗艦，可作為穩定備選
- **GPT-5-mini / GPT-5-nano**：輕量版本，分別針對中等與極低延遲 / 成本的任務
- **GPT-4.1**：tool calling 穩定度極高，需要嚴格 schema 控制時推薦使用
- **o4-mini**：reasoning 導向的輕量模型，適合需要逐步思考的數學、代碼除錯任務

## Anthropic Claude 模型清單

Hyday 設定頁預設提供下列 Claude 模型 (按推薦順序排列)：

- **Claude Opus 4.7**(2026-04)：當前最強的旗艦模型，agentic coding 相較 4.6 顯著提升，視覺解析度達 3.75 MP，適合最複雜的推理與長文檔分析
- **Claude Sonnet 4.6**(2026-02)：性價比最佳的綜合型選擇，Claude Code 內測中 59% 開發者偏好其勝過上一代 Opus 4.5
- **Claude Opus 4.5 / Sonnet 4.5**(2025-11)：穩定的上一代備選，遇到新版本不穩或費用考量時可回退使用
- **Claude Haiku 4.5**(2025-10)：小型快速模型，低延遲低成本，適合大量短任務與背景處理

## Google Gemini 模型清單

Hyday 設定頁預設提供下列 Gemini 模型：

- **Gemini 3.1 Pro (Preview)**：最新的 reasoning-first 旗艦，adaptive thinking、1M tokens 上下文與整合式 grounding
- **Gemini 3.1 Flash Lite (Preview) / Gemini 3 Flash (Preview)**：3.x 系列的速度與成本導向版本，適合大量 chat 與即時互動
- **Gemini 2.5 Pro / 2.5 Flash**：穩定且廣泛驗證的上一代主力，超大上下文視窗，適合處理大型筆記庫
- **Gemma 4 31B IT**：Google 開源權重模型，可在 Hyday API 模式下直接呼叫，也適合透過 Ollama 自架

> **ℹ️ Info**
> Hyday 會自動將已停用的`gemini-3-pro-preview`(Google 於 2026-03-09 退役) 重寫成`gemini-3.1-pro-preview`，使用者無需手動遷移。

## 本機模型推薦 (透過 Ollama)

Hyday 設定頁預設提供下列本機模型 (其餘可透過`customModel`直接呼叫 Ollama 已 pull 的任意模型)：

- **Qwen 3 / Qwen 3-Coder**：阿里巴巴開源系列，中文支援與代碼能力俱佳
- **Llama 3.1**：Meta 開源主流選擇，生態支援最廣
- **DeepSeek V3.1**：邏輯推理與中文語境下表現優異
- **Mistral Small 3.2**：歐洲開源代表，兼顧效率與品質
- **Granite 4**：IBM 開源系列，企業導向、商業授權友善

## 不同應用情境的推薦選擇

應用情境建議模型推薦理由**日常 Chat 對話**Claude Haiku 4.5 / GPT-5-mini / Gemini 2.5 Flash回應速度與成本平衡，適合一般對話與輕量問答。**Agent 代理模式**GPT-5.5 / Claude Sonnet 4.6Tool Calling 穩定度與長任務 agentic 表現最佳。**人格蒸餾**Claude Sonnet 4.6 / Gemini 3.1 Pro (建議搭配 CLI 後端)支援六維網路調研與多階段綜合提煉，需要穩定的搜尋工具與長上下文推理。**隱私與離線處理**Ollama Qwen 3 / Llama 3.1 / DeepSeek V3.1資料完全不離開本機，確保最高隱私權。**程式碼協助**Claude Sonnet 4.6 / Claude Opus 4.7 / Qwen 3-CoderSonnet 4.6 性價比最佳；複雜重構或大型改動建議升級 Opus 4.7；離線代碼可用 Qwen 3-Coder。**深度推理**GPT-5.5 Pro / o4-mini / Claude Opus 4.7需要逐步思考的數學、邏輯謎題或除錯任務，reasoning / Pro 系列模型表現最佳。

> **ℹ️ Info**
> 模型市場發展迅速，若發現 Hyday 預設選單中尚未包含某個新推出的模型，可以使用設定頁面中的`customModel`欄位，手動輸入該模型的 ID 進行呼叫
