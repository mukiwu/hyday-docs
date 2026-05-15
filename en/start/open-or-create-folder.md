---
locale: en
category: start
slug: open-or-create-folder
source: src/content/docs/en/start/open-or-create-folder.tsx
---
> * Hyday treats an entire folder as your personal note space. *

## Open an Existing Folder

You can open any folder that already contains Markdown files. Hyday automatically:

- Reads every `.md` file in the folder and sorts them by modification time by default
- Parses Markdown frontmatter (such as `title`, `type`, `tags`, etc.)
- Recognizes files under `journal/year/` named `YYYY-MM-DD.md` as journal entries

## Create a New Folder

Pick a suitable location on your computer (we recommend `~/Documents/Hyday`). When Hyday creates a new folder, it:

- Doesn't drop any proprietary config files in the folder, aside from the `.hyday/` index cache (which we recommend adding to `.gitignore`). The folder stays clean.
- Saves every note as standard, plain Markdown — you can open them anytime with any text editor.

> **ℹ️ Info**
>  Just run `git init` at the folder's root and exclude the `.hyday/` folder (add it to `.gitignore`). That's all you need.
