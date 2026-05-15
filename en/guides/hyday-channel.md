---
locale: en
category: guides
slug: hyday-channel
source: src/content/docs/en/guides/hyday-channel.tsx
---
> *Hyday Channel turns Claude Code into a real-time collaborator sitting next to Hyday. Two-way communication lets Claude Code see what you're reading, writing, or pausing on — and interact with you through Hyday's Buddy.*

## Why You'd Want Channel

A typical AI Agent is one-way: it waits for you to ask. Hyday Channel is**two-way**, which means Claude Code sees your reading and writing activity inside notes in real time, and can proactively chime in with observations, reminders, or options for what to do next.

For example:

- You read the same note for 30 seconds — Claude Code surfaces related past notes
- You stop typing mid-sentence for 15 seconds — Claude Code might ask, "Want me to continue from here?"
- You're tackling a tricky topic — Claude Code uses Buddy's memory to remind you how you handled similar situations before

## How It Works

Channel connects to Claude Code via**Hyday MCP (`@mukiwu/hyday-channel`)**. The MCP server is launched by Claude Code as a child process and opens a lightweight HTTP server locally (default port`8789`). Hyday POSTs events to it; Claude Code replies through MCP's reply tool. The entire conversation stays on your machine —**no cloud relay is involved**.

- **Hyday → Claude Code**: real-time push of reading, writing, and message events
- **Claude Code → Hyday**: responses appear in Buddy's chat bubble and can include widgets

> **ℹ️ Info**
> Locally: Claude Code CLI (v2.1.80 or later) installed and signed in, plus Bun or Node.js 18+. On the Hyday side, hatch a Buddy first (on the Hyday Agent page), since Channel's chat window is anchored to the Buddy.

## 1. Install Hyday MCP

In the root of your Hyday notes folder, create an`.mcp.json`file with this content:

```
``
```

With Hyday MCP, Claude Code can:

- **Receive events pushed from Hyday in real time**: which note you're reading, how long you've stayed, the paragraph you're writing, and any messages you send
- **Reply into the Buddy chat bubble**: through the built-in`reply`tool, displaying replies (with markdown, lists, tables, code blocks) at the bottom-right of Hyday
- **Read and write your notes folder**: because Claude Code`cd`s into the notes folder on launch, it can read, search, create, and edit markdown files directly (via Claude Code's built-in file tools)
- **Run deep tasks over your notes**: summarize topics, surface forgotten connections, produce summaries, and offer insights on what you're currently reading

On first launch the MCP server generates a`CLAUDE.md`describing the notes folder structure, so Claude doesn't have to re-explore the directory every time.

## 2. Launch Claude Code

Switch to the notes folder that holds the`.mcp.json`file and launch Claude Code:

```
``
```

The Buddy icon in Hyday's sidebar switches from "Not connected" to "Connected", and updates with Claude Code's current state —**Reading**,**Writing**,**Thinking**, and so on.

![Hyday sidebar showing Channel connected with a Buddy chat bubble](https://hyday.tw/docs/screenshots/guides-hyday-channel-1.png)

## 3. Chat with Claude Code

Press**Cmd + Shift + B**to toggle the Channel chat bubble, or click**Hyday Channel**on the right to open the full page. In the bubble you can:

- Send text or upload images to Claude Code
- See observations, widgets, and suggested next steps that Claude Code surfaces on its own

## 4. Privacy Event Toggles

Not every action needs to be pushed to Claude Code. Under**Settings → AI → Channel**, toggle each event type individually:

- **Note reading**: read events fired after you stay on the same note for 30 seconds or more
- **Journal reading**: read events fired on the journal page
- **Writing activity**: write events fired 15 seconds after you stop typing (includes the diff for the current paragraph)
- **Chat messages**: messages you send actively

## 5. How Channel Differs from Hyday Agent

Hyday AgentHyday ChannelModeYou ask, it answersTwo-way — AI can initiateBackendAPI / CLI / Ollama, any of themClaude Code (only)AwarenessSees only the prompt you sendReceives read/write activity in real timeBest forConcrete tasks, running skillsLong companionship, live suggestions

> **ℹ️ Info**
> Hyday Agent and Channel are independent pipes. You can run Agent on a focused task while Channel watches your reading and writing in the background — they don't get in each other's way.

## FAQ

### Why only Claude Code?

Channel needs the CLI to**actively push messages back**through MCP and to understand Hyday's event schema. So far only Claude Code's development-channels mode implements this. Support for other CLIs isn't off the table for the future.

### What if the connection drops?

When Claude Code exits or crashes, Hyday's sidebar shows "Channel disconnected" with a "Re-detect" button. The Channel service also retries every 30 seconds automatically —**no need to restart Hyday**.

### Where are conversations stored?

Channel conversations currently live in memory and clear when Hyday restarts — a design trade-off that preserves Channel's "live conversation" feel. Buddy's long-term memory, on the other hand, is written to`.hyday/observations/`through the reflection flow, so important observations aren't lost.

## Further Reading

- [Hyday Agent](https://hyday.tw/docs/guides/use-ai-agent): the full picture of Agent, skills, widgets, and Buddy
- [Configure AI Providers](https://hyday.tw/docs/guides/configure-ai-provider): setup and overview of each AI provider
