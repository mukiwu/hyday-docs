---
locale: zh-CN
category: start
slug: open-or-create-folder
source: src/content/docs/zh-CN/start/open-or-create-folder.tsx
---
> * Hyday 将整个文件夹视为个人笔记空间 *

## 打开现有文件夹

可直接打开任何存放有 Markdown 文件的文件夹，Hyday 会自动执行以下动作：

- 读取文件夹内的所有 `.md` 文件，并默认按修改时间进行排序
- 解析 Markdown 的 Frontmatter (例如 `title`、`type`、`tags` 等信息)
- 自动将位于 `journal/年份/` 路径下、档名为 `YYYY-MM-DD.md` 的文件辨识为日记

## 建立新文件夹

请在电脑中选择一个合适的位置 (建议路径为 `~/Documents/Hyday`)，Hyday 在建立新文件夹时：

- 除了 `.hyday/` 索引缓存 (建议加入 `.gitignore`) 外，不会存放任何专属的设置档，保持文件夹的纯净。
- 所撰写的每一篇笔记都是标准的纯 Markdown 格式，可使用任何文字编辑器随时打开。

> **ℹ️ Info**
>  只需在文件夹根目录执行 `git init`，并将 `.hyday/` 文件夹排除 (加入 `.gitignore`) 即可轻松管理。
