---
locale: zh-TW
category: concepts
slug: local-first
source: src/content/docs/zh-TW/concepts/local-first.tsx
---
> *Hyday 的核心原則是**筆記永遠儲存在使用者自己的電腦**，而非官方伺服器。雲端功能僅用於同步少部分的個人設定，絕不儲存使用者的檔案。*

## 哪些資料會儲存在本機？

- **所有的筆記內容**(`.md`)
- **所有的日記內容**(`journal/年份/YYYY-MM-DD.md`)
- **白板與 Hyday Agent 對話歷史**(`.hyday/`)
- **搜尋索引與快取**(`.hyday/`)

這些檔案即是資料夾內可見的所有內容。即使解除安裝 Hyday，這些資料依然會完整保留，並可隨時透過任何 Markdown 編輯器開啟

- **應用程式偏好設定**：過濾器、釘選清單、AI Provider 設定...等，存放於系統的 app 資料夾- macOS`~/Library/Application Support/Hyday/preferences.json`
- Windows`%APPDATA%/Hyday/preferences.json`

## 哪些資料會同步至雲端？(選用功能)

登入帳號後，Hyday 會將**跟軟體有關的設定資訊**同步至雲端資料庫 (Firestore)：

- **首頁卡片寬度與位置**：確保在不同裝置間擁有一致的界面佈局
- **電子報訂閱偏好**：紀錄訂閱選擇
- **編輯器的設定**：拼字檢查與圖片寬度設定
- **VVIP 訂閱狀態**：用於驗證進階功能的使用權限

登入後會自動同步，登出後會自動清空雲端設定。此外也可選擇不登入(完全離線) 使用 Hyday，不影響任何筆記功能

## 關於 AI 功能的資料處理

當使用 AI 相關功能 (包括但不限於 Hyday Agent、Hyday Channel、人格蒸餾或脈絡分析) 時，相關內容將會傳送至所選擇的 AI 服務供應商，處理方式依各供應商的隱私政策而定：

- **雲端供應商**(如 OpenAI、Claude、Gemini、OpenRouter)：依據該公司的資料隱私政策處理
- **本機供應商**(如 Ollama)：資料處理完全在電腦上進行，不會傳送到外部網路
- **CLI 供應商**(Claude Code、Gemini CLI、Codex)：依據該工具的運作機制進行處理

建議在處理極其敏感的內容時，優先考慮使用本機 AI 模型。

> **ℹ️ Info**
> 可以將供應商設定為本機端的 Ollama，並下載合適的模型。如此一來，撰寫筆記、AI 分析與 Agent 操作都能在完全不連網的情況下在本機執行。

## 離線狀態下可以使用嗎？

除了帳號登入驗證與雲端 AI 功能外，**Hyday 的絕大部分功能皆支援離線使用**。撰寫筆記、管理日記、探索標籤、操作白板或使用本機 AI，皆無須連網即可流暢運作

## 延伸閱讀

- [隱私與資料儲存政策](https://hyday.tw/docs/reference/privacy)：深入了解完整的資料流向細節
