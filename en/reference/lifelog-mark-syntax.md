---
locale: en
category: reference
slug: lifelog-mark-syntax
source: src/content/docs/en/reference/lifelog-mark-syntax.tsx
---
> *This page explains the syntax rules for LifeLog marks, which give you precise, machine-parseable timeline records.*

## The Five Mark Syntaxes

SyntaxMark NameCategoryContent Inside Parentheses`>(HH:mm)`Task start (taskStart)TimeTime in HH:mm format`<(HH:mm)`Task end (taskEnd)TimeTime in HH:mm format`-(HH:mm)`Current moment (current)TimeTime in HH:mm format`%(content)`Thought / insight (thought)ContentAny descriptive text`!(content)`Important (important)ContentAny key text

## Core Parsing Rules

- A mark must be a contiguous run of characters on a single line —**no line breaks in the middle**.
- The text inside the parentheses**cannot contain another`)`**, or parsing will terminate early.
- The mark must be preceded by either the**start of a line**or a**whitespace character**; otherwise it is not parsed. (This rule prevents false positives inside URLs or code blocks.)
- Any text or other marks may follow immediately after a mark.

The internal regular expression used by the system, for reference:

```
``
```

## Time Format Guidance

For time marks, we strongly recommend`HH:mm`(24-hour clock, e.g.`09:00`,`14:30`). Hyday is somewhat forgiving, but the standard format gives the internal analysis engines (timeline rendering, activity stats, and so on) the most accurate results.

## Combining with Other Syntax

The descriptive text next to a mark may freely contain`[[]]`,`#`, or`@`; the system will parse these relationships at the same time:

```
``
```

> **⚠️ Warning**
> The**contents inside a LifeLog mark's parentheses**must not include`[[]]`,`#`, or`@`.**Incorrect**:`>(09:00 #work)`— the inner`#work`will not be recognized as a tag.

## Time-Order Authoring Tips

Hyday doesn't enforce ordering, but we recommend writing the day's LifeLog marks in chronological order:

- Improves reading flow and intuition.
- The analysis engine sorts automatically, but an ordered record reduces the risk of missing entries.
- You can include multiple`%()`or`!()`within the same hour; they display in the order they appear in the file.

## Handling Cross-Day Records

LifeLog marks are scoped to a single journal file. If a task crosses midnight, split it into the corresponding date's journal entry. For example, write a 1 AM event in the**new day's**journal — don't use non-standard notations like`>(25:00)`.
