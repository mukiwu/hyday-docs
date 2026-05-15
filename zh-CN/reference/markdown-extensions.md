---
locale: zh-CN
category: reference
slug: markdown-extensions
source: src/content/docs/zh-CN/reference/markdown-extensions.tsx
---
> * Hyday 以标准的 GitHub Flavored Markdown (GFM) 为核心，并在此基础上扩充了多项智能标记功能。下表详列目前系统支援的所有语法规范 *

## 标准 Markdown 语法

- **各级标题**：从 H1 (`#`) 至 H6 (`######`)
- **粗体**：`**粗体**`
- **斜体**：`*斜体*`
- **清单格式**：无序清单 (`-` 或 `*`) 与有序清单 (`1.`)
- **引用区块**：使用 `>` 符号
- **程序码标记**：行内程序码 (使用反引号 ````) 与多行程序码区块 (使用 `````)
- **链接与图片**：使用标准的 `[文字](URL)` 与 `![描述](路径)` 语法
- **水平分隔线**：使用 `---`

## GFM (GitHub Flavored Markdown) 扩充

- **表格**：支援标准 Markdown 表格语法
- **待办清单**：使用 `- [ ]` 或 `- [x]` 进行标注
- **删除线**：使用双波浪号 `~~删除线~~`
- **智能自动链接**：原始 URL 网址将自动转换为可点击链接

## 数学公式 (KaTeX)

数学公式在**编辑器中**需透过斜线指令插入，**不会**因为输入 `$` 而自动触发：

- 在编辑器内输入 `/` 唤起菜单，搜索 **Equation** (区块公式) 或 **Inline Equation** (行内公式)
- 插入后在 KaTeX 编辑框内撰写 LaTeX 语法即可即时预览

于 `.md` 文件**外部编辑**时，可以直接写成下列语法，Hyday 加载文件时会自动解析为 KaTeX 渲染：

- **行内公式**：`$E = mc^2$`
- **区块公式**：以双钱字号包覆，例如 `$$\sum_{i=1}^n i$$`

## Mermaid 图表

使用 `mermaid` 语言标记的程序码区块，会自动渲染成图表：

```
``
```

![Mermaid 图表](https://hyday.tw/docs/screenshots/reference-markdown-extensions-1.png)

于设置页可调整节点间距、层级间距与配色主题。详见 `设置 → 编辑器 → Mermaid`

## 提示区块 (Callout)

在编辑器内输入 `/` 唤起菜单，搜索 **Callout** 即可插入提示区块，点击 icon 可以切换 Callout 变体

存档时，Hyday 会将 Callout 转换为标准的 Markdown 语法

![Callout 提示区块](https://hyday.tw/docs/screenshots/reference-markdown-extensions-2.png)

Hyday 原生支援 **10 种 Callout**：`note`、`abstract`、`important`、`reference`、`tip`、`warning`、`action`、`decision`、`question`、`idea`。

常见的 Obsidian 变体 (如 `info`、`caution`、`danger`、`todo`、`summary`、`quote` 等) 会自动对应到最接近的 Hyday 原生变体，导入 Obsidian 笔记时无需手动修改

## Hyday 专属扩充语法

   语法范例 功能用途    `[[笔记标题]]`建立双向链接 (在编辑器内输入 `[[` 会唤起笔记选择器) `#标签`在内文中直接定义标签 `@人事物`标记具体的人物、地点或事物 `>(HH:mm)` / `<(HH:mm)` / `-(HH:mm)`LifeLog 时间标记 (任务开始 / 结束 / 当下) `%(内容)` / `!(内容)`LifeLog 内容标记 (想法 / 重要)  

## 目前不支援的语法

- `[[note#anchor]]`：Obsidian 的标题级锚点
- `[[note#^block-id]]`：Obsidian 的区块引用 (Block Reference)
- `%%`：Obsidian 的隐藏注解语法
- **不安全的 HTML 标签**：基本 HTML 标签 (如 `div`、`span`、上述的 `u` / `mark` / `kbd` / `sup` / `sub`) 会被保留，但具备安全性风险的标签 (如 `<script>`) 会被移除

> **ℹ️ Info**
>  尽管 Hyday 编辑器提供即时的视觉化排版效果，但**文件内容永远以纯 Markdown 格式储存**。如果使用外部文字编辑器打开 `.md` 文件，会完整看到上述原始语法符号。
