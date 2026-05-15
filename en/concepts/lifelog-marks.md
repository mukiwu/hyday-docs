---
locale: en
category: concepts
slug: lifelog-marks
source: src/content/docs/en/concepts/lifelog-marks.tsx
---
> * LifeLog marks help you capture key moments in your journal: **when you started**, **when you finished**, **what just came to mind**, or **what matters**. A few simple characters, and you mark the moment without breaking your writing flow. *

## Five Marks, Two Categories

 Marks come in two flavors: three for **time anchors** (with `HH:mm` inside the parentheses), and two for **content carriers** (with the actual text inside the parentheses). 

### Time Marks

   Syntax Mark Name Purpose     `>(HH:mm)` Task start (taskStart) Records **starting something at this time**.   `<(HH:mm)` Task end (taskEnd) Records **finishing or stopping something at this time**.   `-(HH:mm)` Current (current) Records **what's happening or how you feel right now**.   

> **ℹ️ Info**
>  The actual event description goes next to the mark. For example, `>(09:00) Process inbox` means at 09:00 you started a task called **Process inbox**. 

### Content Marks

   Syntax Mark Name Purpose     `%(content)` Thought (thought) Captures a sudden idea, a reflection, or a meta-thought.   `!(content)` Important (important) Flags the must-remember points so they're easy to find later.   

## Why Split Them Into Two Categories?

- **Time marks** focus on **when an event happened**; the description stays in natural prose.
- **Content marks** focus on **thoughts worth revisiting**; the mark itself carries the core information.

 The split lets the system extract clean timeline data while preserving your personal writing voice and rhythm. 

## A Writing Example

```
``
```

## Flexible Mark Positions

Time marks can appear anywhere on a line — Hyday treats the whole line as the mark's context:

```
`>(09:00) Cleared the inbox, took less than an hour <(09:50)`
```

 Putting marks at the start of a line tends to read best, but Hyday doesn't require a fixed position. 

> **ℹ️ Info**
>  Text next to a mark can include `[[note name]]` backlinks, `#tag`s, or `@entity` references: `-(14:30) [[Q3 Roadmap]] meeting with @Alice #work` 

## The Foundation for Analysis

 LifeLog marks are the foundation Hyday uses for lineage analysis, task scanning, and the AI Agent. The more you log, the more accurately Hyday can recognize your work patterns, habit cycles, and emotional rhythms. 

![LifeLog explorer drawer: timeline view grouped by mark type](https://hyday.tw/docs/screenshots/concepts-lifelog-marks-1.png)

> **ℹ️ Info**
>  There's no expectation to log on any particular cadence — Hyday isn't measuring your **diligence**. The more detail you log, the richer the insights when you look back. 

## Further Reading

- [Track a Day With LifeLog](https://hyday.tw/docs/guides/track-a-day-with-lifelog): A full day-in-the-life example.
- [LifeLog Mark Syntax Reference](https://hyday.tw/docs/reference/lifelog-mark-syntax): Complete syntax rules.
