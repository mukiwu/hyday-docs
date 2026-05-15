---
locale: en
category: troubleshooting
slug: editor-stuck
source: src/content/docs/en/troubleshooting/editor-stuck.tsx
---
> * If the editor stops responding, input feels laggy, or you see a long-running loading skeleton when switching notes, use the suggestions below to diagnose and improve performance. *

## 1. The Loading State Lingers When Switching Notes

Briefly seeing a skeleton while you flip through notes is normal — the system is parsing Markdown in the background. If the loading state never goes away:

- **Check the file size**: a single note over 100 KB takes noticeably longer to parse
- **Check the Console**: open DevTools and look for interrupted script execution

## 2. The Editor Is Completely Frozen

If you can't type and the UI is unresponsive, try the following in order:

1. Close the current tab and reopen it
2. If the problem persists, fully restart the Hyday app

## 3. Content Shifts or Indentation Looks Wrong

If **saved content looks different from what you wrote** (especially with complex nested lists):

- Press `⌘`+`Z` to undo back to the previous state

## 4. Performance Bottlenecks With Huge Files

When a single note exceeds 1 MB, the editing experience degrades noticeably. Suggested optimizations:

- **Split atomically**: break overly long articles into smaller sub-notes and connect them via `[[]]` backlinks
- **Slim down journal entries**: extract long-form topics out of a journal entry into standalone notes and keep only links in the journal entry

## 5. Heavy Syntax Highlighting in Code Blocks

Code blocks containing more than 500 lines consume significant resources for syntax highlighting. What to do:

- Split the code into several shorter blocks
- For plain text that doesn't need syntax highlighting, use a regular paragraph instead of a code block

> **ℹ️ Info**
>  Editor stability directly affects your writing experience. If you ever lose data or content gets modified unexpectedly, **report it to us immediately** with reproduction steps, the time it happened, the file size, and your Hyday version. The team prioritizes these issues.
