---
locale: en
category: concepts
slug: lineage
source: src/content/docs/en/concepts/lineage.tsx
---
> *Lineage helps you see how a topic is moving through your life: how often you've been touching it recently, how much mental weight you're giving it, and what stage it's evolved into.*

## The Three Signal Groups

By analyzing your journal and note content, Hyday automatically computes three signals:

### 1. Frequency

Counts how often the topic shows up in a given time window. Rising frequency means you're actively working on it. Frequency trending toward zero means it's been parked or finished.

### 2. Persistence

Measures how much you're investing in the topic. Even if frequency is low, longer entries, deeper content, or heavy use of LifeLog marks indicate the topic carries real mental weight — it's**on your mind**.

### 3. Evolution

Estimates the current stage of the topic. Is it early ideation, planning, execution, or close to wrap-up? Hyday infers this from verbs in the content, plus task-start`>(time)`and task-end`<(time)`marks.

## Exploring a Topic's Full Lineage

Click any tag or entity tag to open the**lineage drawer**:

- Current values and analysis for all three signal groups.
- Recent notes and journal snippets closely related to the topic.
- **AI lineage summary**: A synthesized narrative of how the topic has flowed through your life.

## Why Lineage Matters

Tag counts only tell you**how often**something appears. Lineage analysis surfaces the deeper signal:

- **Early warning for stress**: Notice that you've started dealing with this stressor frequently again.
- **Real-weight check**: You said it wasn't important, but the persistence signal shows you've poured serious energy into it.
- **Progress visibility**: From ideation to wrap-up, which stage is this project actually at?

> **ℹ️ Info**
> Lineage analysis sends content to the AI provider you chose. If you're concerned about data leaving your machine, configure the provider to local Ollama so the entire analysis runs on-device.

## Further Reading

- [Explore Topic Lineage: Walkthrough](https://hyday.tw/docs/guides/explore-tag-lineage): A deeper guide to working with lineage.
