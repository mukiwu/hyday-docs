---
locale: zh-TW
category: reference
slug: agent-tools
source: src/content/docs/zh-TW/reference/agent-tools.tsx
---
> * 這份文件整理了 Hyday Agent 可調用的所有工具清單，為了確保資料安全，我們將工具分為**讀取**與**修改**兩類，並具備嚴謹的權限驗證流程 *

## 資料讀取類工具

   工具名稱 功能說明    `read_note`讀取指定筆記的內容 `read_journal`讀取特定日期的日記 `list_notes`根據過濾條件列出符合的筆記清單 `search`在整個資料夾中執行全文檢索 `tag_usage`查詢標籤的使用頻率與相關統計 `entity_usage`查詢人事物標記的使用頻率與關聯性 `get_lineage`取得特定主題的脈絡分析數據  

## 資料修改類工具

   工具名稱 功能說明    `create_note`建立一篇全新的筆記檔案 `update_note`修改既有筆記的內文或 Frontmatter `append_to_journal`將資訊附加至今日的日記紀錄中 `add_tags`為指定筆記批量添加標籤 `archive_note`將不再使用的筆記移至封存狀態  

## 分析與處理類工具

   工具名稱 功能說明    `scan_tasks`從指定的內容中掃描並彙整待辦事項  

## UI 與視覺化工具

   工具名稱 功能說明    `render_widget`在對話視窗中渲染互動式組件 (如圖表、選題對比或視覺化統計)
