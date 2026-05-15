---
locale: en
category: reference
slug: markdown-extensions
source: src/content/docs/en/reference/markdown-extensions.tsx
---
> * Hyday is built around standard GitHub Flavored Markdown (GFM) and adds several smart markup features on top. The tables below list every syntax the system currently supports. *

## Standard Markdown Syntax

- **Headings**: from H1 (`#`) through H6 (`######`).
- **Bold**: `**bold**`.
- **Italic**: `*italic*`.
- **Lists**: unordered (`-` or `*`) and ordered (`1.`).
- **Blockquotes**: use the `>` character.
- **Code**: inline code (with backticks ````) and fenced code blocks (with `````).
- **Links and images**: standard `[text](URL)` and `![alt](path)` syntax.
- **Horizontal rule**: use `---`.

## GFM (GitHub Flavored Markdown) Extensions

- **Tables**: standard Markdown table syntax.
- **Task lists**: mark items with `- [ ]` or `- [x]`.
- **Strikethrough**: use double tildes `~~strikethrough~~`.
- **Smart autolinks**: raw URLs are automatically converted into clickable links.

## Math (KaTeX)

Math equations **must be inserted from the slash command menu** inside the editor — they are **not** triggered automatically by typing `$`:

- In the editor, type `/` to open the menu, then search for **Equation** (block formula) or **Inline Equation**.
- Once inserted, write LaTeX syntax inside the KaTeX editor box for a live preview.

When editing the `.md` file **outside the editor**, you can write the following syntax directly, and Hyday will render it with KaTeX on load:

- **Inline math**: `$E = mc^2$`
- **Block math**: wrap with double dollar signs, e.g. `$$\sum_{i=1}^n i$$`

## Mermaid Diagrams

Code blocks tagged with the `mermaid` language are rendered automatically as diagrams:

```
``
```

![Mermaid diagram](https://hyday.tw/docs/screenshots/reference-markdown-extensions-1.png)

You can adjust node spacing, level spacing, and color theme on the settings page. See `Settings → Editor → Mermaid`.

## Callouts

In the editor, type `/` to open the menu and search for **Callout** to insert one. Click the icon to switch between callout variants.

When saving, Hyday converts the callout to standard Markdown syntax.

![Callout block](https://hyday.tw/docs/screenshots/reference-markdown-extensions-2.png)

Hyday natively supports **10 callout types**: `note`, `abstract`, `important`, `reference`, `tip`, `warning`, `action`, `decision`, `question`, and `idea`.

Common Obsidian variants (such as `info`, `caution`, `danger`, `todo`, `summary`, `quote`) map automatically to the closest Hyday-native variant, so you don't need to edit anything when importing Obsidian notes.

## Hyday-Specific Extensions

   Syntax Example Purpose    `[[note title]]`Create a backlink (typing `[[` in the editor opens the note picker). `#tag`Define a tag directly in the body text. `@entity`Mark a specific person, place, or thing. `>(HH:mm)` / `<(HH:mm)` / `-(HH:mm)`LifeLog time marks (task start / task end / current). `%(content)` / `!(content)`LifeLog content marks (thought / important).  

## Syntax Not Currently Supported

- `[[note#anchor]]`: Obsidian's heading-level anchor.
- `[[note#^block-id]]`: Obsidian's block reference.
- `%%`: Obsidian's hidden comment syntax.
- **Unsafe HTML tags**: basic HTML tags (`div`, `span`, and the noted `u` / `mark` / `kbd` / `sup` / `sub`) are preserved, but tags with security risks (such as `<script>`) are stripped.

> **ℹ️ Info**
>  Even though the Hyday editor shows live formatted output, **files are always stored as plain Markdown**. If you open the `.md` file in an external text editor, you'll see the raw syntax exactly as shown above.
