---
locale: en
category: guides
slug: configure-ai-provider
source: src/content/docs/en/guides/configure-ai-provider.tsx
---
> *Hyday supports three ways to plug in AI:**cloud API services**,**CLI subscriptions**(Claude Code / Gemini CLI / Codex CLI), and**local models**(Ollama). All settings live under**Settings → AI**.*

## How the Three Options Compare

TypeWhat you needBillingTool callingCloud API serviceAn API key from each providerBilled by API usageDepends on the modelCLI subscriptionClaude Code / Gemini CLI / Codex CLIinstalled and signed in locallyUses your existing subscription —**no extra charge**Uses the CLI's built-in tools(including web search)Local modelOllama installed and running locallyFree and offlineDepends on the model — most are weaker

## Supported AI Providers

### Cloud API Services

- **OpenAI**: GPT-4o family, GPT-5 family, and more
- **Anthropic Claude**: Claude Opus / Sonnet / Haiku family
- **Google Gemini**: Gemini Pro / Flash family
- **OpenRouter**: a single entry point that aggregates models from many providers
- **Custom (OpenAI-compatible)**: for Groq, Together AI, Fireworks, and other self-hosted or third-party compatible endpoints

### CLI Subscriptions (Recommended If You Already Have One)

If you already subscribe to any of the following services, Hyday can route through the CLI to use that subscription directly —**without consuming additional API quota**:

- **Claude Code**
- **Gemini CLI**
- **Codex CLI**

CLI backends come with built-in web search and file operations, so**features that need live research — like persona distillation and lineage analysis — work out of the box on a CLI backend**. Cloud API backends need the underlying model itself to support those tools.

### Local Models

- **Ollama**: open-source models that run locally. All computation stays on your device and works offline.

## 1. Configure a Cloud API Provider

Press`⌘`+`,`to open settings, switch to the AI tab, pick a provider and model, and enter your API key. Click "Test connection" to verify the key works.

Common errors:`401`= bad key,`429`= rate limit exceeded.

![Settings → AI tab showing the provider list and API key input](https://hyday.tw/docs/screenshots/guides-configure-ai-provider-1.png)

> **ℹ️ Info**
> **Base URL**: enter the service endpoint (Hyday handles the trailing`/v1`automatically)**Model**: enter the exact model ID the provider exposes, for example`llama3.1:8b`or`gemini-flash-lite-latest`

## 2. Set Up and Pick a CLI Subscription

> **⚠️ Warning**
> Make sure the relevant CLI is installed and signed in locally. Hyday auto-detects sign-in status; ready CLIs show up as "Verified" in settings.

- **Claude Code**: follow the[official Anthropic docs](https://docs.anthropic.com/en/docs/claude-code)to install`Claude Code`and sign in
- **Gemini CLI**: follow the[official Google docs](https://geminicli.com/)to install`Gemini CLI`and sign in
- **Codex CLI**: follow the[official OpenAI docs](https://platform.openai.com/docs/plugins/introduction)to install`Codex CLI`and sign in

![Settings → AI tab showing CLI subscription configuration](https://hyday.tw/docs/screenshots/guides-configure-ai-provider-2.png)

## 3. Set Up Local Ollama

First make sure Ollama is running on your machine:

```
``
```

Back in Hyday's settings, enable**Ollama**. The default connection address is`http://localhost:11434`.

## 4. Assign a Different Model to Each Feature

If you have multiple subscriptions or API providers, you can assign a different model to each feature.

![Settings → AI tab showing per-feature routing](https://hyday.tw/docs/screenshots/guides-configure-ai-provider-3.png)

> **⚠️ Warning**
> Both cloud APIs and CLI subscriptions send note snippets to the provider's servers, governed by their privacy policy. If your notes contain highly sensitive data, switch to local Ollama instead.

> **ℹ️ Info**
> If you already subscribe to Claude / ChatGPT / Gemini,**the CLI subscription is the best deal**— no extra charges and access to stronger models. If you don't have a subscription and prefer pay-as-you-go, cloud APIs are simpler. For maximum privacy, choose Ollama.

## Further Reading

- [AI Provider Reference](https://hyday.tw/docs/reference/ai-providers): full model list and tool calling support
- [Hyday Agent](https://hyday.tw/docs/guides/use-ai-agent): the full feature walkthrough for Agent mode
- [Hyday Channel](https://hyday.tw/docs/guides/hyday-channel): turn Claude Code into a real-time collaborator
