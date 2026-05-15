---
locale: en
category: troubleshooting
slug: sync-conflict
source: src/content/docs/en/troubleshooting/sync-conflict.tsx
---
> * When you access the same note folder from multiple devices, file conflicts can happen. Note that Hyday itself does not perform cloud sync — these conflicts are triggered by third-party sync services (iCloud, Dropbox, and the like). *

## How Hyday Thinks About Sync

Hyday is committed to a **local-first** architecture. We **don't have, and have no plans to build**, a proprietary cloud sync service for notes. Multi-device sync relies entirely on external tools of your choosing:

- **iCloud Drive**: the natural choice for users in the Apple ecosystem
- **Mainstream cloud drives**: such as Dropbox, Google Drive, or OneDrive
- **Git version control**: recommended for technical users — gives the most precise conflict resolution

## Common Conflict Scenarios and How to Handle Them

### Scenario A: Two Devices Edit the Same Note at the Same Time

If two computers modify the same `.md` file before sync completes, the cloud service typically keeps both versions to protect your data. You'll see files named like this:

```
``
```

**What to do**: manually compare the two files, merge them, and then delete the leftover conflict copy.

### Scenario B: iCloud's **Optimize Storage** Causes Read Failures

macOS iCloud may enable **Optimize Mac Storage** by default, which moves rarely used notes to the cloud and keeps only a placeholder locally. This prevents Hyday from reading content or building the index. **What to do**:

- Go to System Settings and turn off iCloud storage optimization

## Habits That Prevent Conflicts

1. **One device at a time**: whenever possible, only write from one device at any given time
2. **Check the sync indicator**: before switching devices or shutting down your computer, make sure the sync client's icon shows a **checkmark** indicating completion
3. **Back up before major changes**: before bulk renames, directory moves, or batch edits, manually back up first

## Advanced: Manage Your Notes Folder With Git

For developers or anyone with a technical background, Git is more reliable than a general cloud drive for sync:

```
``
```

Build a habit of running `git push` at the end of each day and `git pull` when you switch devices. Even when conflicts happen, Git's three-way merge tools help resolve them precisely.

> **⚠️ Warning**
>  Whiteboard data (`.hyday/whiteboards-v2.json`) and AI conversation history (`.hyday/agent-conversations/v1.json`) are stored as single consolidated JSON files and aren't suitable for manual merging. If these files end up in a sync conflict, keep the newer version and discard the conflicting copy.
