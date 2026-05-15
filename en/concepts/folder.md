---
locale: en
category: concepts
slug: folder
source: src/content/docs/en/concepts/folder.tsx
---
> *The folder is the core storage unit of Hyday. All notes, journal entries, and settings live inside this folder. It's highly portable, works with version control, and can be opened by any standard Markdown editor.*

## Why a Folder-Based Storage Model?

- **Local-first**: Everything you write lives on your own computer, not on our servers. Your data stays private.
- **Portable**: Markdown files with frontmatter metadata can be read and converted by any modern editor.
- **Version control friendly**: Run`git init`in the folder root and treat your entire library as a Git repository.
- **No vendor lock-in**: Even if you stop using Hyday, your notes keep their original structure and content. Migrate freely.

## Folder Structure at a Glance

```
``
```

- **Note files**: Standard`.md`files. Place them in the root or any subfolder.
- **Journal files**: Files at`journal/<year>/`with names like`YYYY-MM-DD.md`are recognized as journal entries and added to the journal timeline. Hyday creates this structure by default.
- **Media and attachments**: Images and attachments inserted into notes go into the`assets/`folder by default.
- **.hyday/ folder**: Holds the search index and tag statistics cache. If it's lost, Hyday will rebuild it automatically.

## Single Folder vs. Multiple Folders

- **Single folder**: Good for keeping everything in one place so ideas across domains can interlink freely.
- **Multiple folders**: Good for cleanly separating work, personal life, writing, and so on. Switching folders also helps you switch mental contexts.

Either approach works depending on your workflow. Note that Hyday can only open and operate on one folder at a time.

> **ℹ️ Info**
> Yes. Just create your Hyday folder inside iCloud Drive, Dropbox, or Google Drive's sync path. Avoid editing the same file simultaneously on multiple devices to prevent sync conflicts.
