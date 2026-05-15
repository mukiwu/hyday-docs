---
locale: zh-TW
category: guides
slug: configure-ai-provider
source: src/content/docs/zh-TW/guides/configure-ai-provider.tsx
---
> * Hyday 支援三種接入 AI 的方式：**雲端 API 服務**、**CLI 訂閱** (Claude Code / Gemini CLI / Codex CLI)、以及**本機模型** (Ollama)。所有設定都在**設定 → AI** 頁面中管理 *

## 三種接入方式的差異

   類型 需要什麼 計費方式 支援工具呼叫     雲端 API 服務 各家供應商的 API Key 依 API 用量計價 取決於模型   CLI 訂閱 本機已安裝並登入Claude Code / Gemini CLI / Codex CLI 沿用既有訂閱方案，**不另外計費** 沿用 CLI 內建工具(含網路搜尋)   本機模型 本機已安裝並啟動 Ollama 完全免費 / 離線 視模型而定，多數較弱   

## 支援的 AI 供應商

### 雲端 API 服務

- **OpenAI**：GPT-4o 系列、GPT-5 系列等
- **Anthropic Claude**：Claude Opus / Sonnet / Haiku 系列
- **Google Gemini**：Gemini Pro / Flash 系列
- **OpenRouter**：聚合多家模型的單一入口
- **Custom (OpenAI 兼容)**：適用於 Groq、Together AI、Fireworks 等自架或第三方相容端點

### CLI 訂閱 (推薦給已有訂閱的使用者)

若已有以下任一服務的訂閱，可直接讓 Hyday 透過 CLI 接到既有訂閱，**不會再消耗 API 額度**：

- **Claude Code**
- **Gemini CLI**
- **Codex CLI**

CLI 後端本身內建網路搜尋與檔案操作工具，因此**人格蒸餾、脈絡分析等需要即時調研的功能在 CLI 後端上可直接使用**，雲端 API 後端則需要模型本身支援這些工具

### 本機模型

- **Ollama**：本機執行的開源模型，所有運算在裝置內完成，離線可用

## 1. 設定雲端 API 供應商

按下 `⌘` + `,` 開啟設定頁面，切換至 AI 分頁，依序選擇供應商和模型，再輸入 API 金鑰即可完成設定，點擊「測試連線」可即時驗證 API Key 連線是否正常

常見錯誤：`401` = Key 錯誤、`429` = 超過頻率限制

![設定 → AI 分頁，展示 Provider 列表與 API Key 輸入](https://hyday.tw/docs/screenshots/guides-configure-ai-provider-1.png)

> **ℹ️ Info**
>  **Base URL**：填入服務端 Endpoint (Hyday 會自動處理結尾 `/v1`) **Model**：填入該服務商提供的精確模型 ID，例如：`llama3.1:8b`、`gemini-flash-lite-latest` 等 

## 2. 設定並選擇 CLI 訂閱

> **⚠️ Warning**
>  請確認本機已安裝對應的 CLI 並完成登入，Hyday 會自動偵測登入情況，已就緒的 CLI 會在設定頁中顯示為「已驗證」 

- **Claude Code**：依照 [Anthropic 官方文件](https://docs.anthropic.com/en/docs/claude-code) 安裝 `Claude Code` 並完成登入
- **Gemini CLI**：依照 [Google 官方文件](https://geminicli.com/) 安裝 `Gemini CLI` 並完成登入
- **Codex CLI**：依照 [OpenAI 官方文件](https://platform.openai.com/docs/plugins/introduction) 安裝 `Codex CLI` 並完成登入

![設定 → AI 分頁，展示 CLI 訂閱設定](https://hyday.tw/docs/screenshots/guides-configure-ai-provider-2.png)

## 3. 設定本機 Ollama

先確保電腦已執行 Ollama：

```
``
```

回到 Hyday 設定頁，啟用 **Ollama**。預設連線位址為 `http://localhost:11434`

## 4. 給每個功能指定不同的模型

如果你手上有多個訂閱服務或 API 供應商，可以給每個功能指定不同的模型

![設定 → AI 分頁，展示 Functions 分流設定](https://hyday.tw/docs/screenshots/guides-configure-ai-provider-3.png)

> **⚠️ Warning**
>  雲端 API 與 CLI 訂閱都會把傳送的筆記片段送到對應服務的伺服器，受該供應商隱私政策規範。若筆記內容涉及高度敏感資料，請改用本機 Ollama 

> **ℹ️ Info**
>  如果已經有 Claude / ChatGPT / Gemini 訂閱，**CLI 訂閱是最划算的選擇**，不會額外計費還能用到較好的模型；若沒有訂閱、想隨用隨付，雲端 API 較簡單；對隱私要求極高就選 Ollama 

## 延伸閱讀

- [AI Provider 詳細對照表](https://hyday.tw/docs/reference/ai-providers)：完整模型清單與 Tool Calling 支援度
- [Hyday Agent](https://hyday.tw/docs/guides/use-ai-agent)：Agent 模式的完整功能說明
- [Hyday Channel](https://hyday.tw/docs/guides/hyday-channel)：把 Claude Code 接成你的即時協作夥伴
