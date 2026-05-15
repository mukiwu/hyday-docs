---
locale: zh-CN
category: reference
slug: agent-tools
source: src/content/docs/zh-CN/reference/agent-tools.tsx
---
> *这份文件整理了 Hyday Agent 可调用的所有工具清单，为了确保资料安全，我们将工具分为**读取**与**修改**两类，并具备严谨的权限验证流程*

## 资料读取类工具

工具名称功能说明`read_note`读取指定笔记的内容`read_journal`读取特定日期的日记`list_notes`根据过滤条件列出符合的笔记清单`search`在整个文件夹中执行全文检索`tag_usage`查询标签的使用频率与相关统计`entity_usage`查询人事物标记的使用频率与关联性`get_lineage`取得特定主题的脉络分析数据

## 资料修改类工具

工具名称功能说明`create_note`建立一篇全新的笔记文件`update_note`修改既有笔记的内文或 Frontmatter`append_to_journal`将信息附加至今日的日记纪录中`add_tags`为指定笔记批量添加标签`archive_note`将不再使用的笔记移至封存状态

## 分析与处理类工具

工具名称功能说明`scan_tasks`从指定的内容中扫描并汇整待办事项

## UI 与视觉化工具

工具名称功能说明`render_widget`在对话窗口中渲染互动式组件 (如图表、选题对比或视觉化统计)
