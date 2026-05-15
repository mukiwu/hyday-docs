---
locale: en
category: concepts
slug: filters
source: src/content/docs/en/concepts/filters.tsx
---
> *Filters help you quickly narrow notes down by combining conditions. Pin frequent filters to the sidebar and shift away from rigid folder hierarchies toward a more flexible tag-driven mindset.*

## Available Filter Conditions

- **Tag filter**: Include or exclude specific`#tag`values.
- **Content type**: Narrow to a specific type, like`article`,`card`, or`journal`.
- **Sort order**: Sort by**title, tag, or date**.

## Condition Logic

Use**match all (AND)**or**match any (OR)**to build richer filtering logic:

- **Pinpoint**:`#work`AND`#weekly-report`finds every work weekly report.
- **Union search**:`#health`OR`#exercise`surfaces notes from either topic.

## Pin Frequent Filters

Save the filters you use often as**pinned filters**. They stay at the top of the sidebar:

![Pinned filters](https://hyday.tw/docs/screenshots/concepts-filters-1.png)

> **ℹ️ Info**
> In Hyday, the same note can appear in multiple filter views at once. That's the flexibility of pairing tags with filters — and it breaks the one-folder-per-file constraint of traditional folder trees.

## Where Filters Are Stored

Filter settings currently live in the local preferences file on your computer (`preferences.json`). They don't sync across devices yet, so if you switch machines you'll need to recreate your favorite filters.

## Further Reading

- [Pin Frequent Filters: Walkthrough](https://hyday.tw/docs/guides/pin-filters): A step-by-step example.
- [Full Filter Condition List](https://hyday.tw/docs/reference/filter-conditions): Every available filter parameter.
