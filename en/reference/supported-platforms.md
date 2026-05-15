---
locale: en
category: reference
slug: supported-platforms
source: src/content/docs/en/reference/supported-platforms.tsx
---
> *Hyday is a desktop application built on Electron. The tables below list the supported operating systems and hardware requirements.*

## Operating System Support

OSSupport StatusNotesmacOS 12+Primary supportNative builds for Apple Silicon (arm64) and Intel (x64). The primary platform used by the development team.Windows 10 / 11Stable supportStandard NSIS installer (x64), with a digitally signed auto-update bundle.LinuxNot currently supported

## What Does**Primary Support**Mean?

**Primary support**means this platform is the development team's day-to-day environment of choice. Bugs are usually fixed first here, and new features reach stability on this platform first. Other supported platforms are fully functional, but a few system menu behaviors or IME integrations may feel slightly less responsive.

## How to Download

- All stable and beta releases are published on the[official GitHub Releases page](https://github.com/mukiwu/hyday/releases/tag/v0.6.1).
- Hyday is not yet available on Homebrew, the Mac App Store, or the Microsoft Store.

## Hardware Requirements

ComponentMinimumRecommendedmacOS version12 (Monterey)14 (Sonoma) or laterWindows version10 (22H2)11RAM4 GB8 GB or moreFree disk space500 MB1 GB or more (depending on notes and attachments)

> **ℹ️ Info**
> If you plan to run AI features with**local Ollama**, increase the hardware spec further (16 GB or more RAM is recommended for 7B-class models; 32 GB or more for 13B-class models).For cloud AI providers, standard desktop performance is sufficient.
