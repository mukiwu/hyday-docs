---
locale: en
category: guides
slug: organize-on-whiteboard
source: src/content/docs/en/guides/organize-on-whiteboard.tsx
---
> * The whiteboard is Hyday's visual thinking canvas. This guide walks you from creating your first whiteboard to placing notes, drawing connections, grouping things, and finally turning scattered ideas into a coherent structure. *

## 1. Open the Whiteboard and Create a New Canvas

Click **Whiteboard** in the sidebar. The whiteboard list sits on the left and the canvas on the right. Click **New whiteboard** at the top of the list to create a blank canvas, and rename it right away to make it easier to find later.

## 2. Drop in Your First Element

The whiteboard supports three main element types. Pick the one that fits the shape of your idea:

- **Sticky note**: right-click an empty area of the canvas and choose Sticky note. Good for jotting down a keyword, a to-do, or a conclusion.
- **Note card**: browse the **library**, search for an existing note, and **drag it onto the canvas**. Cards are **live references** — editing card content writes back to the original note.
- **Image**: drag any local image onto the canvas. It appears as an image node.

> **ℹ️ Info**
>  Sticky notes are good for **fresh, in-the-moment** ideas whose content lives only on the whiteboard. Note cards are good for referencing **settled** content — they stay in sync with your notes folder both ways. Start with sticky notes for divergent thinking, then promote them to real notes once organized. 

## 3. Draw Connections

Hover the edge of a node and a **connector handle** appears. Drag from the handle to another node to create a connection. You can fine-tune each connection further:

- Right-click the connection to **edit the label** — for example "leads to", "counterexample", "extends from"
- Toggle **one-way / two-way arrows** to express causality or mutual influence
- Pick a **line style** (curved, straight, orthogonal, rounded orthogonal) and **color** to visually differentiate relationships

## 4. Converge with Groups

As the canvas fills up, select nodes that belong to the same topic and press `⌘`+`G` to create a **group**. Groups let you:

- Move everything together instead of one node at a time
- Set a group color so different topics stand apart visually
- Right-click the group to rename, recolor, or ungroup

## 5. Align and Lay Out

Select multiple nodes and right-click to use **Align** and **Distribute**:

- **Align**: left, right, top, bottom, horizontal center, vertical center
- **Distribute**: equal horizontal spacing, equal vertical spacing — clean up the layout

The bottom-right of the canvas has **zoom controls**. Hold `Space` and drag the mouse to pan the canvas.

## Useful Shortcuts

- `⌘`+`G`: create a group
- `⌘`+`C` / `⌘`+`V`: copy / paste nodes
- `⌘`+`Z` / `⌘`+`⇧`+`Z`: undo / redo
- `Delete`: delete the selected nodes or connections
- Hold `Space` and drag: pan the canvas

> **ℹ️ Info**
>  All whiteboards share a single `.hyday/whiteboards-v2.json` file alongside your notes folder. It travels with the folder for backup or version control. See [Whiteboard concept](https://hyday.tw/docs/concepts/whiteboard) for details. 

## Further Reading

- [Visual Whiteboard](https://hyday.tw/docs/concepts/whiteboard): design rationale and storage mechanics
- [Split View](https://hyday.tw/docs/concepts/split-view): an alternative better suited to linear reading and side-by-side editing
