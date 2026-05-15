---
locale: en
category: reference
slug: file-structure
source: src/content/docs/en/reference/file-structure.tsx
---
> *This guide explains the internal file layout of a Hyday notes folder and what each file is for.*

## A Typical Folder Layout

```
``
```

## Primary Content Files (Directly Editable)

ExtensionPurpose`.md`The core format for notes and journal entries — plain Markdown with YAML frontmatter.`.hyday/whiteboards-v2.json`A single centralized JSON file holding all visual whiteboards.`.hyday/agent-conversations/v1.json`A single centralized JSON file holding all AI conversation history, with full context preserved.

## The Index System

To deliver fast search and statistics, Hyday builds shadow index files inside the`.hyday/`folder:

- **notes-index/v1**: Stores titles, first-paragraph snippets, and metadata snapshots to speed up list rendering.
- **tag-stats.json**: Tracks tag occurrence counts and relationship statistics.
- **lineage-cache.json**: Caches lineage analysis results to avoid repeating AI calls.

These files are**fully rebuildable**: if you delete the`.hyday/`folder and restart the app, Hyday will scan your entire notes folder and rebuild the index automatically.

## Version Control Tips (.gitignore)

The`.hyday/`directory contains two kinds of files: whiteboards and AI conversations are**real user content**(worth tracking in version control), while the rest are**rebuildable derived caches**(best excluded). A reference`.gitignore`setup:

```
``
```

This pattern says "ignore everything at the top level of`.hyday/`, then un-ignore the whiteboards and AI conversations." Newly added index files default to being ignored; if you later want to preserve another file, just add another`!.hyday/...`line.

## System Preferences Files

Hyday's global settings (UI theme, filter combinations, AI backend choice, and so on)**are not stored in the notes folder**. They live in two files under your OS's application support path:

- `settings.json`: System-level settings such as folder paths.
- `preferences.json`: UI and feature preferences.

Actual locations:

- **macOS**:`~/Library/Application Support/Hyday/`
- **Windows**:`%APPDATA%\Hyday\`

> **ℹ️ Info**
> Once you sign in to Hyday, 27 settings — including UI theme, interface language, filter combinations, AI backend choice, lineage weights, and Tasks / Journal view preferences — sync automatically to the cloud and apply on any new device after sign-in.You can still sync`settings.json`/`preferences.json`manually (for example, by placing them in iCloud and using a symlink), which works well for users who prefer not to sign in but still want cross-machine settings.

## Performance with Large Note Libraries

- **Under 1,000 notes**: smooth experience, no search lag.
- **1,000 to 10,000 notes**: the first indexing scan is slower, but daily use stays snappy once it's done.
- **More than 10,000 notes**: for file system performance reasons, consider splitting your notes into multiple independent Hyday folders.
