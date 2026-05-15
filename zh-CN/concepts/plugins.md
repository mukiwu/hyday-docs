---
locale: zh-CN
category: concepts
slug: plugins
source: src/content/docs/zh-CN/concepts/plugins.tsx
---
> * Plugins 可以扩充 Hyday 笔记软件，通常会将常用的工具组件、第三方服务整合或自定义脚本挂载至 Hyday 中，与笔记文件夹协同运作 *

## 何谓 Hyday Plugins？

- **独立运作**：Plugins 可常驻于 Hyday 主界面或侧边栏
- **受控存取**：透过 Host API 进行笔记读写、标签查询或脉络分析
- **安全执行**：于沙箱 (Sandbox) 环境中运作，无法直接存取系统底层文件
- **权限透明**：每个 Plugin 安装时皆须明确声明其所需的存取权限

## Hyday 官方 Plugins

- **便笺**：将便条常驻在右上角，可以写想法、临时纪录、待办.. 等等的随手记信息，自动储存，有需要也可以直接新增到笔记或日记里
- **随机笔记**：随机显示任意一篇笔记，适合用来找寻灵感或是复习旧笔记
- **蕃茄钟计时器**：设置专注时长与休息时间，以提升专注力与工作效率
- 陆续增加中 ...

## Plugins 市集

Plugins 为 VVIP 专属功能，成为 VVIP 后可以在市集使用官方的 Plugins

![Plugins 市集](https://hyday.tw/docs/screenshots/concepts-plugins-1.png)

## 自定义与第三方 Plugins

开发者可以运用 HTML 与 JavaScript 撰写个人专属插件。关于 Host API 的完整定义、沙箱环境限制与开发流程，请参考独立的**开发者文件** (开发中，敬请期待)
