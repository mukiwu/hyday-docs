---
locale: zh-TW
category: guides
slug: use-command-palette
source: src/content/docs/zh-TW/guides/use-command-palette.tsx
---
> *Hyday 有提供命令面板，可讓使用者無須離開鍵盤即可快速跳轉至任何頁面或執行各種功能指令*

## 1. 核心快捷鍵對照

功能用途macOSWindows**命令面板**(執行功能指令)`Cmd`+`Shift`+`P``Ctrl`+`Shift`+`P`**全域搜尋**(尋找筆記與內容)`Cmd`+`K``Ctrl`+`K`

可將**命令面板**視為執行**動作**的窗口，而將**全域搜尋**視為尋找**資料**的入口。兩者相輔相成，分工明確。

![命令面板功能介面展示](https://hyday.tw/docs/screenshots/guides-use-command-palette-1.png)

## 2. 命令面板的主要功能範圍

- **內容建立**：例如**建立新筆記**或**新增日記**
- **快速導航**：和 Hyday Agent 對話、跳轉至日記、任務、白板、設定頁面或垃圾桶

## 3. 全域搜尋支援的檢索對象

- 筆記標題與全文內容檢索
- 標籤名稱 (Tags)
- 人事物 (Entities)
- 搭配 embedding 語意模型進行非關鍵字搜尋

## 4. 編輯器內的觸發機制

除了上述全域快捷鍵外，編輯器內也支援多種基於字元的快速觸發：

- `/`：喚起斜線指令選單。
- `[``[`：插入雙向連結。
- `#`：標記標籤。
- `@`：標記實體。

## 5. 一切功能的起點

若忘記某項功能的所在位置，最直覺的方式就是按下`Cmd (Ctrl)`+`Shift`+`P`並輸入關鍵字，系統通常能立即找出對應的操作指令。
