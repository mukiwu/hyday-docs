---
locale: zh-CN
category: guides
slug: capture-a-note
source: src/content/docs/zh-CN/guides/capture-a-note.tsx
---
> * 这份指南提供建立第一篇笔记的完整流程 *

## 1. 建立新笔记

按下快捷键 `⌘`+`N`，或点击「笔记总览」的「新增笔记」按钮即可打开新的空白笔记

## 2. 设置标题与 frontmatter

空白笔记的标题默认叫做**未命名笔记**，请修改成适当的标题名称

**frontmatter** 是笔记最上方的一小段程序码区域，用来存放笔记的**中继资料**。以下是 frontmatter 的基本结构：

```
``
```

各栏位说明：

- `title`：笔记标题
- `type`：笔记类型，可填 `article`、`card`、`img`、`link`、`video`
- `stage`：成熟度阶段，可填 `seed` (种子)、`sapling` (幼苗)、`evergreen` (长青)；未标记则省略此栏位
- `tags`：标签清单，使用 YAML 阵列语法
- `pinned`：是否钉选到列表顶端

其他栏位 (如 `createdAt`、`lastModified`) 由 Hyday 自动维护，不需手动修改

![frontmatter](https://hyday.tw/docs/screenshots/capture-a-note-1.png)

## 3. 撰写内容

可直接开始打字。若需调整格式，有以下几种方式：

- **Markdown 语法**：使用 `**粗体**`、`*斜体*` 或 `## 二级标题` 等标准语法
- **斜线指令**：输入 `/` 唤起命令菜单，快速插入清单、引用、程序码区块或表格
- **系统快捷键**：直接使用 `⌘`+`B` 套用粗体或 `⌘`+`I` 套用斜体

## 4. 建立与其他笔记的链接

输入 `[[` 搜索并选取想链接的笔记，按下 Enter 键即可建立双向链接

## 5. 无须手动储存

Hyday 具备即时自动储存功能。可随时离开或关闭应用程序，所有改动皆会完整保存于本机文件夹中

> **ℹ️ Info**
>  尝试写一篇**为什么我想试试 Hyday**。列出对笔记工具的期待、对现有工具的不满，以及希望追踪的主题。半年后再次回顾，将能看见自己真正的需求演进
