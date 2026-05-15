---
locale: zh-CN
category: reference
slug: supported-platforms
source: src/content/docs/zh-CN/reference/supported-platforms.tsx
---
> * Hyday 是一款基于 Electron 架构开发的桌面应用程序，下表详细列出了目前支援的作业系统环境与硬件需求 *

## 作业系统支援表

   作业系统 支援状态 详细说明     macOS 12+ 主要支援 提供 Apple Silicon(arm64) 与 Intel(x64) 原生建置版本，为开发团队主要使用平台   Windows 10 / 11 稳定支援 提供标准 NSIS 安装程序(x64 架构)，包含数位签署的自动更新套件   Linux 暂不支援    

## 何谓**主要支援**？

**主要支援**代表该平台是开发团队日常工作的首选环境，因此程序错误 (Bug) 通常能获得最优先修复，各项新功能也最先在该平台达到稳定。其他支援平台虽然功能完备，但在部分系统菜单行为或输入法 (IME) 整合上，反应速度可能稍慢

## 下载方式

- 所有稳定版与测试版皆发布于 [GitHub Releases 官方页面](https://github.com/mukiwu/hyday/releases/tag/v0.6.1)
- 目前尚未于 Homebrew、Mac App Store 或 Microsoft Store 上架

## 硬件系统需求

   硬件项目 最低需求 建议配置    macOS 版本12 (Monterey)14 (Sonoma) 或更新版本 Windows 版本10 (22H2)11 随机存取记忆体 (RAM)4 GB8 GB 或以上 磁碟剩余空间500 MB1 GB 以上 (视笔记与附件量而定)  

> **ℹ️ Info**
>  若打算使用**本机 Ollama** 执行 AI 功能，建议硬件配置应进一步提升 (跑 7B 等级模型建议具备 16 GB 以上 RAM，13B 以上模型则建议 32 GB 以上)若使用云端 AI Provider，则维持一般桌面操作效能即可
