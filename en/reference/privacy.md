---
locale: en
category: reference
slug: privacy
source: src/content/docs/en/reference/privacy.tsx
---
<!-- UNCONVERTIBLE: Lock --> Never uploaded 

 <!-- UNCONVERTIBLE: Cloud -->  

> * Hyday is 100% committed to keeping your notes yours. Note content is only stored on your device and is never uploaded to Hyday's servers. Cloud sync is limited to a small amount of system preferences and licensing data. The table below details how each category of data flows. *

## Data Categories and Flow

   Data Category Storage Location Synced to the cloud?    Note body contentYour chosen local folder (`.md`)<!-- UNCONVERTIBLE: LocalOnly --> Journal entries and life momentsYour chosen local folder (`.md`)<!-- UNCONVERTIBLE: LocalOnly --> Visual whiteboard dataLocal folder `.hyday/whiteboards-v2.json`<!-- UNCONVERTIBLE: LocalOnly --> AI agent conversation historyLocal folder `.hyday/agent-conversations/v1.json`<!-- UNCONVERTIBLE: LocalOnly --> Tag and entity stats and indexesCache directory in the local hidden folder<!-- UNCONVERTIBLE: LocalOnly --> Global filters and pinned listLocal `preferences.json`<!-- UNCONVERTIBLE: LocalOnly --> Account login infoEncrypted secure transport<!-- UNCONVERTIBLE: CloudSynced --> VVIP subscription and payment statusEncrypted database<!-- UNCONVERTIBLE: CloudSynced --> Authorized device listEncrypted database<!-- UNCONVERTIBLE: CloudSynced --> Home page card layoutEncrypted database<!-- UNCONVERTIBLE: CloudSynced --> Newsletter subscription preferencesEncrypted database<!-- UNCONVERTIBLE: CloudSynced -->  

## AI Feature Privacy

When you use an AI feature (such as chat, the Agent, persona distillation, or lineage analysis), the relevant note excerpts are sent to your chosen service provider:

- **Cloud providers** (OpenAI / Claude / Gemini / OpenRouter, etc.): data handling is governed by each company's privacy policy. Most providers offer an option to **opt out of using API data for model training**; see their official documentation.
- **Local provider** (Ollama): all computation runs inside your computer; data never leaves your local network and works offline.

> **⚠️ Warning**
>  Hyday cannot control how your chosen **cloud provider** accesses data on its servers. For highly sensitive content (trade secrets, personal health information, or identity data), we strongly recommend running the local Ollama backend as your AI engine. 

## Telemetry and Usage Statistics

Hyday is committed to a tracking-free experience and **does not collect** any telemetry about your behavior (which buttons you click, which notes you open, and so on). When you sign in, the system only sends the following essential information to keep features working:

- **App version**: used for automatic update checks and prompts.
- **Device hardware info**: OS and chip type, used for license verification and compatibility tuning.

## What Happens When You Sign Out

When you sign out:

- **All local content and settings are preserved in full.**
- **Home page layout** and **newsletter subscription settings** stored in Firestore are removed.
- Your VVIP license record stays safely tied to your account and is restored when you sign back in.

## What Happens If You Uninstall the App

- **Your notes folder remains intact** — you can continue reading the content with any third-party Markdown editor.
- The local `preferences.json` file usually stays in the system path; you can choose to inherit it on reinstall (manually).
- Cloud records remain stored until you actively request account deletion.

## Contact the Privacy Team

If you have any questions or concerns about data safety, email `mukispace@gmail.com`. We aim to reply in detail within 7 business days.
