---
locale: en
category: reference
slug: ai-providers
source: src/content/docs/en/reference/ai-providers.tsx
---
> *Hyday supports multiple AI service providers, so you can pick the model that best fits your needs for speed, reasoning, or privacy. This page covers providers configured via an**API key (or local endpoint URL)**; Claude Code, Gemini CLI, Codex CLI, and similar CLI backends are not covered here.*

## Supported Providers

ProviderModeTool CallingRequirementsOpenAICloudSupportedAPI keyAnthropic ClaudeCloudSupportedAPI keyGoogle GeminiCloudSupportedAPI keyOpenRouterCloud aggregatorDepends on underlying modelAPI keyOllamaLocalDepends on underlying modelLocal Ollama serviceCustom (OpenAI-compatible)Cloud / self-hostedDepends on endpoint configurationBase URL + API key

## OpenAI Models

The Hyday settings page offers the following OpenAI models by default (listed in recommended order):

- **GPT-5.5 / GPT-5.5 Pro**(2026-04): The latest flagship, with a 1M-token context window and significantly improved agentic coding and long-running agent capabilities; the Pro version is further tuned for complex reasoning.
- **GPT-5.4**: The previous-generation flagship, a stable fallback choice.
- **GPT-5-mini / GPT-5-nano**: Lightweight versions, tuned for moderate and extremely low latency / cost respectively.
- **GPT-4.1**: Extremely reliable tool calling; recommended when you need strict schema control.
- **o4-mini**: A reasoning-oriented lightweight model, suited for step-by-step math and code-debugging tasks.

## Anthropic Claude Models

The Hyday settings page offers the following Claude models by default (listed in recommended order):

- **Claude Opus 4.7**(2026-04): The current top-tier flagship, with agentic coding significantly improved over 4.6 and visual resolution up to 3.75 MP. Best for the most complex reasoning and long-document analysis.
- **Claude Sonnet 4.6**(2026-02): The best all-rounder for the price; in Claude Code internal testing, 59% of developers preferred it over the previous-generation Opus 4.5.
- **Claude Opus 4.5 / Sonnet 4.5**(2025-11): A stable previous-generation fallback to use when the new version is unstable or cost is a concern.
- **Claude Haiku 4.5**(2025-10): A small, fast model with low latency and low cost, suited for large volumes of short tasks and background processing.

## Google Gemini Models

The Hyday settings page offers the following Gemini models by default:

- **Gemini 3.1 Pro (Preview)**: The latest reasoning-first flagship, with adaptive thinking, a 1M-token context, and integrated grounding.
- **Gemini 3.1 Flash Lite (Preview) / Gemini 3 Flash (Preview)**: The speed- and cost-oriented options in the 3.x series, well suited to high-volume chat and real-time interaction.
- **Gemini 2.5 Pro / 2.5 Flash**: The stable, well-validated previous-generation workhorses, with very large context windows and good for processing large note libraries.
- **Gemma 4 31B IT**: Google's open-weight model, callable directly in Hyday's API mode and also a good fit for self-hosting via Ollama.

> **ℹ️ Info**
> Hyday automatically rewrites the deprecated`gemini-3-pro-preview`(retired by Google on 2026-03-09) to`gemini-3.1-pro-preview`, so you don't have to migrate manually.

## Recommended Local Models (via Ollama)

The Hyday settings page offers the following local models by default (you can call any other model already pulled by Ollama via the`customModel`field):

- **Qwen 3 / Qwen 3-Coder**: Alibaba's open-source series, with strong Chinese support and coding capability.
- **Llama 3.1**: Meta's mainstream open-source choice, with the broadest ecosystem support.
- **DeepSeek V3.1**: Excellent at logical reasoning and Chinese-language tasks.
- **Mistral Small 3.2**: A leading European open-source option, balancing efficiency and quality.
- **Granite 4**: IBM's open-source series, enterprise-oriented and friendly for commercial licensing.

## Recommendations by Use Case

Use CaseRecommended ModelWhy**Everyday chat**Claude Haiku 4.5 / GPT-5-mini / Gemini 2.5 FlashA good balance of response speed and cost, ideal for general chat and lightweight Q&A.**Agent mode**GPT-5.5 / Claude Sonnet 4.6Best tool-calling reliability and long-horizon agentic performance.**Persona distillation**Claude Sonnet 4.6 / Gemini 3.1 Pro (recommended with a CLI backend)Supports six-dimensional web research and multi-stage synthesis; requires a stable search tool and long-context reasoning.**Privacy and offline processing**Ollama Qwen 3 / Llama 3.1 / DeepSeek V3.1Data never leaves the local machine, guaranteeing maximum privacy.**Code assistance**Claude Sonnet 4.6 / Claude Opus 4.7 / Qwen 3-CoderSonnet 4.6 offers the best price-to-performance; upgrade to Opus 4.7 for complex refactors or large-scale changes; use Qwen 3-Coder for offline coding.**Deep reasoning**GPT-5.5 Pro / o4-mini / Claude Opus 4.7For step-by-step math, logic puzzles, or debugging tasks, the reasoning / Pro tier models perform best.

> **ℹ️ Info**
> The model market evolves quickly. If a newly released model isn't in Hyday's default menu yet, use the`customModel`field on the settings page to manually enter the model ID and call it.
