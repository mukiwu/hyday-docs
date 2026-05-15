---
locale: zh-CN
category: concepts
slug: local-first
source: src/content/docs/zh-CN/concepts/local-first.tsx
---
> * Hyday 的核心原则是**笔记永远储存在使用者自己的电脑**，而非官方伺服器。云端功能仅用于同步少部分的个人设置，绝不储存使用者的文件。 *

## 哪些资料会储存在本机？

- **所有的笔记内容** (`.md`)
- **所有的日记内容** (`journal/年份/YYYY-MM-DD.md`)
- **白板与 Hyday Agent 对话历史** (`.hyday/`)
- **搜索索引与缓存** (`.hyday/`)

这些文件即是文件夹内可见的所有内容。即使解除安装 Hyday，这些资料依然会完整保留，并可随时透过任何 Markdown 编辑器打开

- **应用程序偏好设置**：过滤器、钉选清单、AI Provider 设置...等，存放于系统的 app 文件夹   - macOS `~/Library/Application Support/Hyday/preferences.json`
  - Windows `%APPDATA%/Hyday/preferences.json` 

## 哪些资料会同步至云端？(选用功能)

登录帐号后，Hyday 会将**跟软件有关的设置信息**同步至云端数据库 (Firestore)：

- **首页卡片宽度与位置**：确保在不同装置间拥有一致的界面布局
- **电子报订阅偏好**：纪录订阅选择
- **编辑器的设置**：拼字检查与图片宽度设置
- **VVIP 订阅状态**：用于验证进阶功能的使用权限

登录后会自动同步，退出登录后会自动清空云端设置。此外也可选择不登录(完全离线) 使用 Hyday，不影响任何笔记功能

## 关于 AI 功能的资料处理

当使用 AI 相关功能 (包括但不限于 Hyday Agent、Hyday Channel、人格蒸馏或脉络分析) 时，相关内容将会传送至所选择的 AI 服务供应商，处理方式依各供应商的隐私政策而定：

- **云端供应商** (如 OpenAI、Claude、Gemini、OpenRouter)：依据该公司的资料隐私政策处理
- **本机供应商** (如 Ollama)：资料处理完全在电脑上进行，不会传送到外部网络
- **CLI 供应商** (Claude Code、Gemini CLI、Codex)：依据该工具的运作机制进行处理

建议在处理极其敏感的内容时，优先考虑使用本机 AI 模型。

> **ℹ️ Info**
>  可以将供应商设置为本机端的 Ollama，并下载合适的模型。如此一来，撰写笔记、AI 分析与 Agent 操作都能在完全不连网的情况下在本机执行。 

## 离线状态下可以使用吗？

除了帐号登录验证与云端 AI 功能外，**Hyday 的绝大部分功能皆支援离线使用**。撰写笔记、管理日记、探索标签、操作白板或使用本机 AI，皆无须连网即可流畅运作

## 延伸阅读

- [隐私与数据存储政策](https://hyday.tw/docs/reference/privacy)：深入了解完整的资料流向细节
