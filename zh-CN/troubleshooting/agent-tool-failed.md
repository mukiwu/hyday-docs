---
locale: zh-CN
category: troubleshooting
slug: agent-tool-failed
source: src/content/docs/zh-CN/troubleshooting/agent-tool-failed.tsx
---
> * 若 AI Agent 在执行工具呼叫后跳出错误，或是陷入重复呼叫同一工具而无结果的无限循环，请参考以下排除方案 *

## 1. 陷入 Widget 渲染重试循环

当 Agent 尝试呼叫 `render_widget` 失败时，偶尔会发生过度重试的情况。**症状表现**：

- 对话窗口中不断自动跳出新的、且呈现错误的 Widget 组件
- 对话历程长度急遽增加，导致 `.hyday/agent-conversations/v1.json` 文件异常变大并拖慢系统效能

**处理对策**：

1. 立即点击对话界面右上角的**停止**按钮强行中断任务
2. 弃用当前对话，并打开一段新对话
3. 若特定指令必然触发此现象，请前往 GitHub 提交 Issue 并附上该 Widget 的内容格式范例

## 2. 服务商不支援工具呼叫

若 AI Agent 完全不执行任何工具，仅透过纯文字描述其**想做的事**，通常代表选用的模型不支援 Function Calling 语法

请参考 [AI 供应商对照表](/docs/reference/ai-providers)，确保已切换至具备代理能力的进阶模型

## 3. 清理损坏的对话纪录文件

若某段对话文件因先前的异常循环而导致打开缓慢或卡死，建议将其彻底移除：

1. 于侧边栏对话列表中找到该问题对话
2. 点击 「...」 选取**删除对话**进行删除
3. 从干净的状态重新开始对话任务

> **⚠️ Warning**
>  清理对话纪录仅会影响 `.hyday/agent-conversations/v1.json` 内被删除的那段对话，**不会删除或修改笔记原文内容**。但请注意，**删除对话**是一项不可撤销的操作，一旦执行即无法恢复。若内容极其重要，建议先备份对话档
