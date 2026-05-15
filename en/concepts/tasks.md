---
locale: en
category: concepts
slug: tasks
source: src/content/docs/en/concepts/tasks.tsx
---
> *In Hyday, tasks aren't a separate to-do list that sits outside your notes. Hyday scans your notes and journal entries for todos automatically, so you can manage tasks naturally as you write.*

## How Does Content Become a Task?

Hyday recognizes tasks primarily through these patterns:

### Standard Markdown Task Lists

```
``
```

### Setting Due Dates and Schedules

Type`/`to open the panel and choose to set a due date, scheduled date, or start date:

- **Due date**: The task must be done by this date. Once it passes uncompleted, it falls into the**Overdue**bucket and is highlighted in red.
- **Scheduled date**: When you intend to work on the task. Past due is also treated as**Overdue**.
- **Start date**: You can't start the task until this date. Before the start date it sits in the**Scheduled**bucket; once it arrives, instead of becoming overdue it moves to**Next**.

You can use all three at once. For example, the same todo can have both a start date and a due date — describing "you can work on it from this day, you have until this day".

The bottom of the panel also lets you set the task's**priority**, which affects ranking on the dashboard:

- **Highest priority**: The most urgent tasks. Ranked first.
- **High priority**: Important, but not urgent.
- **Low priority**: Lesser priorities.
- **Lowest priority**: Nice-to-haves. Ranked last.

Tasks without an explicit priority are treated as normal — ranked between High and Low.

![Date marks added after a todo](https://hyday.tw/docs/screenshots/concepts-tasks-2.png)

## The Task Management View

The sidebar's**Tasks**tab sorts everything Hyday finds into seven buckets:

- **Overdue**: Tasks whose due or scheduled date has passed and remain undone.
- **Today**: Tasks due today, scheduled for today, or starting today.
- **Upcoming**: Tasks whose due date is within the next three days and need attention soon.
- **Scheduled**: Tasks with a future date or start date that aren't yet eligible to start.
- **Next**: Todos without a specific execution time set.
- **Completed**: Tasks already checked as`[x]`. Hidden by default — use the toolbar's**Show completed items**option to view.
- **Canceled**: Tasks marked as`[-]`— kept on record but excluded from your active list.

![Task management view](https://hyday.tw/docs/screenshots/concepts-tasks-1.png)

## Trace Back to the Source

Every task card supports a quick jump. Click a task to land right where it appears in the note or journal entry, with that line highlighted automatically so you can pick up the context fast.

## Completion and State Sync

When you check off a task in the Tasks view, Hyday:

- Updates the source Markdown file from`- [ ]`to`- [x]`.
- Removes the item from the current list (unless**Show completed items**is on).

> **ℹ️ Info**
> Hyday is intentionally low-pressure: no push notifications, no streaks. The task view is designed to help you see what's on your plate, not to add to it.
