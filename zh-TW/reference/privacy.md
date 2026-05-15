---
locale: zh-TW
category: reference
slug: privacy
source: src/content/docs/zh-TW/reference/privacy.tsx
---
<!-- UNCONVERTIBLE: Lock --> 絕不上傳 

 <!-- UNCONVERTIBLE: Cloud -->  

> * Hyday 100% 承諾使用者所有的筆記專屬於使用者自己，筆記內容只會儲存在使用者自己的設備中，不會上傳到 Hyday 的伺服器。雲端同步僅限於少量的系統偏好與授權設定，下表詳細說明系統中各類資料的流向 *

## 資料分類與流向對照表

   資料類別 儲存位置 是否同步至雲端？    筆記原文內容指定的本機資料夾 (`.md`)<!-- UNCONVERTIBLE: LocalOnly --> 日記紀錄與生活點滴指定的本機資料夾 (`.md`)<!-- UNCONVERTIBLE: LocalOnly --> 視覺化白板數據本機資料夾 `.hyday/whiteboards-v2.json`<!-- UNCONVERTIBLE: LocalOnly --> AI 代理對話歷程本機資料夾 `.hyday/agent-conversations/v1.json`<!-- UNCONVERTIBLE: LocalOnly --> 標籤、人事物統計與索引本機隱藏資料夾的快取目錄<!-- UNCONVERTIBLE: LocalOnly --> 全域過濾器與釘選清單本機 `preferences.json`<!-- UNCONVERTIBLE: LocalOnly --> 帳號登入資訊加密安全傳輸<!-- UNCONVERTIBLE: CloudSynced --> VVIP 訂閱與支付狀態加密資料庫<!-- UNCONVERTIBLE: CloudSynced --> 已授權的裝置清單加密資料庫<!-- UNCONVERTIBLE: CloudSynced --> 首頁卡片配置加密資料庫<!-- UNCONVERTIBLE: CloudSynced --> 電子報訂閱偏好加密資料庫<!-- UNCONVERTIBLE: CloudSynced -->  

## 關於 AI 功能的隱私處理

啟動 AI 相關功能 (如對話、Agent 代理、人格蒸餾或脈絡分析) 時，相關的筆記片段會傳送至選取的服務供應商：

- **雲端供應商** (OpenAI / Claude / Gemini / OpenRouter 等)：資料處理受各公司的隱私政策規範。大多數供應商提供**不將 API 資料用於模型訓練**的選項，請參閱官方文件
- **本機供應商** (Ollama)：所有的運算皆在電腦內部執行，資料絕不離開區域網路，且離線可用

> **⚠️ Warning**
>  Hyday 無法控制選用的**雲端供應商**如何存取伺服器上的資料。針對涉及高度敏感內容 (如商業機密、個人健康隱私或身分資訊)，強烈建議選用本機執行的 Ollama 作為 AI 引擎 

## 遙測與使用統計

Hyday 致力於無追蹤體驗，**不收集**任何關於使用者行為的遙測數據 (例如：點擊了哪個按鈕、開啟了哪些筆記等)，僅在登入帳戶時，系統會傳送以下必要資訊以確保功能運作：

- **應用程式版本號**：用於自動檢查與提示更新
- **裝置硬體資訊**：包括作業系統與晶片類型，用於授權驗證與相容性最佳化

## 帳號登出時的處理機制

當執行登出時：

- **本機的所有內容與設定皆會完整保留**
- 儲存於雲端 Firestore 的**首頁配置**與**電子報訂閱設定**會同步移除
- VVIP 授權記錄依然安全儲存於帳戶中，下次重新登入後即可恢復

## 解除安裝應用程式後的狀態

- **筆記資料夾將完整保留**，可以隨時使用任何第三方 Markdown 編輯器繼續讀取內容
- 本機的 `preferences.json` 設定檔通常會保留在系統路徑中，重新安裝時可選擇繼承 (需手動)
- 雲端紀錄將繼續保存，直至主動要求刪除帳號為止

## 聯繫隱私團隊

若對資料安全有任何疑問或疑慮，歡迎致信至 `mukispace@gmail.com`。會在 7 個工作日內提供詳細回覆
