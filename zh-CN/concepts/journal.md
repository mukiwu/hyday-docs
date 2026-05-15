---
locale: zh-CN
category: concepts
slug: journal
source: src/content/docs/zh-CN/concepts/journal.tsx
---
> *日记 (Journal) 是以**天**为单位的纪录，Hyday 推荐搭配 LifeLog 时间标记，将生活点滴、会议纪录、待办事项与灵感闪现，汇整于同一条清晰的时间轴上。*

## 自动识别机制

只要文件名称符合下列格式，Hyday 就会自动将其归类为日记类型：

- `YYYY-MM-DD.md`(例如`2026-05-09.md`)
- `YYYY.MM.DD.md`(例如`2026.05.09.md`)
- 点选侧边栏的「日记」菜单就会自动新增今天的日记文件，使用者不需要手动建立

## 日记的构成：区块 (Block)

在 Hyday 中，编辑器中看到的内容，并非单一的大篇幅文字，而是由多个**区块 (Block)**构成。每个区块可以代表不同的内容类型：

- 一段纯文字
- 一个 LifeLog 时间标记 (如任务、想法、重要事项)
- 一张图片或附件
- 一个提示区块 (Callout)、引用块或程序码区块
- 待办清单项目

![日记页面展示：一天由多个不同类型的区块组成](https://hyday.tw/docs/screenshots/concepts-journal-1.png)

## 跨日期对照阅读

可同时选取两天的日记并启用**分割视图**，即可左右并排对照。这在撰写周记或进行月度回顾时格外有帮助。

![分割视图：左右面板并排显示](https://hyday.tw/docs/screenshots/concepts-journal-2.png)

## 为什么坚持**一天一文件**？

将每一天的纪录独立为单一 Markdown 文件具备以下优势：

- **检索方便**：易于使用`grep`或各类搜索工具进行精确检索
- **版本控制清晰**：Git 的差异比对 (diff) 能清楚呈现每天的修改纪录
- **资料安全**：若单一文件损坏，不会影响到其他日期
- **相容性高**：外部指令码 (Scripts) 能轻松针对特定日期文件进行自动化处理

> **ℹ️ Info**
> 日记文件皆为标准 Markdown 格式，可使用任何喜爱的编辑器进行撰写，Hyday 会在下次启动时自动读取最新的改动

## 延伸阅读

- [LifeLog 时间标记](https://hyday.tw/docs/concepts/lifelog-marks)：了解如何让日记转化为可供分析的数据时间轴
- [撰写日记](https://hyday.tw/docs/guides/create-journal-entry)：实战流程引导
