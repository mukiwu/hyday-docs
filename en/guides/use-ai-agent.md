---
locale: en
category: guides
slug: use-ai-agent
source: src/content/docs/en/guides/use-ai-agent.tsx
---
> *Hyday Agent reads and writes your notes, runs skills, responds with interactive widgets, and accumulates long-term memory through Buddy — so AI becomes**a collaborator that knows you**instead of a stranger you have to brief every time.*

## 1. Open Hyday Agent

Click**Hyday Agent**in the sidebar to open the chat page.

![Hyday Agent main screen: conversation history on the left, message stream in the middle, mode toggle in the top right](https://hyday.tw/docs/screenshots/guides-use-ai-agent-1.png)

## 2. Widgets — Interactive Responses

Hyday Agent doesn't just reply in plain text. Depending on the task, it calls the**render_widget**tool to embed interactive cards in the conversation. Supported widget types today:

- **note-list**: filter results shown as a clickable note list — click to jump straight in
- **summary-card**: a segmented summary, perfect for daily wrap-ups or health-check reports
- **tag-cloud**: a tag cloud showing frequency distribution with color coding
- **health-report**: a notes folder health report listing issues grouped by severity
- **connection-map**: hidden connections between two notes, with "bridge concept" explanations
- **action-buttons**: suggested next steps — click to navigate, apply tags, create a note, or send a follow-up prompt
- **option-compare**: a "pick one of two" decision card with side-by-side options

The Agent picks widgets on its own. You don't need to specify a type in the prompt — the AI chooses the right format for the task.

## 3. Skills — One-Click Preset Tasks

Skills are pre-written workflows for common tasks, grouped into a few categories:

- **Built-in skills**: today's note summary, find hidden connections between notes, notes folder health check, compose cards into an article, organize notes onto a whiteboard
- **User skills**: your own personalized tasks, up to 50 of them. Edit / duplicate / export / delete anytime.
- **CLI skills**: when the backend is a CLI subscription like Claude Code or Gemini CLI, the CLI's own skills are also listed
- **MCP**: external tools connected via the MCP protocol

Click the**Skills button at the top of Hyday Agent**to manage skills in one place — reorder, disable, or export to share with others.

## 4. Buddy — Long-Term Memory and Personality

Hyday raises a**Buddy**alongside the Agent. It's the Agent's memory layer. As you interact with the Agent, Buddy**reflects periodically**and writes long-term observations about you into four files:

- **Communication style**: your habitual tone, response rhythm, and whether you prefer concise or detailed answers
- **Preferences**: topics you care about, things you dislike, principles you hold
- **Recurring topics**: subjects you think about, track, or wrestle with repeatedly
- **Recent context**: what you're working on lately and where you're stuck

Each Agent response injects these observations as background, so the more you converse,**the better the Agent knows you**— no need to re-explain who you are or what you're doing every time.

> **ℹ️ Info**
> Every Buddy observation lives under`.hyday/observations/`in your notes folder as plain markdown. Open them anytime to see how Buddy understands you, and edit by hand if something looks off.

## 5. Where Conversations Are Stored

All Agent conversations live in`.hyday/agent-conversations/v1.json`in your notes folder, so they travel with the folder for backup or version control.

## Common Use Cases

- **Knowledge organization**: take product-design-related content from the #inspiration tag and shape it into an article draft
- **Lineage tracking**: list every passage from the last 30 days that mentions @deep-work
- **Notes folder maintenance**: create a note with type card, title X, and content Y
- **Deep analysis**: run a lineage evolution analysis on the #wellbeing tag

## Further Reading

- [Agent Tools Reference](https://hyday.tw/docs/reference/agent-tools): full list of tools and permissions
- [Hyday Channel](https://hyday.tw/docs/guides/hyday-channel): hook up Claude Code as a real-time collaborator
- [Troubleshooting: Tool Call Failed](https://hyday.tw/docs/troubleshooting/agent-tool-failed): common fixes
