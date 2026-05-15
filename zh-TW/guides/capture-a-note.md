---
locale: zh-TW
category: guides
slug: capture-a-note
source: src/content/docs/zh-TW/guides/capture-a-note.tsx
---
> * 這份指南提供建立第一篇筆記的完整流程 *

## 1. 建立新筆記

按下快捷鍵 `⌘`+`N`，或點擊「筆記總覽」的「新增筆記」按鈕即可開啟新的空白筆記

## 2. 設定標題與 frontmatter

空白筆記的標題預設叫做**未命名筆記**，請修改成適當的標題名稱

**frontmatter** 是筆記最上方的一小段程式碼區域，用來存放筆記的**中繼資料**。以下是 frontmatter 的基本結構：

```
``
```

各欄位說明：

- `title`：筆記標題
- `type`：筆記類型，可填 `article`、`card`、`img`、`link`、`video`
- `stage`：成熟度階段，可填 `seed` (種子)、`sapling` (幼苗)、`evergreen` (長青)；未標記則省略此欄位
- `tags`：標籤清單，使用 YAML 陣列語法
- `pinned`：是否釘選到列表頂端

其他欄位 (如 `createdAt`、`lastModified`) 由 Hyday 自動維護，不需手動修改

![frontmatter](https://hyday.tw/docs/screenshots/capture-a-note-1.png)

## 3. 撰寫內容

可直接開始打字。若需調整格式，有以下幾種方式：

- **Markdown 語法**：使用 `**粗體**`、`*斜體*` 或 `## 二級標題` 等標準語法
- **斜線指令**：輸入 `/` 喚起命令選單，快速插入清單、引用、程式碼區塊或表格
- **系統快捷鍵**：直接使用 `⌘`+`B` 套用粗體或 `⌘`+`I` 套用斜體

## 4. 建立與其他筆記的連結

輸入 `[[` 搜尋並選取想連結的筆記，按下 Enter 鍵即可建立雙向連結

## 5. 無須手動儲存

Hyday 具備即時自動儲存功能。可隨時離開或關閉應用程式，所有改動皆會完整保存於本機資料夾中

> **ℹ️ Info**
>  嘗試寫一篇**為什麼我想試試 Hyday**。列出對筆記工具的期待、對現有工具的不滿，以及希望追蹤的主題。半年後再次回顧，將能看見自己真正的需求演進
