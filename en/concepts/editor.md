---
locale: en
category: concepts
slug: editor
source: src/content/docs/en/concepts/editor.tsx
---
> * The Hyday editor combines the convenience of **WYSIWYG** with the stability of plain Markdown files. The typing experience is as smooth as any modern notes app, while your data always stays in standard Markdown. *

## WYSIWYG Editing

Whether you're typing a heading, bold text, a list, or a code block, the editor renders it instantly. You don't have to stare at raw Markdown like `**bold**` — just focus on the writing.

## Supported Markdown Syntax

- **Standard Markdown**: Headings, lists, blockquotes, and code blocks.
- **GitHub Flavored Markdown (GFM)**: Tables, task lists, and strikethrough.
- **Math formulas**: Write `$\LaTeX$` formulas.
- **Callouts**: Obsidian-style callout syntax (such as `> [!note]` or `> [!warning]`).

## Hyday-Specific Extensions

- [LifeLog marks](https://hyday.tw/docs/concepts/lifelog-marks): Our timeline-and-thought marking syntax.
- [Backlinks](https://hyday.tw/docs/concepts/backlinks): Type `[[` to quickly reference another note.
- [Tag system](https://hyday.tw/docs/concepts/tags): Type `#` to categorize content by topic.
- [Entity tagging](https://hyday.tw/docs/concepts/entities): Type `@` to link a specific person, place, or thing.

## Slash Commands

Type `/` in the editor to open the command menu and quickly insert any block:

- Headings at any level (H1 / H2 / H3).
- List types (bulleted, numbered, task list).
- Blockquotes, code blocks, or callouts.
- Tables, dividers, image uploads, or YouTube embeds.

![Slash command menu](https://hyday.tw/docs/screenshots/concepts-editor-1.png)

## Keyboard-First Operation

The editor ships with keyboard shortcuts for everything you use often:

- `⌘`+`B` for bold, `⌘`+`I` for italic, `⌘`+`U` for underline.
- `⌘`+`⇧`+`X` for strikethrough, `⌘`+`⇧`+`H` for highlight.
- `⌘`+`E` for inline code, `⌘`+`↵` to break out of a code block.

See the [full keyboard shortcut list](https://hyday.tw/docs/reference/keyboard-shortcuts) for more.

> **ℹ️ Info**
>  Every styled block you see in the editor is saved to disk as standard plain text, keeping your data readable for the long haul.
