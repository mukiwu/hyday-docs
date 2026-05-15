---
locale: en
category: concepts
slug: backlinks
source: src/content/docs/en/concepts/backlinks.tsx
---
> *Backlinks let notes reference each other. Create a link in one note and the connection appears on both sides automatically.*

## How Do You Create a Link?

Type`[['`in the editor and Hyday opens a note picker. Pick an existing note or type to search:

```
`This idea ties closely to [[2025-04 Spring Plan]]`
```

## The Value of**Bidirectional**Links

When**Note A**includes`[[Note B]]`, opening**Note B**shows**Note A links to this note**in the right-side panel.**You don't have to manually link both ways**— Hyday maintains the relationship for you.

![Backlinks panel on the right side of a note](https://hyday.tw/docs/screenshots/concepts-backlinks-1.png)

## Linking to a Journal Entry

Besides regular notes, you can link straight to a journal entry on a specific date:

```
`This decision was later revised in the [[2026-05-09]] entry`
```

> **⚠️ Warning**
> Hyday currently supports links at the level of an**entire note**or a**single journal entry**. Obsidian-style block-level anchors (such as`[[2026-05-09#10:30]]`) are not supported yet.

## What Happens If I Rename a File?

If you manually rename a note's file, every`[[]]`reference that points to it updates automatically.

## Finding**Orphan Notes**

From Settings → Manage library, you can see notes that no other note references. It's a handy view for tidying up your library and rebuilding connections.
