---
locale: en
category: concepts
slug: ai-agent
source: src/content/docs/en/concepts/ai-agent.tsx
---
> * AI Agent is Hyday's built-in advanced assistant. Beyond regular conversation, it can actively call **tools** to read notes, create new files, run lineage analysis, and organize your tasks. *

## Chat Mode vs. Agent Mode

- **Chat mode**: Pure text conversation. The AI answers your questions but doesn't access or modify any file in your folder.
- **Agent mode**: The AI can **act**. It calls tools to read notes, write content, query tags, or run deep analyses on your behalf.

## The AI Agent's Toolbox (Capabilities)

- **Read content**: Open a specific note or the journal entry for a given date.
- **Create content**: Spin up new notes or append a summary to today's journal.
- **Structured search**: Find notes matching specific tags, time ranges, or entity references.
- **Deep lineage analysis**: Run the lineage algorithm to surface trends on a topic.
- **Task scanning**: Pull TODOs out of messy notes.
- **Widget rendering**: Generate charts, comparison tables, or other interactive widgets.

## Conversation History and Traceability

All Agent conversations are saved in a single JSON file at `.hyday/agent-conversations/v1.json` inside your notes folder. Revisit conversations anytime or check the file into version control.

## Supported Providers

Agent mode requires native **tool calling** support, so we recommend these providers:

- **OpenAI**: GPT-4o or newer.
- **Anthropic Claude**: Claude Sonnet or Opus.
- **Google Gemini**: Gemini 2.5, 3.0, or later.
- **OpenRouter**: Depends on the underlying model you pick.
- **Local Ollama**: Pick a model that supports function calling. Performance depends on your hardware.

## Further Reading

- [Configure an AI Provider](https://hyday.tw/docs/guides/configure-ai-provider): How AI providers map to Hyday features.
- [AI Agent Hands-On Guide](https://hyday.tw/docs/guides/use-ai-agent): Conversation patterns that work.
- [Full Agent Tool List](https://hyday.tw/docs/reference/agent-tools): Capabilities and limits of each tool.
