---
locale: zh-TW
category: concepts
slug: note-types
source: src/content/docs/zh-TW/concepts/note-types.tsx
---
> *每一篇筆記都有其對應的**類型**(Note Type)，這將決定它在列表中的呈現方式，以及預設模板的內容。Hyday 目前內建了六種主要類型。*

## 六種內建類型

類型主要用途典型內容示例`article`一般文章與筆記想法整理、長篇筆記、會議或討論紀錄`card`卡片式短文摘錄、靈感片段、格言或佳句`img`圖片與視覺紀錄截圖、設計靈感圖、視覺化收藏`link`網址與書籤網路文章連結、參考資料書籤`video`影片筆記YouTube 學習紀錄、Podcast 心得`journal`日記條目每日生活紀錄，由系統根據檔名自動識別

## 如何指定筆記類型？

可透過以下三種方式設定：

- 新增文章時，直接填寫圖片、連結或影片的網址，讓 Hyday 自動辨識類型
- 在新增文章時，透過下拉選單選擇指定的類型，Hyday 會自動將格式寫入 Frontmatter
- 也能直接在文章中編輯類型

![筆記類型設定](https://hyday.tw/docs/screenshots/concepts-note-types-2.png)

![筆記類型設定](https://hyday.tw/docs/screenshots/concepts-note-types-1.png)

## 類型對功能的影響

**筆記類型並不影響核心功能**。所有類型的筆記皆可添加標籤、建立雙向連結或被 AI 代理 (Agent) 引用。類型主要影響**視覺呈現**：例如`img`類型在列表中會以縮圖優先顯示，而`link`則會展示來源網域與預覽資訊

![筆記類型的樣式差異](https://hyday.tw/docs/screenshots/concepts-note-types-3.png)

> **ℹ️ Info**
> `journal`類型是透過檔名格式辨識 (如`YYYY-MM-DD.md`)，因此無須手動在 Frontmatter 寫入`type: journal`。

## 延伸閱讀

- [筆記類型詳細清單](https://hyday.tw/docs/reference/note-types)：深入了解各類型的識別規則與 Frontmatter 範例。
