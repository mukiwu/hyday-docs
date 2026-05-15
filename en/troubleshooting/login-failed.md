---
locale: en
category: troubleshooting
slug: login-failed
source: src/content/docs/en/troubleshooting/login-failed.tsx
---
> *If Google sign-in misbehaves, the browser redirect never returns to the app, or you stay marked as "not signed in" even after a successful login, this guide walks you through the fix.*

## 1. The Standard Sign-In Flow

A normal sign-in flow looks like this:

1. Open**Settings**→**Account**and click the**Sign in**button
2. Hyday opens your default browser and redirects to Google's authorization page
3. After you grant authorization, the browser shows**Sign-in successful, return to Hyday**
4. Switch back to the app and the UI should automatically update to the signed-in state

## 2. Authorized Domain Error

If you see`Error 400: redirect_uri_mismatch`or a similar message, that's typically a Firebase configuration issue on the cloud side. Users can't fix this — file an Issue and we'll handle it.

## 3. Sign-In Succeeded but the VVIP Subscription Status Hasn't Updated

If you've subscribed but the UI still shows the Free tier:

- **Force a refresh**: try**signing out**and then**signing in**again
- **Check the account matches**: confirm the Google account you're signed in with is the exact one you used when purchasing the subscription
- **Wait for the system to sync**: cloud database permission sync can occasionally lag by a few minutes

## 4. Contact the Development Team

If none of the above worked, file an Issue and include a screenshot of your payment receipt so we can investigate.

> **ℹ️ Info**
> Hyday's core features don't require sign-in. If a login issue is hard to resolve right now and you only need local notes, you can**simply stay signed out**— this won't affect 99% of the core editing and management features. You can try signing in again after a future update.
