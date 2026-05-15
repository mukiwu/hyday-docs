---
locale: en
category: concepts
slug: whiteboard
source: src/content/docs/en/concepts/whiteboard.tsx
---
> *The whiteboard is an infinite canvas for visual thinking. Lay out notes, sticky notes, and images freely; use connections and groups to build out three-dimensional structures of thought.*

## When to Use the Whiteboard

- **Untangle non-linear relationships**: When linear notes can't capture complex logic, causality, or hierarchy.
- **Project brainstorming**: Early in planning, put ideas and material on the canvas freely to explore and converge.
- **Visual topic roundup**: See all the information and references for a topic at a glance.
- **Structured meeting notes**: Use connections, groups, and highlights to turn scattered meeting comments into a clear consensus map.

## What Lives on the Whiteboard?

- **Sticky notes**: Quick capture for short thoughts or titles.
- **Note cards**: Embed a note from your folder directly on the canvas —**content stays in sync**, so the information is consistent.
- **Images**: Drag images straight onto the canvas for visual display.
- **Connection tool**: Draw connecting lines between elements and add labels to them.
- **Groups**: Select multiple elements and press`⌘`+`G`to group them — easy to move and organize together.

![Whiteboard view](https://hyday.tw/docs/screenshots/concepts-whiteboard-1.png)

## Whiteboard vs. Split View

- **Whiteboard**: 2D free-form layout. Best for**organizing the shape of your thinking**and building mental models.
- **Split View**: Two columns side by side. Best for**linear reading**and side-by-side editing.

## Where Whiteboards Are Saved

All whiteboards are stored together in a single JSON file at`.hyday/whiteboards-v2.json`in your notes folder (`.hyday/`is the hidden sidecar directory). That means you can version-control them, or easily copy and migrate them to another folder.

## Common Shortcuts

- `⌘`+`G`: Group the selected elements.
- `⌘`+`C`/`⌘`+`V`: Copy and paste canvas elements.
- `⌘`+`Z`: Undo the last action.
- Hold`Space`and drag with the mouse: Pan the canvas viewport.

> **ℹ️ Info**
> Note cards embedded on the whiteboard use**live references**, not plain content copies. Edit the source note and the card updates in sync — and vice versa.
