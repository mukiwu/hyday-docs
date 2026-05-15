---
locale: en
category: troubleshooting
slug: distillation-stalls
source: src/content/docs/en/troubleshooting/distillation-stalls.tsx
---
> * If persona distillation takes forever, gets stuck at a particular phase, or produces a persona of obviously poor quality, follow this guide to diagnose and resolve the issue. *

## 1. Confirm the AI Backend Supports Web Search

Phase 1 of persona distillation requires **real-time web research across six dimensions**. Whether a search tool is available decides whether the whole process can run at all:

- **CLI backends are recommended** (Claude Code, Gemini CLI, Codex CLI): these ship with built-in search tools and work out of the box
- If you choose an API backend, you must configure a search tool separately, or Phase 1 will fail outright or produce vague content.

**Where to switch**: Settings → AI → Functions → Persona Distillation

## 2. Stuck on Phase 1 (Six-Dimension Research) for Too Long

Phase 1 searches the open web across six dimensions: works, conversations, expression, others' perspectives, decisions, and timeline. It normally takes 2 to 5 minutes. If it has been stuck for more than 10 minutes:

- **Check your network**: a CLI backend's search tool needs a stable external connection
- **Confirm the CLI tool is signed in**: for example, Claude Code requires `claude login` first
- **Verify how much public material exists about the subject**: very obscure people or those who only recently became public may cause search misses repeatedly, and the AI will note thin data in the "honest boundaries" section

## 3. The Generated Persona's Voice or Judgment Differs Substantially From the Real Person

In most cases this means Phase 1 didn't gather enough material to support Phase 2's synthesis:

- **Add a Wikipedia link**: this speeds up fact-checking and provides a stable biographical base
- **Provide representative links**: up to 3 URLs of this person's most representative interviews, talks, or writings
- **Specify categories**: for example, label Morris Chang as "Business and finance" or "Leadership and management" to keep the AI from inferring the wrong direction
- Review the **honest boundaries** section at the end of the persona file — the AI calls out which dimensions had thin data

## 4. The Local Ollama Backend Produces Low-Quality Output

Persona distillation demands strong search and reasoning capabilities. Small local models (7B–13B) typically struggle with:

- **Phase 1 fails outright**: most local models lack search tool integration, or their tool-call format is unstable
- **Phase 2 structural collapse**: mental models, decision heuristics, and the expression DNA can't be reliably produced
- **Phase 4 verification fails repeatedly**: the honest boundaries section fills up with weaknesses.

**What to do**: prefer a CLI backend or a high-tier cloud model for persona distillation. Local models can serve as the runtime backend for conversing with the finished persona later, but the distillation itself should run on the cloud.

## 5. Restarting After an Aborted Run

Distillation can be aborted at any time. Aborting won't leave a half-baked persona file behind (the persona file is only written in Phase 3). Just trigger it again, and consider:

- Pulling your previous inputs from **History** instead of retyping them
- Adjusting the Wikipedia link or representative links so the rerun's research is more stable

## 6. Diagnosing Persistent Failures

If the same subject keeps failing:

- Switch AI backends and try again (for example, from Gemini CLI to Claude Code)
- Run a smoke test with a **more internationally recognizable subject** (Steve Jobs, for instance) to confirm the backend and search tool work
- If the problem persists, open a GitHub Issue and include the **inputs** and the full Console error output

> **ℹ️ Info**
>  Persona distillation is a **heavyweight operation**. Depending on the backend's search speed and how much material exists about the subject, it usually takes 5 to 10 minutes. The job runs in the background, so you can keep writing notes — a toast notification will appear when it finishes.
