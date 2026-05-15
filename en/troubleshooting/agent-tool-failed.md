---
locale: en
category: troubleshooting
slug: agent-tool-failed
source: src/content/docs/en/troubleshooting/agent-tool-failed.tsx
---
> * If the AI Agent throws an error after calling a tool, or gets stuck in an infinite loop calling the same tool with no result, follow the steps below to troubleshoot. *

## 1. Stuck in a Widget Render Retry Loop

When the Agent fails while calling `render_widget`, it can occasionally retry excessively. **Symptoms**:

- New, malformed widget components keep popping up in the conversation window
- The conversation history grows rapidly, causing `.hyday/agent-conversations/v1.json` to balloon in size and slow the app down

**What to do**:

1. Immediately click the **Stop** button in the top-right corner of the conversation pane to abort the task
2. Abandon the current conversation and start a new one
3. If a specific prompt reliably triggers this behavior, open a GitHub Issue and attach an example of the widget content that caused it

## 2. The Provider Does Not Support Tool Calls

If the AI Agent never actually runs any tools and only describes **what it intends to do** in plain text, the selected model probably does not support function calling.

See the [AI provider reference](/docs/reference/ai-providers) and switch to an advanced model that supports agentic tool use.

## 3. Clean Up a Corrupted Conversation File

If a conversation file became slow or unresponsive after a previous retry loop, remove it entirely:

1. Find the problem conversation in the sidebar list
2. Click "..." and choose **Delete conversation**
3. Start a fresh conversation from a clean state

> **⚠️ Warning**
>  Cleaning up a conversation only affects the deleted entry inside `.hyday/agent-conversations/v1.json` — **it does not delete or modify any note content**. That said, **Delete conversation** cannot be undone. If the content is important, back up the conversation file before deleting.
