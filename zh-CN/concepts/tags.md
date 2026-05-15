---
locale: zh-CN
category: concepts
slug: tags
source: src/content/docs/zh-CN/concepts/tags.tsx
---
> * 标签 (Tags) 是管理与分类笔记最轻量的方式。Hyday 同时支援**行内标签**与 **Frontmatter 标签**两种标注方式 *

## 两种标注方式

- **行内标签 (Inline Tags)**：直接在笔记内文中撰写 `#标签名称`，系统将自动将该标签辨识为行内标签。
- **Frontmatter 标签**：在笔记最上方的元资料区块定义：

```
``
```

不论采用哪种方式，所有标签都会汇整至同一个标签索引系统中

## 如何选择适合的标注方式？

   场景需求 建议使用     整篇笔记皆围绕某个特定主题 Frontmatter   仅文中某一段落与该主题相关 内联 `#标签`   希望标签紧随文字脉络，方便阅读中跳转 内联标签   希望被搜索系统检索，但不希望干扰阅读视觉 Frontmatter   

## 标签探索 (Tag Exploration)

点击任何标签即可打开**标签探索抽屉** (Tag Explore Drawer)，可检视：

- **使用纪录**：列出所有标注该标签的笔记，以及热度分布时间轴
- **相关标签 (Co-occurrence)**：显示与当前标签最常同时出现的其他相关主题

![标签探索抽屉界面展示](https://hyday.tw/docs/screenshots/concepts-tags-1.png)

## 延伸阅读

- [使用标签进行分类](https://hyday.tw/docs/guides/organize-with-tags)：基础实战分享
- [探索主题脉络](https://hyday.tw/docs/guides/explore-tag-lineage)：标签应用的进阶导引
