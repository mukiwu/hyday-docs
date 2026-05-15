---
locale: en
category: reference
slug: supported-platforms
source: src/content/docs/en/reference/supported-platforms.tsx
---
> * Hyday is a desktop application built on Electron. The tables below list the supported operating systems and hardware requirements. *

## Operating System Support

   OS Support Status Notes     macOS 12+ Primary support Native builds for Apple Silicon (arm64) and Intel (x64). The primary platform used by the development team.   Windows 10 / 11 Stable support Standard NSIS installer (x64), with a digitally signed auto-update bundle.   Linux Not currently supported    

## What Does **Primary Support** Mean?

**Primary support** means this platform is the development team's day-to-day environment of choice. Bugs are usually fixed first here, and new features reach stability on this platform first. Other supported platforms are fully functional, but a few system menu behaviors or IME integrations may feel slightly less responsive.

## How to Download

- All stable and beta releases are published on the [official GitHub Releases page](https://github.com/mukiwu/hyday/releases/tag/v0.6.1).
- Hyday is not yet available on Homebrew, the Mac App Store, or the Microsoft Store.

## Hardware Requirements

   Component Minimum Recommended    macOS version12 (Monterey)14 (Sonoma) or later Windows version10 (22H2)11 RAM4 GB8 GB or more Free disk space500 MB1 GB or more (depending on notes and attachments)  

> **ℹ️ Info**
>  If you plan to run AI features with **local Ollama**, increase the hardware spec further (16 GB or more RAM is recommended for 7B-class models; 32 GB or more for 13B-class models).For cloud AI providers, standard desktop performance is sufficient.
