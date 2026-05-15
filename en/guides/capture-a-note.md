---
locale: en
category: guides
slug: capture-a-note
source: src/content/docs/en/guides/capture-a-note.tsx
---
> * This guide walks through the full flow of creating your first note. *

## 1. Create a New Note

Press `⌘`+`N`, or click "New note" in the note overview to open a blank note.

## 2. Set the Title and Frontmatter

A blank note defaults to the title **Untitled note**. Change it to something meaningful.

**Frontmatter** is a small code block at the top of every note that stores its **metadata**. Here's the basic structure:

```
``
```

Field reference:

- `title`: the note's title
- `type`: the note type — one of `article`, `card`, `img`, `link`, `video`
- `stage`: maturity stage — `seed`, `sapling`, or `evergreen`. Omit the field if you haven't decided.
- `tags`: a tag list, written in YAML array syntax
- `pinned`: whether to pin the note to the top of the list

Other fields (such as `createdAt` and `lastModified`) are managed by Hyday automatically — don't edit them by hand.

![frontmatter](https://hyday.tw/docs/screenshots/capture-a-note-1.png)

## 3. Write the Content

Just start typing. When you need formatting, there are a few options:

- **Markdown syntax**: use standard syntax like `**bold**`, `*italic*`, or `## Heading 2`
- **Slash commands**: type `/` to open the command menu and quickly insert lists, quotes, code blocks, or tables
- **System shortcuts**: press `⌘`+`B` for bold or `⌘`+`I` for italic

## 4. Link to Other Notes

Type `[[` to search for the note you want to link, then press Enter to create a backlink.

## 5. No Need to Save Manually

Hyday auto-saves in real time. You can leave or quit the app at any time — every change is already on your local disk.

> **ℹ️ Info**
>  Try writing one titled **Why I want to try Hyday**. List what you expect from a note-taking tool, what frustrates you about your current setup, and the topics you want to track. Revisit it in six months and you'll see how your needs really evolve.
