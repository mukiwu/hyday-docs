---
locale: en
category: concepts
slug: journal
source: src/content/docs/en/concepts/journal.tsx
---
> * Journal entries are records at the **day** level. Hyday recommends pairing them with LifeLog time marks so daily life, meetings, todos, and flashes of inspiration all live on a single clear timeline. *

## Automatic Recognition

Any file whose name matches one of the following patterns is automatically treated as a journal entry:

- `YYYY-MM-DD.md` (for example `2026-05-09.md`)
- `YYYY.MM.DD.md` (for example `2026.05.09.md`)
- Click the "Journal" menu in the sidebar and Hyday creates today's journal file for you — no manual setup needed.

## How a Journal Entry Is Built: Blocks

In Hyday, what you see in the editor isn't one big stream of text — it's a sequence of **blocks**. Each block can be a different content type:

- A paragraph of plain text.
- A LifeLog time mark (task, thought, important note).
- An image or attachment.
- A callout, blockquote, or code block.
- A task list item.

![Journal view: a day made up of several different block types](https://hyday.tw/docs/screenshots/concepts-journal-1.png)

## Reading Across Dates

Open two days side by side using **Split View**. It's especially handy when writing weekly recaps or doing monthly reviews.

![Split View: panels displayed side by side](https://hyday.tw/docs/screenshots/concepts-journal-2.png)

## Why **One File per Day**?

Keeping each day as its own Markdown file has real upsides:

- **Easy to search**: Tools like `grep` can pinpoint exactly what you're looking for.
- **Clean version control**: Git diffs clearly show each day's changes.
- **Safer data**: If one file gets corrupted, the others are untouched.
- **Compatible**: External scripts can easily automate work against a specific day's file.

> **ℹ️ Info**
>  Journal files are standard Markdown. Edit them in whatever editor you love — Hyday picks up the changes on next launch. 

## Further Reading

- [LifeLog Time Marks](https://hyday.tw/docs/concepts/lifelog-marks): Turn your journal into a timeline you can actually analyze.
- [Write a Journal Entry](https://hyday.tw/docs/guides/create-journal-entry): A step-by-step walkthrough.
