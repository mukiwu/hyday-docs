---
locale: zh-TW
category: concepts
slug: journal
source: src/content/docs/zh-TW/concepts/journal.tsx
---
> *日記 (Journal) 是以**天**為單位的紀錄，Hyday 推薦搭配 LifeLog 時間標記，將生活點滴、會議紀錄、待辦事項與靈感閃現，彙整於同一條清晰的時間軸上。*

## 自動識別機制

只要檔案名稱符合下列格式，Hyday 就會自動將其歸類為日記類型：

- `YYYY-MM-DD.md`(例如`2026-05-09.md`)
- `YYYY.MM.DD.md`(例如`2026.05.09.md`)
- 點選側邊欄的「日記」選單就會自動新增今天的日記檔案，使用者不需要手動建立

## 日記的構成：區塊 (Block)

在 Hyday 中，編輯器中看到的內容，並非單一的大篇幅文字，而是由多個**區塊 (Block)**構成。每個區塊可以代表不同的內容類型：

- 一段純文字
- 一個 LifeLog 時間標記 (如任務、想法、重要事項)
- 一張圖片或附件
- 一個提示區塊 (Callout)、引用塊或程式碼區塊
- 待辦清單項目

![日記頁面展示：一天由多個不同類型的區塊組成](https://hyday.tw/docs/screenshots/concepts-journal-1.png)

## 跨日期對照閱讀

可同時選取兩天的日記並啟用**分割視圖**，即可左右並排對照。這在撰寫週記或進行月度回顧時格外有幫助。

![分割視圖：左右面板並排顯示](https://hyday.tw/docs/screenshots/concepts-journal-2.png)

## 為什麼堅持**一天一檔案**？

將每一天的紀錄獨立為單一 Markdown 檔案具備以下優勢：

- **檢索方便**：易於使用`grep`或各類搜尋工具進行精確檢索
- **版本控制清晰**：Git 的差異比對 (diff) 能清楚呈現每天的修改紀錄
- **資料安全**：若單一檔案損壞，不會影響到其他日期
- **相容性高**：外部指令碼 (Scripts) 能輕鬆針對特定日期檔案進行自動化處理

> **ℹ️ Info**
> 日記檔案皆為標準 Markdown 格式，可使用任何喜愛的編輯器進行撰寫，Hyday 會在下次啟動時自動讀取最新的改動

## 延伸閱讀

- [LifeLog 時間標記](https://hyday.tw/docs/concepts/lifelog-marks)：了解如何讓日記轉化為可供分析的數據時間軸
- [撰寫日記](https://hyday.tw/docs/guides/create-journal-entry)：實戰流程引導
