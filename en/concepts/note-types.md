---
locale: en
category: concepts
slug: note-types
source: src/content/docs/en/concepts/note-types.tsx
---
> * Every note has a **type**. The type decides how it's presented in the list and what the default template looks like. Hyday ships with six built-in types. *

## Six Built-In Types

   Type Primary Use Typical Content     `article` Long-form articles and notes Idea processing, long-form notes, meeting or discussion records   `card` Short cards Excerpts, snippets of inspiration, quotes   `img` Images and visual records Screenshots, design inspiration, visual collections   `link` URLs and bookmarks Web article links, reference bookmarks   `video` Video notes YouTube learning notes, podcast takeaways   `journal` Journal entries Daily life entries — recognized automatically by filename   

## How to Set a Note's Type

You have three options:

- When creating a new article, paste an image, link, or video URL directly — Hyday detects the type automatically.
- When creating a new article, pick a type from the dropdown. Hyday writes the type into frontmatter for you.
- Edit the type directly inside the article.

![Note type settings](https://hyday.tw/docs/screenshots/concepts-note-types-2.png)

![Note type settings](https://hyday.tw/docs/screenshots/concepts-note-types-1.png)

## How the Type Affects Functionality

**The note type doesn't change the core features**. Every type supports tags, backlinks, and being referenced by AI Agent. The type mainly affects **visual presentation**: `img` shows a thumbnail first in the list, while `link` displays the source domain and a preview.

![Visual differences across note types](https://hyday.tw/docs/screenshots/concepts-note-types-3.png)

> **ℹ️ Info**
>  The `journal` type is recognized by filename format (such as `YYYY-MM-DD.md`), so you don't need to write `type: journal` into frontmatter manually. 

## Further Reading

- [Note Types Reference](https://hyday.tw/docs/reference/note-types): Detection rules and frontmatter examples for each type.
