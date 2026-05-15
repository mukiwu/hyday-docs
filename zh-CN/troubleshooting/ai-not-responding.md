---
locale: zh-CN
category: troubleshooting
slug: ai-not-responding
source: src/content/docs/zh-CN/troubleshooting/ai-not-responding.tsx
---
> * 若在使用 AI 功能时遇到系统无反应、持续加载、或跳出错误消息时，请参考以下诊断流程进行排除 *

## 1. 检查服务供应商的连线状态

请前往**设置** (`⌘` + `,`) → **AI**分页，找到正在使用的供应商信息，点击**测试连线**按钮。连线失败的常见原因包括：

- **API Key 异常**：金钥已过期、被撤销或输入不完整
- **帐户额度不足**：云端供应商的额度已耗尽
- **服务端故障**：该供应商的伺服器目前正处于维护或异常状态

## 2. 云端供应商：检查网络环境

部分办公室网络或防火墙设置可能会阻挡特定的 AI 服务通讯。可以尝试：

- 切换至其他网络环境 (例如使用手机热点) 进行交叉测试
- 造访供应商官方状态页面确认服务状况：[OpenAI Status](https://status.openai.com/)、[Anthropic Status](https://status.anthropic.com/)、[Google Cloud Status](https://status.cloud.google.com/)

## 3. 本机 Ollama：确认服务是否正常运作

请于终端机执行以下指令测试 Ollama 是否正常回应：

```
``
```

若回应 200 代表正常；若回应 `Connection refused`，代表 Ollama 服务尚未启动，请执行：

```
``
```

同时请确认设置的模型已下载完成：

```
``
```

## 4. 自定义端点：验证路径格式

Hyday 会自动处理 `/v1` 路径后缀，请检查 Base URL 设置：

- 若填入 `https://api.example.com`：Hyday 会自动对接至 `/v1/chat/completions`
- 若填入 `https://api.example.com/v1`：Hyday 会直接对接至 `/chat/completions`

请注意，自定义服务端必须符合 OpenAI 相容格式，否则可能无法正常运作

## 5. AI Agent 操作卡死处理

若 Agent 在执行任务时陷入死循环或停止回应：

- 点击对话窗口右上角的**停止**按钮强行中断
- 打开一段全新的对话进行测试
- 若特定指令反复导致卡死，请检查所选模型是否完整支援**工具呼叫**功能，详见 [AI 供应商对照表](/docs/reference/ai-providers)

## 6. 常见错误代码对照表

   错误代码 代表意义 建议处理方式    401API Key 错误请重新检查并贴上正确的金钥 403权限受限请检查帐号是否有权限存取该特定模型 429请求频率超限 请稍候再试，或升级帐号等级 500 / 503供应商端故障此为供应商端问题，请关注官方状态页面 Context length exceeded内容超出长度上限请减少一次传送的笔记量，或更换为具备大上下文窗口的模型  

> **ℹ️ Info**
>  若某一供应商反复失败，建议暂时切换至另一个供应商 (如从云端切换至本机 Ollama)。若切换后功能正常，则代表问题出在供应商端而非 Hyday 本身
