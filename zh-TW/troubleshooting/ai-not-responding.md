---
locale: zh-TW
category: troubleshooting
slug: ai-not-responding
source: src/content/docs/zh-TW/troubleshooting/ai-not-responding.tsx
---
> * 若在使用 AI 功能時遇到系統無反應、持續載入、或跳出錯誤訊息時，請參考以下診斷流程進行排除 *

## 1. 檢查服務供應商的連線狀態

請前往**設定** (`⌘` + `,`) → **AI**分頁，找到正在使用的供應商資訊，點擊**測試連線**按鈕。連線失敗的常見原因包括：

- **API Key 異常**：金鑰已過期、被撤銷或輸入不完整
- **帳戶額度不足**：雲端供應商的額度已耗盡
- **服務端故障**：該供應商的伺服器目前正處於維護或異常狀態

## 2. 雲端供應商：檢查網路環境

部分辦公室網路或防火牆設定可能會阻擋特定的 AI 服務通訊。可以嘗試：

- 切換至其他網路環境 (例如使用手機熱點) 進行交叉測試
- 造訪供應商官方狀態頁面確認服務狀況：[OpenAI Status](https://status.openai.com/)、[Anthropic Status](https://status.anthropic.com/)、[Google Cloud Status](https://status.cloud.google.com/)

## 3. 本機 Ollama：確認服務是否正常運作

請於終端機執行以下指令測試 Ollama 是否正常回應：

```
``
```

若回應 200 代表正常；若回應 `Connection refused`，代表 Ollama 服務尚未啟動，請執行：

```
``
```

同時請確認設定的模型已下載完成：

```
``
```

## 4. 自訂端點：驗證路徑格式

Hyday 會自動處理 `/v1` 路徑後綴，請檢查 Base URL 設定：

- 若填入 `https://api.example.com`：Hyday 會自動對接至 `/v1/chat/completions`
- 若填入 `https://api.example.com/v1`：Hyday 會直接對接至 `/chat/completions`

請注意，自訂服務端必須符合 OpenAI 相容格式，否則可能無法正常運作

## 5. AI Agent 操作卡死處理

若 Agent 在執行任務時陷入死循環或停止回應：

- 點擊對話視窗右上角的**停止**按鈕強行中斷
- 開啟一段全新的對話進行測試
- 若特定指令反覆導致卡死，請檢查所選模型是否完整支援**工具呼叫**功能，詳見 [AI 供應商對照表](/docs/reference/ai-providers)

## 6. 常見錯誤代碼對照表

   錯誤代碼 代表意義 建議處理方式    401API Key 錯誤請重新檢查並貼上正確的金鑰 403權限受限請檢查帳號是否有權限存取該特定模型 429請求頻率超限 請稍候再試，或升級帳號等級 500 / 503供應商端故障此為供應商端問題，請關注官方狀態頁面 Context length exceeded內容超出長度上限請減少一次傳送的筆記量，或更換為具備大上下文視窗的模型  

> **ℹ️ Info**
>  若某一供應商反覆失敗，建議暫時切換至另一個供應商 (如從雲端切換至本機 Ollama)。若切換後功能正常，則代表問題出在供應商端而非 Hyday 本身
