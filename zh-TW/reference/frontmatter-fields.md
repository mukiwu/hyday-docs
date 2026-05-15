---
locale: zh-TW
category: reference
slug: frontmatter-fields
source: src/content/docs/zh-TW/reference/frontmatter-fields.tsx
---
> * Frontmatter 是位於筆記最頂部的 YAML 格式區塊，用於定義筆記的元資料 (Metadata)，Hyday 會自動解析並應用下列特定欄位 *

## 基本範例

```
``
```

## 標準核心欄位

   欄位名稱 資料型別 功能說明    `title`string筆記的顯示標題 `type`string筆記類型 (支援 `article` / `card` / `img` / `link` / `video`) `tags`string[]標籤陣列，支援標準 YAML 列表或行內 `[a, b]` 寫法。 `pinned`boolean是否將此筆記釘選於側邊欄頂部 `archived`boolean是否將筆記封存 (封存後預設不在主要列表中顯示) `createdAt`datetime筆記建立時間 (系統自動填寫，格式為 `YYYY-MM-DD HH:mm:ss`) `lastModified`datetime最後修改時間 (系統自動更新，格式同上) `createdBy`string建立來源 (使用者建立的筆記預設為 `User`)  

## 連結與媒體來源欄位

針對 `link` 或 `video` 類型的筆記，從外部擷取資料時 Hyday 會自動填入以下資訊：

   欄位名稱 資料型別 功能說明    `sourceUrl`string原始內容的來源 URL `sourceDomain`string來源網域 (由系統自動解析) `sourceTitle`string來源頁面的原始標題 `sourceDescription`string來源頁面的摘要描述 `sourceImage`string預覽圖片的儲存路徑 `sourceEmbedUrl`string用於嵌入顯示的特殊 URL (如影片 Embed 連結) `capturedAt`datetime內容擷取的時間點 (格式為 `YYYY-MM-DD HH:mm:ss`)  

## 內容演化狀態欄位

   欄位名稱 資料型別 功能說明    `stage`string筆記演化階段，僅接受 `seed` / `sapling` / `evergreen` 三個值 `stagePromotedAt`datetime記錄進入當前階段的時間點 (格式為 `YYYY-MM-DD HH:mm:ss`)  

## YAML 撰寫注意事項

- Frontmatter 必須位於檔案的**絕對開頭**，並以三條連字號 `---` 前後包覆
- 陣列可使用 `[a, b]` 或標準 YAML 列表格式 (每行一個標籤，例如 `- a`)
- 若標題包含中文或特殊字元，建議使用雙引號包覆：`title: "我的專業筆記"`
- 布林值必須使用小寫：`true` 或 `false`
