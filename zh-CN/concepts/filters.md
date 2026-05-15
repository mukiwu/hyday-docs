---
locale: zh-CN
category: concepts
slug: filters
source: src/content/docs/zh-CN/concepts/filters.tsx
---
> *过滤器 (Filters) 协助使用者透过特定组合快速筛选笔记，将常用条件钉选于侧边栏，可将传统的文件夹分类转化为更灵活的标签管理思维*

## 可供过滤的条件种类

- **标签过滤**：指定包含或排除特定的`#标签`
- **内容类型**：筛选特定类型，例如仅看`article`(文章)、`card`(卡片) 或`journal`(日记)
- **排序规则**：可以根据**标题、标签、日期**进行排序

## 条件逻辑组合

可以利用**全部符合 (AND)**或**任一符合 (OR)**来建构更多的筛选逻辑：

- **精确定位**：`#工作`AND`#周报`找出所有的工作周报
- **联集搜索**：`#健康`OR`#运动`：同时检视这两类主题的笔记

## 钉选常用过滤器

将常用的过滤设置存为**钉选过滤器**(Pinned Filter)，将会常驻于侧边栏顶部：

![钉选过滤器](https://hyday.tw/docs/screenshots/concepts-filters-1.png)

> **ℹ️ Info**
> 在 Hyday 中，同一篇笔记可以同时出现在多个不同的过滤器视图中，这正是标签系统与过滤器协同运作的灵活性所在，打破了传统树状文件夹一档只能放一处的限制

## 过滤器的储存位置

目前的过滤器设置储存于电脑本机设备的偏好设置档 (`preferences.json`) 中。请注意，这些筛选组合目前不会跨装置同步，若更换使用设备，需重新设置常用的过滤器。

## 延伸阅读

- [钉选常用过滤器实战](https://hyday.tw/docs/guides/pin-filters)：操作流程详解。
- [过滤条件完整清单](https://hyday.tw/docs/reference/filter-conditions)：查看所有可用的筛选参数。
