---
locale: en
category: concepts
slug: local-first
source: src/content/docs/en/concepts/local-first.tsx
---
> * Hyday's core principle: **your notes always live on your own computer**, not on our servers. The cloud only syncs a small slice of personal settings — never your files. *

## What Lives Locally?

- **All note content** (`.md`)
- **All journal content** (`journal/year/YYYY-MM-DD.md`)
- **Whiteboards and Hyday Agent conversation history** (`.hyday/`)
- **Search index and cache** (`.hyday/`)

Everything you see in the folder is everything there is. Uninstall Hyday and these files stay intact — open them in any Markdown editor.

- **App preferences**: Filters, pinned lists, AI provider settings, and so on. Stored in the system's app data folder:   - macOS: `~/Library/Application Support/Hyday/preferences.json`
  - Windows: `%APPDATA%/Hyday/preferences.json` 

## What Syncs to the Cloud? (Optional)

When you sign in, Hyday syncs **app-related settings** to a cloud database (Firestore):

- **Dashboard card widths and positions**: Keeps the layout consistent across devices.
- **Newsletter preferences**: Records your subscription choices.
- **Editor settings**: Spell check and image width.
- **VVIP subscription status**: Used to verify access to advanced features.

Sync runs automatically when you sign in, and your cloud settings are wiped when you sign out. You can also choose not to sign in at all and use Hyday fully offline — note features all keep working.

## How AI Features Handle Your Data

When you use AI features (including but not limited to Hyday Agent, Hyday Channel, persona distillation, and lineage analysis), the relevant content is sent to the AI provider you chose. Handling depends on each provider's privacy policy:

- **Cloud providers** (OpenAI, Claude, Gemini, OpenRouter): Handled per that company's data privacy policy.
- **Local providers** (Ollama): Everything runs on your computer — nothing leaves the device.
- **CLI providers** (Claude Code, Gemini CLI, Codex): Handled per that tool's operating model.

For highly sensitive content, we recommend leaning on local AI models.

> **ℹ️ Info**
>  Set your provider to local Ollama and download a suitable model. Writing notes, AI analysis, and Agent actions can all run on-device, fully disconnected from the internet. 

## Does Hyday Work Offline?

Beyond sign-in verification and cloud AI features, **most of Hyday works offline**. Writing notes, managing your journal, exploring tags, working on the whiteboard, and running local AI all work fine without a network connection.

## Further Reading

- [Privacy and Data Storage Policy](https://hyday.tw/docs/reference/privacy): A full breakdown of where data goes.
