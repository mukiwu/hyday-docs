---
locale: en
category: concepts
slug: plugins
source: src/content/docs/en/concepts/plugins.tsx
---
> *Plugins extend the Hyday app. They typically attach commonly used utility components, third-party integrations, or custom scripts to Hyday and work alongside your notes folder.*

## What Are Hyday Plugins?

- **Stand-alone**: A plugin can sit on Hyday's main interface or in the sidebar.
- **Controlled access**: Plugins read and write notes, query tags, or run lineage analysis through the Host API.
- **Sandboxed execution**: They run in a sandbox and can't directly touch system files.
- **Transparent permissions**: Every plugin must declare exactly what it needs when installed.

## Official Hyday Plugins

- **Sticky note**: Pins a note to the top-right corner for jotting thoughts, quick notes, todos, and other on-the-fly bits. Auto-saves, and you can promote anything to a real note or journal entry on demand.
- **Random note**: Shows a random note. Good for finding inspiration or revisiting older work.
- **Pomodoro timer**: Set focus and break intervals to lift your focus and productivity.
- More on the way…

## Plugin Marketplace

Plugins are a VVIP-only feature. After upgrading to VVIP you get access to the official plugins from the marketplace.

![Plugin marketplace](https://hyday.tw/docs/screenshots/concepts-plugins-1.png)

## Custom and Third-Party Plugins

Developers can write their own plugins in HTML and JavaScript. The full Host API definition, sandbox constraints, and development workflow will live in a dedicated**developer documentation**(work in progress, stay tuned).
