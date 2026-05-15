---
locale: zh-TW
category: concepts
slug: plugins
source: src/content/docs/zh-TW/concepts/plugins.tsx
---
> *Plugins 可以擴充 Hyday 筆記軟體，通常會將常用的工具元件、第三方服務整合或自訂腳本掛載至 Hyday 中，與筆記資料夾協同運作*

## 何謂 Hyday Plugins？

- **獨立運作**：Plugins 可常駐於 Hyday 主介面或側邊欄
- **受控存取**：透過 Host API 進行筆記讀寫、標籤查詢或脈絡分析
- **安全執行**：於沙箱 (Sandbox) 環境中運作，無法直接存取系統底層檔案
- **權限透明**：每個 Plugin 安裝時皆須明確聲明其所需的存取權限

## Hyday 官方 Plugins

- **便箋**：將便條常駐在右上角，可以寫想法、臨時紀錄、待辦.. 等等的隨手記資訊，自動儲存，有需要也可以直接新增到筆記或日記裡
- **隨機筆記**：隨機顯示任意一篇筆記，適合用來找尋靈感或是複習舊筆記
- **蕃茄鐘計時器**：設定專注時長與休息時間，以提升專注力與工作效率
- 陸續增加中 ...

## Plugins 市集

Plugins 為 VVIP 專屬功能，成為 VVIP 後可以在市集使用官方的 Plugins

![Plugins 市集](https://hyday.tw/docs/screenshots/concepts-plugins-1.png)

## 自訂與第三方 Plugins

開發者可以運用 HTML 與 JavaScript 撰寫個人專屬插件。關於 Host API 的完整定義、沙箱環境限制與開發流程，請參考獨立的**開發者文件**(開發中，敬請期待)
