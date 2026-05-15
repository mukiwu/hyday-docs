---
locale: zh-TW
category: guides
slug: import-existing-notes
source: src/content/docs/zh-TW/guides/import-existing-notes.tsx
---
> * 不論是從 Obsidian、Bear、Notion 還是 Apple Notes 遷移而來，將資料搬移至 Hyday 的核心邏輯皆為：將原始資料匯出為 Markdown 格式，隨後直接在 Hyday 中開啟資料夾 *

## 從 Obsidian 遷移

Hyday 有特別替 Obsidian 的使用者做了完整的遷移規劃：

1. 在 Hyday 啟動頁**新增資料夾** → 從 Obsidian 匯入
2. 照著指引依序匯入筆記、日記以及圖片，Hyday 會自動識別所有的 `.md` 檔案、Frontmatter 元資料以及 `[[]]` 雙向連結

> **⚠️ Warning**
>  Hyday 尚不支援 Obsidian 的區塊級雙向連結 (如 `[[note#^block-id]]`) 這類語法將顯示為失效連結 

如果一開始沒有選擇轉移 Obsidian 檔案，事後也可以在設定 → 匯入 中選擇 Obsidian 資料夾進行轉移

![從 Obsidian 匯入](https://hyday.tw/docs/screenshots/guides-import-existing-notes-1.png)

## 從其他筆記工具遷移

除了 Obsidian 外，Hyday 沒有製作其他的筆記轉換工具，但可以透過第三方工具先將筆記轉換為 Markdown 格式，再自行放到 Hyday 的筆記資料夾中

> **ℹ️ Info**
>  搬家完成後，可嘗試在 Hyday 持續記錄一週的日記、體驗 LifeLog 標記的便利性，並建立幾組跨筆記的雙向連結。只有在實際使用中，才能深刻體會 Hyday 與傳統筆記工具在思考維度上的差異
