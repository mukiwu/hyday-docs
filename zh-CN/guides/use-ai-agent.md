---
locale: zh-CN
category: guides
slug: use-ai-agent
source: src/content/docs/zh-CN/guides/use-ai-agent.tsx
---
> *Hyday Agent 可以读写你的笔记、执行 skill、用互动 widget 回应、并透过 Buddy 累积对你的长期记忆，让 AI 真的变成**了解你的协作者**，而不是每次都要从头解释一遍的陌生人*

## 1. 进入 Hyday Agent

点击侧边栏的**Hyday Agent**进入对话页面

![Hyday Agent 主界面：左侧对话历史、中间消息流、右上模式切换](https://hyday.tw/docs/screenshots/guides-use-ai-agent-1.png)

## 2. Widget — 互动式回应

Hyday Agent 不只回传纯文字，它会根据任务性质呼叫**render_widget**工具，在对话中嵌入可互动的卡片。目前支援的 widget 类型：

- **note-list**：筛选结果以笔记清单呈现，可直接点击跳转
- **summary-card**：分段摘要，适合每日总结、健康检查报告
- **tag-cloud**：标签云，展示频率分布与颜色标记
- **health-report**：笔记库健检报告，依严重度分类列出问题项目
- **connection-map**：两则笔记的隐藏链接，附上「桥接概念」说明
- **action-buttons**：建议的下一步操作，点击可导航、套用标签、新增笔记或送出后续 prompt
- **option-compare**：「请你二选一」型的决策卡，并排呈现选项供比较

Widget 是 Agent 主动选用的，我们不需要在 prompt 里指定要哪一种，AI 会依照任务性质自动挑合适的格式

## 3. 技能 (Skill) — 一键启动的默认任务

Skill 是预先写好的常用工作流，分为几类：

- **内建 skill**：今日笔记摘要、发现笔记间的隐藏链接、笔记库健康检查、卡片组合成文章、笔记整理成白板
- **使用者 skill**：自行新增的个人化任务，最多 50 个，可随时编辑 / 复制 / 导出 / 删除
- **CLI skill**：当后端为 Claude Code / Gemini CLI 等 CLI 订阅时，CLI 本身的 skill 也会被列入菜单
- **MCP**：透过 MCP 协定接入的外部工具

点击**Hyday Agent 上方菜单的「技能」按钮**以集中管理 Skills，可重新排序、停用、或导出分享给其他人

## 4. Buddy — 长期记忆与人格

Hyday 在 Agent 旁边养着一只**Buddy**，它是 Agent 的记忆层。Buddy 会在你与 Agent 互动的过程中，**定期反思**并把对你的长期观察写进四份文件：

- **沟通风格**：你习惯的语气、回应节奏、喜欢简短还是详细
- **偏好**：你关心的主题、讨厌的东西、坚持的原则
- **反复主题**：你经常思考、追踪、纠结的主题
- **近期脉络**：最近这段时间正在做的事、卡关的点

每次 Agent 回应时会自动把这些观察当作背景注入，所以对话次数越多，**Agent 会越认识你**，不需要每次重新解释你是谁、在做什么

> **ℹ️ Info**
> 所有 Buddy 观察都存在笔记文件夹的`.hyday/observations/`底下，是纯 markdown 文件。你可以直接打开检视 Buddy 对你的理解，觉得不对也可以手动修改

## 5. 对话历程的储存位置

所有 Agent 对话集中储存在笔记文件夹的`.hyday/agent-conversations/v1.json`，可随文件夹一起备份或版本控制

## 典型应用场景

- **知识整理**：把 #灵感 标签里与产品设计相关的内容，整合成文章草稿
- **脉络追踪**：列出我最近 30 天有提到 @深度工作力 的所有段落
- **文件维护**：建立一篇 type 为 card 的笔记，标题 X、内容 Y
- **深度分析**：对 #身心状态 标签做一次脉络演化分析

## 延伸阅读

- [Agent 工具清单](https://hyday.tw/docs/reference/agent-tools)：完整工具与权限说明
- [Hyday Channel](https://hyday.tw/docs/guides/hyday-channel)：把 Claude Code 接成即时协作伙伴
- [疑难排解：工具呼叫失败](https://hyday.tw/docs/troubleshooting/agent-tool-failed)：常见错误对策
