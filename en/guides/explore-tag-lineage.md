---
locale: en
category: guides
slug: explore-tag-lineage
source: src/content/docs/en/guides/explore-tag-lineage.tsx
---
> *The lineage drawer is Hyday's core interface for exploring a topic. Open it by clicking any tag, entity, or LifeLog mark. It consolidates statistics, the timeline, and related topics into a single panel — and can call on AI for deeper lineage analysis.*

## 1. What the Drawer Shows

Click any**tag**(`#tag`),**entity**(`@entity`), or**LifeLog mark**(`>(`,`<(`,`-(`,`%(`,`!(`) and the drawer slides in from the right. It's made up of these sections:

![Lineage drawer showing the topic header, three-column stats, and tabbed content](https://hyday.tw/docs/screenshots/ui-lineage-drawer.png)

### Topic Header

The top displays the selected topic, its type (tag / entity / lifelog), the date it first appeared, and the total number of records — quick context to ground you.

### Three Live Stats

- **Last 7 days**: occurrences over the past week, plus the percentage change vs. the previous week (shown only when the difference exceeds 10%)
- **Related topic**: the tag or entity most frequently co-occurring with this topic
- **Open tasks**: the count of unclosed`>(`tasks tied to this topic

### Three Tabs

- **Overview**: core summary, strongly connected topics, things to watch, and sentiment analysis (LifeLog topics only)
- **Timeline**: historical records grouped by file and sorted by date — useful for spotting active periods and gaps at a glance
- **Related**: other topics that co-occur most often with this one within a chosen time window (default 30 days)

## 2. Lineage Analysis (VVIP Only)

The AI analysis built into the drawer is a[VVIP-only feature](https://hyday.tw/docs/reference/plans). It sends the last 90 days of records for the topic to your configured AI provider and produces a text summary. Two analyses are available:

### Topic Evolution

Located at the top of the**Overview**tab — click "Analyze lineage" to start. The AI answers:

- Are your thoughts on this topic currently**exploring, clarifying, deepening, or repeating**?
- Has your stance shifted? (e.g. you leaned toward A three months ago and have moved toward B recently)
- Which other topics does this one keep getting tangled with?

Results are cached after generation. Click "Regenerate" to refresh, or "Collapse" to fold the panel.

### Timeline Highlights

Located at the top of the**Timeline**tab — click "Extract highlights" to start. The AI groups records from the last 90 days into:

- **Completed**: what you actually finished during this period
- **Key decisions**: explicit judgments and trade-offs recorded
- **Open items**: things still in progress that need follow-up

> **ℹ️ Info**
> AI analysis calls the provider you've configured. If the network is shaky, the provider isn't set up, or it can't respond, you'll see**Unable to analyze**. If the topic doesn't have enough history to yield a meaningful trend, you'll see**Insufficient data**. If you have concerns about sending data out, switch to local Ollama under**Settings → AI**.

## When to Open the Lineage Drawer

- **Periodic reviews**: at month- or quarter-end, check which topics have absorbed your energy lately
- **Recurring problems**: trace how you've thought about the same topic over time and avoid repeating mistakes
- **Big decisions**: before committing, quickly review the topic's history and context
- **Reconnecting lost threads**: use the "Related topic" stat and the "Related" tab to discover what you once tied this topic to

## Further Reading

- [Lineage Analysis](https://hyday.tw/docs/concepts/lineage): the calculation logic behind the three development signals
- [Stages](https://hyday.tw/docs/concepts/stages): how stages influence lineage weighting
- [Plan Comparison](https://hyday.tw/docs/reference/plans): differences between VVIP and Free
