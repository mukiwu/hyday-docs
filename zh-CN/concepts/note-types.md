---
locale: zh-CN
category: concepts
slug: note-types
source: src/content/docs/zh-CN/concepts/note-types.tsx
---
> *每一篇笔记都有其对应的**类型**(Note Type)，这将决定它在列表中的呈现方式，以及默认模板的内容。Hyday 目前内建了六种主要类型。*

## 六种内建类型

类型主要用途典型内容示例`article`一般文章与笔记想法整理、长篇笔记、会议或讨论纪录`card`卡片式短文摘录、灵感片段、格言或佳句`img`图片与视觉纪录截图、设计灵感图、视觉化收藏`link`网址与书签网络文章链接、参考资料书签`video`影片笔记YouTube 学习纪录、Podcast 心得`journal`日记条目每日生活纪录，由系统根据档名自动识别

## 如何指定笔记类型？

可透过以下三种方式设置：

- 新增文章时，直接填写图片、链接或影片的网址，让 Hyday 自动辨识类型
- 在新增文章时，透过下拉菜单选择指定的类型，Hyday 会自动将格式写入 Frontmatter
- 也能直接在文章中编辑类型

![笔记类型设置](https://hyday.tw/docs/screenshots/concepts-note-types-2.png)

![笔记类型设置](https://hyday.tw/docs/screenshots/concepts-note-types-1.png)

## 类型对功能的影响

**笔记类型并不影响核心功能**。所有类型的笔记皆可添加标签、建立双向链接或被 AI 代理 (Agent) 引用。类型主要影响**视觉呈现**：例如`img`类型在列表中会以缩图优先显示，而`link`则会展示来源网域与预览信息

![笔记类型的样式差异](https://hyday.tw/docs/screenshots/concepts-note-types-3.png)

> **ℹ️ Info**
> `journal`类型是透过档名格式辨识 (如`YYYY-MM-DD.md`)，因此无须手动在 Frontmatter 写入`type: journal`。

## 延伸阅读

- [笔记类型详细清单](https://hyday.tw/docs/reference/note-types)：深入了解各类型的识别规则与 Frontmatter 范例。
