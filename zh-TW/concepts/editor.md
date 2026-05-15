---
locale: zh-TW
category: concepts
slug: editor
source: src/content/docs/zh-TW/concepts/editor.tsx
---
> *Hyday 編輯器完美結合了**所見即所得**(WYSIWYG) 的便利性與純 Markdown 檔案的穩定性。輸入體驗如同使用現代筆記軟體般流暢，但資料核心始終保持標準的 Markdown 格式。*

## 所見即所得的編輯體驗

無論是各級標題、粗體、清單或是程式碼區塊，編輯器都會即時呈現渲染後的排版外觀，讓輸入時無須面對如`**粗體**`等原始 Markdown 符號，專注於內容創作。

## 支援的 Markdown 語法

- **標準 Markdown**：包含標題、各類清單、引用塊與程式碼區塊。
- **GitHub Flavored Markdown (GFM)**：支援表格、待辦清單與刪除線。
- **數學公式**：支援撰寫`$\LaTeX$`公式。
- **提示區塊 (Callout)**：支援 Obsidian 風格的提示語法 (例如`> [!note]`或`> [!warning]`)。

## Hyday 專屬擴充語法

- [LifeLog Marks](https://hyday.tw/docs/concepts/lifelog-marks)：獨家的時間軸與想法紀錄標記。
- [雙向連結](https://hyday.tw/docs/concepts/backlinks)：輸入`[[`即可快速引用其他筆記。
- [標籤系統](https://hyday.tw/docs/concepts/tags)：輸入`#`即可為內容進行主題分類。
- [人事物標記](https://hyday.tw/docs/concepts/entities)：輸入`@`即可關聯特定的人、事、物。

## 斜線指令 (Slash Commands)

在編輯器中輸入`/`即可呼叫指令選單，快速插入各類區塊：

- 各層級標題 (H1 / H2 / H3)。
- 清單類型 (項目符號、編號清單、待辦事項)。
- 引用塊、程式碼區塊或提示區塊。
- 表格、分隔線、圖片上傳或 YouTube 影片嵌入。

![斜線指令選單介面](https://hyday.tw/docs/screenshots/concepts-editor-1.png)

## 鍵盤優先的操作邏輯

為了提升輸入效率，編輯器提供了多種常用的快捷鍵：

- `⌘`+`B`粗體、`⌘`+`I`斜體、`⌘`+`U`底線。
- `⌘`+`⇧`+`X`刪除線、`⌘`+`⇧`+`H`螢光標記。
- `⌘`+`E`行內程式碼、`⌘`+`↵`快速跳出程式碼區塊。

可參考[鍵盤快捷鍵清單](https://hyday.tw/docs/reference/keyboard-shortcuts)了解更多詳細指令。

> **ℹ️ Info**
> 在編輯器中所見到的所有精美排版，存入磁碟後皆會轉換為標準的純文字格式，確保資料的長期可讀性
