---
locale: en
category: reference
slug: agent-tools
source: src/content/docs/en/reference/agent-tools.tsx
---
> * This document lists all the tools that the Hyday Agent can call. To ensure data safety, tools are split into **read** and **write** categories, with a strict permission verification flow. *

## Data Read Tools

   Tool Name Description    `read_note`Read the content of a specific note `read_journal`Read the journal entry for a specific date `list_notes`List notes that match the given filter criteria `search`Run a full-text search across the entire folder `tag_usage`Look up tag usage frequency and related statistics `entity_usage`Look up entity frequency and relationships `get_lineage`Retrieve lineage analysis data for a specific topic  

## Data Write Tools

   Tool Name Description    `create_note`Create a brand new note file `update_note`Modify the body or frontmatter of an existing note `append_to_journal`Append information to today's journal entry `add_tags`Bulk add tags to a specific note `archive_note`Move a note that's no longer in use to the archive  

## Analysis and Processing Tools

   Tool Name Description    `scan_tasks`Scan and aggregate to-dos from the specified content  

## UI and Visualization Tools

   Tool Name Description    `render_widget`Render interactive components in the conversation window (e.g. charts, option comparisons, or visualized statistics)
