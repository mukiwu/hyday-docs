---
locale: zh-TW
category: reference
slug: supported-platforms
source: src/content/docs/zh-TW/reference/supported-platforms.tsx
---
> * Hyday 是一款基於 Electron 架構開發的桌面應用程式，下表詳細列出了目前支援的作業系統環境與硬體需求 *

## 作業系統支援表

   作業系統 支援狀態 詳細說明     macOS 12+ 主要支援 提供 Apple Silicon(arm64) 與 Intel(x64) 原生建置版本，為開發團隊主要使用平台   Windows 10 / 11 穩定支援 提供標準 NSIS 安裝程式(x64 架構)，包含數位簽署的自動更新套件   Linux 暫不支援    

## 何謂**主要支援**？

**主要支援**代表該平台是開發團隊日常工作的首選環境，因此程式錯誤 (Bug) 通常能獲得最優先修復，各項新功能也最先在該平台達到穩定。其他支援平台雖然功能完備，但在部分系統選單行為或輸入法 (IME) 整合上，反應速度可能稍慢

## 下載方式

- 所有穩定版與測試版皆發布於 [GitHub Releases 官方頁面](https://github.com/mukiwu/hyday/releases/tag/v0.6.1)
- 目前尚未於 Homebrew、Mac App Store 或 Microsoft Store 上架

## 硬體系統需求

   硬體項目 最低需求 建議配置    macOS 版本12 (Monterey)14 (Sonoma) 或更新版本 Windows 版本10 (22H2)11 隨機存取記憶體 (RAM)4 GB8 GB 或以上 磁碟剩餘空間500 MB1 GB 以上 (視筆記與附件量而定)  

> **ℹ️ Info**
>  若打算使用**本機 Ollama** 執行 AI 功能，建議硬體配置應進一步提升 (跑 7B 等級模型建議具備 16 GB 以上 RAM，13B 以上模型則建議 32 GB 以上)若使用雲端 AI Provider，則維持一般桌面操作效能即可
