---
locale: en
category: guides
slug: sign-in-and-sync
source: src/content/docs/en/guides/sign-in-and-sync.tsx
---
> * Signing in is entirely optional in Hyday. You get the full notes and journal experience offline without an account. Signing in unlocks VVIP entitlement, official updates, and cross-device preference sync. *

## 1. Why Sign In?

- **Cross-device settings sync**: keep UI preferences, home layout, and other user settings consistent across multiple computers
- **Entitlement check**: verifies your VVIP subscription
- **Official updates**: newsletter subscriptions

## 2. How to Sign In

1. Go to **Settings → Account** and click **Sign in**
2. Hyday opens your default browser to walk through the Google OAuth flow
3. Once authorized, return to Hyday and sync completes automatically

Today only Google sign-in is supported. More sign-in methods are coming.

## 3. What Gets Uploaded to the Cloud?

While signed in, Hyday only syncs **a minimal set of entitlement and preference data** to the encrypted cloud database (Firestore):

- Newsletter subscription status
- UI language, theme, and font preferences
- Editor and content display preferences (spell check, image width, Mermaid settings)
- Home cards and the layout/sort order of the notes / journal / tasks pages
- AI model, AI exclusion tags, Insights, and lineage personalization settings
- Pinned filters and Channel notifications

## 4. About Signing Out

You can sign out anytime from **Settings → Account**. When you sign out:

- **Local notes stay completely intact** — signing out doesn't touch them
- Cloud-synced UI preferences are removed from this device
- The app returns to an **offline / unauthenticated** state, with the core Markdown editor still fully working

## 5. Multi-Device Tips

The same Google account can be signed in on several machines to share VVIP entitlements. Just remember that **Hyday does not sync the note contents themselves**: you need to deploy your notes folder across devices using a sync app or Git.

## Further Reading

- [Local-First and Cloud Architecture](https://hyday.tw/docs/concepts/local-first): a deeper look at the data flow.
- [Troubleshooting: Sign-in Issues](https://hyday.tw/docs/troubleshooting/login-failed): common fixes for authorization failures.
