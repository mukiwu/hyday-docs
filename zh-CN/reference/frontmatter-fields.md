---
locale: zh-CN
category: reference
slug: frontmatter-fields
source: src/content/docs/zh-CN/reference/frontmatter-fields.tsx
---
> * Frontmatter 是位于笔记最顶部的 YAML 格式区块，用于定义笔记的元资料 (Metadata)，Hyday 会自动解析并应用下列特定栏位 *

## 基本范例

```
``
```

## 标准核心栏位

   栏位名称 资料型别 功能说明    `title`string笔记的显示标题 `type`string笔记类型 (支援 `article` / `card` / `img` / `link` / `video`) `tags`string[]标签阵列，支援标准 YAML 列表或行内 `[a, b]` 写法。 `pinned`boolean是否将此笔记钉选于侧边栏顶部 `archived`boolean是否将笔记封存 (封存后默认不在主要列表中显示) `createdAt`datetime笔记建立时间 (系统自动填写，格式为 `YYYY-MM-DD HH:mm:ss`) `lastModified`datetime最后修改时间 (系统自动更新，格式同上) `createdBy`string建立来源 (使用者建立的笔记默认为 `User`)  

## 链接与媒体来源栏位

针对 `link` 或 `video` 类型的笔记，从外部撷取资料时 Hyday 会自动填入以下信息：

   栏位名称 资料型别 功能说明    `sourceUrl`string原始内容的来源 URL `sourceDomain`string来源网域 (由系统自动解析) `sourceTitle`string来源页面的原始标题 `sourceDescription`string来源页面的摘要描述 `sourceImage`string预览图片的储存路径 `sourceEmbedUrl`string用于嵌入显示的特殊 URL (如影片 Embed 链接) `capturedAt`datetime内容撷取的时间点 (格式为 `YYYY-MM-DD HH:mm:ss`)  

## 内容演化状态栏位

   栏位名称 资料型别 功能说明    `stage`string笔记演化阶段，仅接受 `seed` / `sapling` / `evergreen` 三个值 `stagePromotedAt`datetime记录进入当前阶段的时间点 (格式为 `YYYY-MM-DD HH:mm:ss`)  

## YAML 撰写注意事项

- Frontmatter 必须位于文件的**绝对开头**，并以三条连字号 `---` 前后包覆
- 阵列可使用 `[a, b]` 或标准 YAML 列表格式 (每行一个标签，例如 `- a`)
- 若标题包含中文或特殊字元，建议使用双引号包覆：`title: "我的专业笔记"`
- 布林值必须使用小写：`true` 或 `false`
