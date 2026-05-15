---
locale: en
category: reference
slug: frontmatter-fields
source: src/content/docs/en/reference/frontmatter-fields.tsx
---
> * Frontmatter is the YAML block at the very top of a note, used to define the note's metadata. Hyday automatically parses and applies the following fields. *

## Basic Example

```
``
```

## Standard Core Fields

   Field Type Description    `title`stringThe display title of the note. `type`stringNote type (supports `article` / `card` / `img` / `link` / `video`). `tags`string[]An array of tags; supports standard YAML lists or inline `[a, b]` syntax. `pinned`booleanWhether to pin this note to the top of the sidebar. `archived`booleanWhether the note is archived (archived notes are hidden from the main list by default). `createdAt`datetimeNote creation time (filled in by the system, formatted as `YYYY-MM-DD HH:mm:ss`). `lastModified`datetimeLast modified time (updated automatically, same format as above). `createdBy`stringCreation source (defaults to `User` for notes created manually).  

## Link and Media Source Fields

For `link` or `video` notes, when content is fetched from an external source Hyday automatically fills in the following:

   Field Type Description    `sourceUrl`stringSource URL of the original content. `sourceDomain`stringSource domain (parsed automatically). `sourceTitle`stringOriginal title of the source page. `sourceDescription`stringSummary description of the source page. `sourceImage`stringStorage path of the preview image. `sourceEmbedUrl`stringSpecial URL used for embedded display (e.g. a video embed link). `capturedAt`datetimeWhen the content was captured (formatted as `YYYY-MM-DD HH:mm:ss`).  

## Content Evolution Fields

   Field Type Description    `stage`stringThe note's evolution stage; only accepts `seed`, `sapling`, or `evergreen`. `stagePromotedAt`datetimeWhen the note entered the current stage (formatted as `YYYY-MM-DD HH:mm:ss`).  

## YAML Authoring Tips

- Frontmatter must sit at the **absolute top** of the file, wrapped by three hyphens `---` on each side.
- Arrays can use either `[a, b]` or the standard YAML list format (one tag per line, e.g. `- a`).
- If the title contains Chinese characters or special symbols, wrap it in double quotes: `title: "My Professional Notes"`.
- Booleans must be lowercase: `true` or `false`.
