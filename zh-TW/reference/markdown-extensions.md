---
locale: zh-TW
category: reference
slug: markdown-extensions
source: src/content/docs/zh-TW/reference/markdown-extensions.tsx
---
> * Hyday 以標準的 GitHub Flavored Markdown (GFM) 為核心，並在此基礎上擴充了多項智慧標記功能。下表詳列目前系統支援的所有語法規範 *

## 標準 Markdown 語法

- **各級標題**：從 H1 (`#`) 至 H6 (`######`)
- **粗體**：`**粗體**`
- **斜體**：`*斜體*`
- **清單格式**：無序清單 (`-` 或 `*`) 與有序清單 (`1.`)
- **引用區塊**：使用 `>` 符號
- **程式碼標記**：行內程式碼 (使用反引號 ````) 與多行程式碼區塊 (使用 `````)
- **連結與圖片**：使用標準的 `[文字](URL)` 與 `![描述](路徑)` 語法
- **水平分隔線**：使用 `---`

## GFM (GitHub Flavored Markdown) 擴充

- **表格**：支援標準 Markdown 表格語法
- **待辦清單**：使用 `- [ ]` 或 `- [x]` 進行標註
- **刪除線**：使用雙波浪號 `~~刪除線~~`
- **智慧自動連結**：原始 URL 網址將自動轉換為可點擊連結

## 數學公式 (KaTeX)

數學公式在**編輯器中**需透過斜線指令插入，**不會**因為輸入 `$` 而自動觸發：

- 在編輯器內輸入 `/` 喚起選單，搜尋 **Equation** (區塊公式) 或 **Inline Equation** (行內公式)
- 插入後在 KaTeX 編輯框內撰寫 LaTeX 語法即可即時預覽

於 `.md` 檔案**外部編輯**時，可以直接寫成下列語法，Hyday 載入檔案時會自動解析為 KaTeX 渲染：

- **行內公式**：`$E = mc^2$`
- **區塊公式**：以雙錢字號包覆，例如 `$$\sum_{i=1}^n i$$`

## Mermaid 圖表

使用 `mermaid` 語言標記的程式碼區塊，會自動渲染成圖表：

```
``
```

![Mermaid 圖表](https://hyday.tw/docs/screenshots/reference-markdown-extensions-1.png)

於設定頁可調整節點間距、層級間距與配色主題。詳見 `設定 → 編輯器 → Mermaid`

## 提示區塊 (Callout)

在編輯器內輸入 `/` 喚起選單，搜尋 **Callout** 即可插入提示區塊，點擊 icon 可以切換 Callout 變體

存檔時，Hyday 會將 Callout 轉換為標準的 Markdown 語法

![Callout 提示區塊](https://hyday.tw/docs/screenshots/reference-markdown-extensions-2.png)

Hyday 原生支援 **10 種 Callout**：`note`、`abstract`、`important`、`reference`、`tip`、`warning`、`action`、`decision`、`question`、`idea`。

常見的 Obsidian 變體 (如 `info`、`caution`、`danger`、`todo`、`summary`、`quote` 等) 會自動對應到最接近的 Hyday 原生變體，匯入 Obsidian 筆記時無需手動修改

## Hyday 專屬擴充語法

   語法範例 功能用途    `[[筆記標題]]`建立雙向連結 (在編輯器內輸入 `[[` 會喚起筆記選擇器) `#標籤`在內文中直接定義標籤 `@人事物`標記具體的人物、地點或事物 `>(HH:mm)` / `<(HH:mm)` / `-(HH:mm)`LifeLog 時間標記 (任務開始 / 結束 / 當下) `%(內容)` / `!(內容)`LifeLog 內容標記 (想法 / 重要)  

## 目前不支援的語法

- `[[note#anchor]]`：Obsidian 的標題級錨點
- `[[note#^block-id]]`：Obsidian 的區塊引用 (Block Reference)
- `%%`：Obsidian 的隱藏註解語法
- **不安全的 HTML 標籤**：基本 HTML 標籤 (如 `div`、`span`、上述的 `u` / `mark` / `kbd` / `sup` / `sub`) 會被保留，但具備安全性風險的標籤 (如 `<script>`) 會被移除

> **ℹ️ Info**
>  儘管 Hyday 編輯器提供即時的視覺化排版效果，但**檔案內容永遠以純 Markdown 格式儲存**。如果使用外部文字編輯器開啟 `.md` 檔案，會完整看到上述原始語法符號。
