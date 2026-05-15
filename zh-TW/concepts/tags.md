---
locale: zh-TW
category: concepts
slug: tags
source: src/content/docs/zh-TW/concepts/tags.tsx
---
> * 標籤 (Tags) 是管理與分類筆記最輕量的方式。Hyday 同時支援**行內標籤**與 **Frontmatter 標籤**兩種標註方式 *

## 兩種標註方式

- **行內標籤 (Inline Tags)**：直接在筆記內文中撰寫 `#標籤名稱`，系統將自動將該標籤辨識為行內標籤。
- **Frontmatter 標籤**：在筆記最上方的元資料區塊定義：

```
``
```

不論採用哪種方式，所有標籤都會彙整至同一個標籤索引系統中

## 如何選擇適合的標註方式？

   場景需求 建議使用     整篇筆記皆圍繞某個特定主題 Frontmatter   僅文中某一段落與該主題相關 內聯 `#標籤`   希望標籤緊隨文字脈絡，方便閱讀中跳轉 內聯標籤   希望被搜尋系統檢索，但不希望干擾閱讀視覺 Frontmatter   

## 標籤探索 (Tag Exploration)

點擊任何標籤即可開啟**標籤探索抽屜** (Tag Explore Drawer)，可檢視：

- **使用紀錄**：列出所有標註該標籤的筆記，以及熱度分布時間軸
- **相關標籤 (Co-occurrence)**：顯示與當前標籤最常同時出現的其他相關主題

![標籤探索抽屜介面展示](https://hyday.tw/docs/screenshots/concepts-tags-1.png)

## 延伸閱讀

- [使用標籤進行分類](https://hyday.tw/docs/guides/organize-with-tags)：基礎實戰分享
- [探索主題脈絡](https://hyday.tw/docs/guides/explore-tag-lineage)：標籤應用的進階導引
