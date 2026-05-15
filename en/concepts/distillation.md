---
locale: en
category: concepts
slug: distillation
source: src/content/docs/en/concepts/distillation.tsx
---
> *Persona distillation refines a person's**mental model, way of expressing themselves, and decision-making habits**into a runnable persona framework — so an AI can think, respond, and debate the way they would, on your behalf.*

## What Is Persona Distillation?

Most AI tools only let you switch tone or character prompts. Hyday's persona distillation goes much further. We run a 4-phase pipeline to extract a person's**cognitive structure**and assemble a persona file you can plug straight into Hyday Agent conversations and roundtable discussions.

Once distilled, you can use a persona to:

- Switch perspectives during a**Hyday Agent conversation**— for example, get the AI to respond the way Naval Ravikant, Morris Chang, or Feynman would think.
- Run a**roundtable**where multiple personas debate side by side, filling in the blind spots of any single viewpoint.
- Walk through a critical decision with a specific person first, to surface what you might be missing.

> **ℹ️ Info**
> Free users get access to 10 official Hyday personas they can switch between and chat with — free forever, no restrictions.Roundtable discussions and custom persona distillation are VVIP-only features. See[Plan Comparison](https://hyday.tw/docs/reference/plans).

## Distillation Inputs

To kick off a distillation you only need a small amount of information — the system handles the research:

- **Person's name**(required): for example*Richard Feynman*,*Morris Chang*, or*Naval Ravikant*.
- **Wikipedia link**(optional): speeds up the fact-checking in Phase 1.
- **Representative links**(optional, up to 3): their most defining interviews, talks, or publications.
- **Category**(optional): pick one of 10 categories like "Startup & Product" or "Learning & Knowledge", or leave blank and let the AI infer it.

## 4-Phase Distillation Pipeline

The full pipeline takes about**5 to 10 minutes**. It runs in the background, and you can stop it at any point.

### Phase 1: Six-Dimension Research

The AI searches the public web across six dimensions:

- **Writings**,**conversations**,**expression DNA**
- **External views**,**decisions**,**timeline**

If one dimension has noticeably thin public material, the AI marks it as**low evidence**and notes it in the final**honest boundaries**section.

### Phase 2: Synthesis

The six-dimension research gets compressed into a structured persona profile, including:

- **Mental models**: core thinking frameworks backed by cross-domain evidence.
- **Decision heuristics**: how they judge and trade off in real situations.
- **Expression DNA**: sentence structure, vocabulary, rhythm, humor, certainty levels, citation habits.
- **Values and anti-patterns**: what they pursue, what they reject, internal tensions.
- **Intellectual lineage**: who shaped them, who they shaped, where they sit in the history of ideas.
- **Signature quotes**and a**one-line essence**.

### Phase 3: Persona File Assembly

The structured profile from Phase 2 gets assembled into a complete markdown file.

### Phase 4: Quality Validation

Three test prompts verify the distillation quality:

- **Consistency check**: basic factual consistency.
- **Edge-case test**: does the persona still hold the person's judgment in edge scenarios?
- **Expression quality**: does the voice match the expression DNA from Phase 2?

## Why Do We Need Web Search?

Phase 1 has to run live research across six dimensions, so we**strongly recommend a CLI backend**(Claude Code, Gemini CLI, or Codex CLI) — these come with built-in search tools and work out of the box. If you go with an API backend, you'll need to configure a search tool separately, otherwise Phase 1 may not complete.

To pick the right CLI for you, see**Settings → AI → Functions → Persona distillation**.

## What Can You Do After Distillation?

- **Enable / disable**: manage all personas under "Settings → Persona distillation & management".
- **Edit**: fine-tune the system prompt manually or update the persona's avatar.
- **Switch perspectives mid-conversation**: swap personas anytime while chatting with Hyday Agent.
- **Roundtable**: invite multiple distilled personas to debate at the same table (VVIP).

## Privacy and Compute Cost

Persona distillation runs against**the AI provider you choose**, and only sends public data (the person's name and the links you provide) for research. Your notes are never uploaded. If you need maximum privacy, you can use local Ollama — but local models perform noticeably worse at six-dimension research and synthesis, which may cause Phase 1 to fail outright or drop the quality of the Phase 2 structure.

> **ℹ️ Info**
> Hyday's persona distillation pipeline is adapted from[nuwa-skill](https://github.com/alchaincyf/nuwa-skill)(Copyright © 2026 Huashu), used under the MIT license.

## Further Reading

- [Distillation Stalls or Fails](https://hyday.tw/docs/troubleshooting/distillation-stalls): common troubleshooting tips.
- [Agent Tool Reference](https://hyday.tw/docs/reference/agent-tools): how personas plug into Agent conversations.
- [Plan Comparison](https://hyday.tw/docs/reference/plans): VVIP entitlements in detail.
