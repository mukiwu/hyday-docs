---
locale: en
category: concepts
slug: stages
source: src/content/docs/en/concepts/stages.tsx
---
> *Stages mark how mature a note is, on a three-tier scale:**Seed, Sapling, Evergreen**. They're not just decoration — they directly shape the lineage analysis call on which stage a topic is currently in.*

## Why Stages?

The same topic at different times has very different value and character: a freshly sparked idea, a draft still being rewritten, and a fully structured mature note — mixing them together distorts the lineage of a topic.

Stages exist to separate those three states, so Hyday can tell whether a topic is**just sprouting**,**actively being worked on**, or**already settled**.

## The Three Stages

### Seed

A raw thought, spark, quote, or fragment you just captured — not yet rewritten in your own words, not yet linked to other notes. Seed means "this topic just sprouted".

Journal entries don't need manual stage marking —**the system treats them as Seeds automatically**, since journals are where ideas first surface.

### Sapling

A note you've started rewriting in your own words, tidying up, and connecting to other notes via backlinks or tags. Sapling means "this topic is being worked on".

If a note has no manual stage but contains[LifeLog time marks](https://hyday.tw/docs/concepts/lifelog-marks)(`>(`,`<(`,`-(`,`%(`,`!(`), Hyday infers it as a Sapling — those marks signal "in progress". A manual stage always overrides the auto-inferred one.

### Evergreen

A mature note that's structurally complete, atomic, and stable. Evergreen notes are a topic's**resting point**— referenced repeatedly without changing often.

## How Stages Affect Lineage Analysis

When computing how "active" a topic is, lineage analysis weights notes differently by stage:

- **Seed**carries the highest weight — a freshly sprouting idea signals the topic is entering your attention.
- **Sapling**comes next — being worked on counts as actively in motion.
- **Unmarked**: kept at a low weight so old, untouched notes don't muddy the topic signal.
- **Evergreen**has weight 0 — settled mature notes no longer drive the activity score, but remain searchable and referenceable.

In other words,**promoting a note from Sapling to Evergreen tells Hyday: I've worked this aspect of the topic out**. Lineage analysis stops counting it toward the "currently in progress" signal.

> **ℹ️ Info**
> There's no need to rush a promotion — stages are signals to your future self. We recommend promoting to Sapling only after you've**actually rewritten the content in your own words**, and to Evergreen only when**the content is stable and unlikely to need big rewrites**.

## How to Set a Stage

The title bar at the top of the note editor shows the current stage label (default "Unmarked"). Click it to pick Seed, Sapling, or Evergreen — or choose "Clear stage" to go back to unmarked.

![Stage label](https://hyday.tw/docs/screenshots/concepts-stages-1.png)

## Further Reading

- [Lineage Analysis](https://hyday.tw/docs/concepts/lineage): How stages feed into the topic evolution signal.
- [LifeLog Time Marks](https://hyday.tw/docs/concepts/lifelog-marks): The basis for automatic stage inference when unmarked.
