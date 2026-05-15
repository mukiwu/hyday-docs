---
locale: zh-CN
category: guides
slug: hyday-channel
source: src/content/docs/zh-CN/guides/hyday-channel.tsx
---
> * Hyday Channel 把 Claude Code 变成你在 Hyday 旁边的即时协作伙伴，透过双向通讯，让 Claude Code 主动感知你在笔记里读什么、写什么、停在哪里，并透过用 Hyday 的伙伴 (Buddy) 与你互动 *

## 为什么需要 Channel？

一般的 AI Agent 是「你问它才答」的单向对话，而 Hyday Channel 是**双向**的，这表示我们在笔记里的阅读与写作行为会即时被 Claude Code 看到，它可以主动丢出观察、提醒、或让你选择下一步要做什么

例如：

- 你连续阅读同一篇笔记 30 秒以上，Claude Code 会主动拉出相关的历史笔记
- 你写到一半停了 15 秒，Claude Code 可能会问「需要我帮你接下去吗？」
- 你在处理一个棘手主题，Claude Code 可以用 Buddy 的记忆提醒你过去类似情境怎么处理

## 运作原理

Channel 透过 **Hyday MCP (`@mukiwu/hyday-channel`)** 与 Claude Code 对接：MCP server 由 Claude Code 以子程序方式启动，并在本机开一个轻量 HTTP 伺服器 (默认 port `8789`)。Hyday app 把事件 POST 过去、Claude Code 透过 MCP 的 reply 工具回送，整个通讯只在本机，**不经过任何云端中继**

- **Hyday → Claude Code**：阅读、写作、消息等事件即时推送
- **Claude Code → Hyday**：回应透过 Buddy 的对话框呈现，并可附带 widget

> **ℹ️ Info**
>  本机需有 Claude Code CLI (v2.1.80 以上) 并完成登录，加上 Bun 或 Node.js 18+；Hyday 端则需先孵化一只 Buddy (在 Hyday Agent 页面进行)，因为 Channel 的对话窗口绑在 Buddy 上 

## 1. 安装 Hyday MCP

在你的 Hyday 笔记文件夹根目录建立 `.mcp.json` 文件，内容如下：

```
``
```

透过 Hyday MCP，Claude Code 可以：

- **即时接收 Hyday 推送的事件**：你正在阅读哪篇笔记、停留多久、写到什么段落、传了什么消息
- **回送消息到 Buddy 对话气泡**：透过内建的 `reply` 工具，把回复 (支援 markdown、清单、表格、程序码区块) 直接显示在 Hyday 右下角
- **读写你的笔记文件夹**：因为 Claude Code 启动时 `cd` 到笔记文件夹，可以直接读、搜索、新增、修改 markdown 文件 (透过 Claude Code 内建的文件工具)
- **对你的笔记做深度任务**：归纳主题、找出被遗忘的关联、产出摘要、针对你正在读的内容提出洞察

第一次启动时，MCP server 会自动产生一份 `CLAUDE.md` 描述笔记文件夹结构，让 Claude 不必每次重新探索目录

## 2. 启动 Claude Code

切换到刚放 `.mcp.json` 的笔记文件夹，启动 Claude Code：

```
``
```

Hyday 侧边栏的 Buddy 图示会从「未连线」变成「已连线」，并随 Claude Code 当下状态显示**阅读中**、**写作中**、**思考中**等提示

![Hyday 侧边栏显示 Channel 已连线状态，并有 Buddy 对话气泡](https://hyday.tw/docs/screenshots/guides-hyday-channel-1.png)

## 3. 跟 Claude Code 对话

按下 **Cmd + Shift + B** 切换 Channel 对话气泡，或点右侧的 **Hyday Channel** 进入完整页面。气泡里可以：

- 输入文字、上传图片给 Claude Code
- 看到 Claude Code 主动丢出的观察、widget、建议下一步

## 4. 隐私事件开关

并不是所有行为都要推给 Claude Code。在**设置 → AI → Channel**可以分项开关以下事件：

- **笔记阅读**：停留在同一篇笔记 30 秒以上时的阅读事件
- **日记阅读**：停留在日记页面的阅读事件
- **写作活动**：你停止打字 15 秒后的写作事件 (含当前段落的内容差异)
- **聊天消息**：你主动传送的消息

## 5. 跟 Hyday Agent 的差异

    Hyday Agent Hyday Channel     运作模式 你问才答的对话 双向，AI 可主动发起   后端 API / CLI / Ollama 皆可 Claude Code (专属)   感知能力 只看你送进来的 prompt 读写行为即时推送   适合情境 明确任务、执行 skill 长时间陪伴、即时建议   

> **ℹ️ Info**
>  Hyday Agent 跟 Channel 是两条独立的线路。可以一边跑 Agent 处理明确任务、一边让 Channel 在背景观察你的阅读写作流动，互不干扰 

## 常见问题

### 为什么只支援 Claude Code？

Channel 需要 CLI 端能透过 MCP 协定**主动回传消息**并理解 Hyday 推送的事件结构，目前只有 Claude Code 的 development-channels 模式针对这套协定做了实作。未来不排除支援其他 CLI

### 连线断掉怎么办？

当 Claude Code 结束或当机，Hyday 侧边栏会显示「Channel 未连线」并提供「重新侦测」按钮。Channel 服务也会每 30 秒自动重试一次，**不需要重启 Hyday**

### 对话会被存到哪里？

Channel 对话目前储存在记忆体中，Hyday 重启后会清空，这是设计上的取舍，让 Channel 保留「即时对话」的性质。而 Buddy 的长期记忆会透过反思流程写到 `.hyday/observations/`，让重要的观察不会遗失

## 延伸阅读

- [Hyday Agent](https://hyday.tw/docs/guides/use-ai-agent)：理解 Agent、Skill、Widget、Buddy 的完整脉络
- [设置 AI 供应商](https://hyday.tw/docs/guides/configure-ai-provider)：多个 AI 供应商的设置与介绍
