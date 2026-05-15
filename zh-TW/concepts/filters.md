---
locale: zh-TW
category: concepts
slug: filters
source: src/content/docs/zh-TW/concepts/filters.tsx
---
> * 過濾器 (Filters) 協助使用者透過特定組合快速篩選筆記，將常用條件釘選於側邊欄，可將傳統的資料夾分類轉化為更靈活的標籤管理思維 *

## 可供過濾的條件種類

- **標籤過濾**：指定包含或排除特定的 `#標籤`
- **內容類型**：篩選特定類型，例如僅看 `article`(文章)、`card`(卡片) 或 `journal`(日記)
- **排序規則**：可以根據**標題、標籤、日期** 進行排序

## 條件邏輯組合

可以利用**全部符合 (AND) **或**任一符合 (OR) **來建構更多的篩選邏輯：

- **精確定位**：`#工作` AND `#週報`找出所有的工作週報
- **聯集搜索**：`#健康` OR `#運動`：同時檢視這兩類主題的筆記

## 釘選常用過濾器

將常用的過濾設定存為**釘選過濾器** (Pinned Filter)，將會常駐於側邊欄頂部：

![釘選過濾器](https://hyday.tw/docs/screenshots/concepts-filters-1.png)

> **ℹ️ Info**
>  在 Hyday 中，同一篇筆記可以同時出現在多個不同的過濾器視圖中，這正是標籤系統與過濾器協同運作的靈活性所在，打破了傳統樹狀資料夾一檔只能放一處的限制 

## 過濾器的儲存位置

目前的過濾器設定儲存於電腦本機設備的偏好設定檔 (`preferences.json`) 中。請注意，這些篩選組合目前不會跨裝置同步，若更換使用設備，需重新設定常用的過濾器。

## 延伸閱讀

- [釘選常用過濾器實戰](https://hyday.tw/docs/guides/pin-filters)：操作流程詳解。
- [過濾條件完整清單](https://hyday.tw/docs/reference/filter-conditions)：查看所有可用的篩選參數。
