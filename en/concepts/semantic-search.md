---
locale: en
category: concepts
slug: semantic-search
source: src/content/docs/en/concepts/semantic-search.tsx
---
> * Semantic search lets you find notes by meaning rather than exact words — even when you can't recall the keywords you originally used. Everything runs on your own machine, and the index never leaves your computer. *

## What problem does it solve?

 Regular full-text search matches **literal words**: searching for "stressed" only finds notes that actually contain that word. But often you remember *writing about a feeling* without remembering the exact wording. 

 Semantic search compares **meaning** instead. For example, if you once wrote "work has been moving way too fast lately," searching for **"stressed"** or **"overwhelmed"** will still surface that note, because they describe a similar feeling. 

## How it works

 Hyday turns each note into a string of numbers that represents its meaning (an **embedding vector**). When you search, your query is turned into a vector too, and Hyday finds the notes whose meaning is closest. 

 This conversion is handled entirely by **local Ollama**, so you need a dedicated embedding model installed. That is also the key difference from cloud AI: **your note content is never sent to any external server**. 

## Enabling it

Semantic search is off by default. Before turning it on, get Ollama and an embedding model ready:

- Make sure **Ollama** is installed and running (the same local-model setup as in [Configure AI Provider](https://hyday.tw/docs/guides/configure-ai-provider))
- Have an embedding model ready, such as the default `bge-m3` (best CJK support)
- Press `⌘`+`,` to open Settings, go to the **AI** tab, find the **Semantic Search** section, turn on **Enable semantic search**, and pick an Embedding Model

> **ℹ️ Info**
>  If you don't have an embedding model yet, the settings page lists recommended ones (`bge-m3`, `qwen3-embedding:0.6b`, and more) that you can download directly in Hyday — no need to run `ollama pull` in a terminal. 

## Where is the index stored?

 Once enabled, Hyday computes a vector for each note in the background and stores them in a single index file, inside the hidden directory of your notes folder: 

```
``
```

- The index updates **incrementally in the background**: editing one note only re-embeds that note, without interrupting your reading or writing
- It is **derived, rebuildable data**: delete it and hit "Rebuild Index" in settings to re-scan your whole library and regenerate it
- It contains only vectors plus a title and preview snapshot, and **always stays on your machine** — it is never synced to the cloud

> **ℹ️ Info**
>  Whether semantic search is on and which model you picked is synced to the cloud after you sign in. The actual vector index, however, lives only on your machine — each device builds its own. 

## See also

- [Configure AI Provider](https://hyday.tw/docs/guides/configure-ai-provider): install and set up local Ollama
- [File Structure & Sidecar](https://hyday.tw/docs/reference/file-structure): other indexes and caches inside `.hyday/`
- [Local-First & Cloud](https://hyday.tw/docs/concepts/local-first): what stays local and what syncs
