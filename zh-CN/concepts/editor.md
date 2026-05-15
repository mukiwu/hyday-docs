---
locale: zh-CN
category: concepts
slug: editor
source: src/content/docs/zh-CN/concepts/editor.tsx
---
> *Hyday 编辑器完美结合了**所见即所得**(WYSIWYG) 的便利性与纯 Markdown 文件的稳定性。输入体验如同使用现代笔记软件般流畅，但资料核心始终保持标准的 Markdown 格式。*

## 所见即所得的编辑体验

无论是各级标题、粗体、清单或是程序码区块，编辑器都会即时呈现渲染后的排版外观，让输入时无须面对如`**粗体**`等原始 Markdown 符号，专注于内容创作。

## 支援的 Markdown 语法

- **标准 Markdown**：包含标题、各类清单、引用块与程序码区块。
- **GitHub Flavored Markdown (GFM)**：支援表格、待办清单与删除线。
- **数学公式**：支援撰写`$\LaTeX$`公式。
- **提示区块 (Callout)**：支援 Obsidian 风格的提示语法 (例如`> [!note]`或`> [!warning]`)。

## Hyday 专属扩充语法

- [LifeLog Marks](https://hyday.tw/docs/concepts/lifelog-marks)：独家的时间轴与想法纪录标记。
- [双向链接](https://hyday.tw/docs/concepts/backlinks)：输入`[[`即可快速引用其他笔记。
- [标签系统](https://hyday.tw/docs/concepts/tags)：输入`#`即可为内容进行主题分类。
- [人事物标记](https://hyday.tw/docs/concepts/entities)：输入`@`即可关联特定的人、事、物。

## 斜线指令 (Slash Commands)

在编辑器中输入`/`即可呼叫指令菜单，快速插入各类区块：

- 各层级标题 (H1 / H2 / H3)。
- 清单类型 (项目符号、编号清单、待办事项)。
- 引用块、程序码区块或提示区块。
- 表格、分隔线、图片上传或 YouTube 影片嵌入。

![斜线指令菜单界面](https://hyday.tw/docs/screenshots/concepts-editor-1.png)

## 键盘优先的操作逻辑

为了提升输入效率，编辑器提供了多种常用的快捷键：

- `⌘`+`B`粗体、`⌘`+`I`斜体、`⌘`+`U`底线。
- `⌘`+`⇧`+`X`删除线、`⌘`+`⇧`+`H`萤光标记。
- `⌘`+`E`行内程序码、`⌘`+`↵`快速跳出程序码区块。

可参考[键盘快捷键清单](https://hyday.tw/docs/reference/keyboard-shortcuts)了解更多详细指令。

> **ℹ️ Info**
> 在编辑器中所见到的所有精美排版，存入磁碟后皆会转换为标准的纯文字格式，确保资料的长期可读性
