---
locale: en
category: troubleshooting
slug: ai-not-responding
source: src/content/docs/en/troubleshooting/ai-not-responding.tsx
---
> *If AI features hang, keep loading, or return error messages, work through the following diagnostic steps.*

## 1. Check the Provider's Connection Status

Open**Settings**(`⌘`+`,`) →**AI**, find the provider you're using, and click**Test connection**. Common reasons a connection fails:

- **API key problems**: the key has expired, been revoked, or was pasted incomplete
- **Account quota exhausted**: the cloud provider's quota has been used up
- **Provider outage**: the provider's servers are under maintenance or experiencing issues

## 2. Cloud Providers: Check Your Network

Some office networks or firewall configurations block specific AI services. Try:

- Switching to a different network (for example, a phone hotspot) for a cross-check
- Visiting the provider's official status page:[OpenAI Status](https://status.openai.com/),[Anthropic Status](https://status.anthropic.com/),[Google Cloud Status](https://status.cloud.google.com/)

## 3. Local Ollama: Verify the Service Is Running

Run this command in your terminal to test whether Ollama is responding:

```
``
```

A 200 response means it's working. If you see`Connection refused`, the Ollama service isn't running. Start it with:

```
``
```

Also confirm the configured model has been downloaded:

```
``
```

## 4. Custom Endpoints: Verify the URL Format

Hyday handles the`/v1`path suffix automatically. Check your Base URL setting:

- If you enter`https://api.example.com`: Hyday will call`/v1/chat/completions`
- If you enter`https://api.example.com/v1`: Hyday will call`/chat/completions`directly

Note that the custom endpoint must be OpenAI-compatible, or it will not work correctly.

## 5. The AI Agent Hangs Mid-Task

If the Agent gets stuck in a loop or stops responding while running a task:

- Click the**Stop**button in the top-right corner of the conversation pane to abort
- Start a fresh conversation to test
- If a specific prompt repeatedly causes a hang, check whether the selected model fully supports**tool calls**— see the[AI provider reference](/docs/reference/ai-providers)

## 6. Common Error Codes

Error codeMeaningWhat to do401API key errorDouble-check the key and paste the correct one403Permission deniedConfirm your account has access to that specific model429Rate limit exceededWait a moment and retry, or upgrade your account tier500 / 503Provider outageThis is on the provider's end — watch their official status pageContext length exceededContent exceeds the model's context windowSend fewer notes at once, or switch to a model with a larger context window

> **ℹ️ Info**
> If one provider keeps failing, temporarily switch to another (for example, from a cloud provider to local Ollama). If everything works after switching, the problem is on the provider's end, not Hyday's.
