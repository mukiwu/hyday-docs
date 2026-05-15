---
locale: zh-CN
category: guides
slug: import-existing-notes
source: src/content/docs/zh-CN/guides/import-existing-notes.tsx
---
> * 不论是从 Obsidian、Bear、Notion 还是 Apple Notes 迁移而来，将资料搬移至 Hyday 的核心逻辑皆为：将原始资料导出为 Markdown 格式，随后直接在 Hyday 中打开文件夹 *

## 从 Obsidian 迁移

Hyday 有特别替 Obsidian 的使用者做了完整的迁移规划：

1. 在 Hyday 启动页**新增文件夹** → 从 Obsidian 导入
2. 照着指引依序导入笔记、日记以及图片，Hyday 会自动识别所有的 `.md` 文件、Frontmatter 元资料以及 `[[]]` 双向链接

> **⚠️ Warning**
>  Hyday 尚不支援 Obsidian 的区块级双向链接 (如 `[[note#^block-id]]`) 这类语法将显示为失效链接 

如果一开始没有选择转移 Obsidian 文件，事后也可以在设置 → 导入 中选择 Obsidian 文件夹进行转移

![从 Obsidian 导入](https://hyday.tw/docs/screenshots/guides-import-existing-notes-1.png)

## 从其他笔记工具迁移

除了 Obsidian 外，Hyday 没有制作其他的笔记转换工具，但可以透过第三方工具先将笔记转换为 Markdown 格式，再自行放到 Hyday 的笔记文件夹中

> **ℹ️ Info**
>  搬家完成后，可尝试在 Hyday 持续记录一周的日记、体验 LifeLog 标记的便利性，并建立几组跨笔记的双向链接。只有在实际使用中，才能深刻体会 Hyday 与传统笔记工具在思考维度上的差异
