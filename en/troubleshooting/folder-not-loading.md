---
locale: en
category: troubleshooting
slug: folder-not-loading
source: src/content/docs/en/troubleshooting/folder-not-loading.tsx
---
> *If Hyday hangs on a loading screen at startup, or the sidebar is completely empty, follow the steps below to troubleshoot.*

## 1. Confirm the Folder Path Is Still Valid

The folder path Hyday remembers can become invalid if the folder was moved, renamed, or lives on a disconnected external drive.

Press`⌘`+`,`to open**Settings**→**Storage**→ click**Change folder**and select the correct path.

![Data management tab in Settings](https://hyday.tw/docs/screenshots/ui-settings-data-folder.png)

## 2. Verify File Access Permissions

On macOS, when you first open a folder on an external drive, iCloud, or a removable disk, the system asks for permission to access it. If you accidentally clicked**Don't Allow**, go to**System Settings → Privacy & Security → Files and Folders**and grant Hyday access manually.

## 3. Rebuild the Index

If you made large manual changes to the folder structure (for example, batch-synced a lot of files via`git pull`), the local index may temporarily be out of sync.

Open the Command Palette and run the**Rebuild folder index**command.

## If None of the Above Worked

1. Quit Hyday completely
2. Go to your notes folder and delete the entire`.hyday/`subfolder (it will be fully rebuilt on next launch)
3. Restart Hyday

> **⚠️ Warning**
> This operation never damages your note content — all`.md`files are preserved. The index data is purely derived cache and can safely be rebuilt at any time.

If the problem persists after a full rebuild, file a report on[GitHub Issues](https://github.com/mukiwu/hyday/issues)and include a screenshot of the Console log and a rough count of files in the folder.
