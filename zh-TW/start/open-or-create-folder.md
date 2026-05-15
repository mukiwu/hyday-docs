---
locale: zh-TW
category: start
slug: open-or-create-folder
source: src/content/docs/zh-TW/start/open-or-create-folder.tsx
---
> *Hyday 將整個資料夾視為個人筆記空間*

## 開啟現有資料夾

可直接開啟任何存放有 Markdown 檔案的資料夾，Hyday 會自動執行以下動作：

- 讀取資料夾內的所有`.md`檔案，並預設按修改時間進行排序
- 解析 Markdown 的 Frontmatter (例如`title`、`type`、`tags`等資訊)
- 自動將位於`journal/年份/`路徑下、檔名為`YYYY-MM-DD.md`的檔案辨識為日記

## 建立新資料夾

請在電腦中選擇一個合適的位置 (建議路徑為`~/Documents/Hyday`)，Hyday 在建立新資料夾時：

- 除了`.hyday/`索引快取 (建議加入`.gitignore`) 外，不會存放任何專屬的設定檔，保持資料夾的純淨。
- 所撰寫的每一篇筆記都是標準的純 Markdown 格式，可使用任何文字編輯器隨時開啟。

> **ℹ️ Info**
> 只需在資料夾根目錄執行`git init`，並將`.hyday/`資料夾排除 (加入`.gitignore`) 即可輕鬆管理。
