<div align="center">

# 🛸 agentic-underground

**Open tools and research for building software with AI agents** —<br>
disciplined workflows, safety, token efficiency, and reproducible model research.

[![On Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-agentic--underground-ffcc4d)](https://huggingface.co/agentic-underground)
[![Collection: PrattleNot](https://img.shields.io/badge/collection-PrattleNot-6366f1)](https://huggingface.co/collections/agentic-underground/prattlenot-6af7ac5e95e0fc80de563d61)
[![Live demo](https://img.shields.io/badge/demo-PrattleNot%20in%20your%20browser-a855f7)](https://agentic-underground.github.io/PrattleNot/)

</div>

---

## 🧱 What we build

| | Project | What it gives you | |
|:-:|:--|:--|:--|
| 🔀 | **[PrattleNot](https://github.com/agentic-underground/PrattleNot)** | An independent reproduction of [**LatentPort**](https://latentport.com/), Simon Villani's method, in Rust and WebAssembly: a small model reads the prompt, a fitted bridge translates its memory, and a larger model answers from it — sooner: up to **3.39×** faster to first token on LatentPort's own 4B → 27B pair, and **1.87×** on a new pair, running [in your browser](https://agentic-underground.github.io/PrattleNot/), carried to a five-times size gap (SmolLM2-360M → 1.7B), and to two more model families (Qwen3, Gemma 3) and a hybrid attention–recurrent model (Qwen3.5). | Rust · Apache-2.0 |
| 🏭 | **[idea-to-production](https://github.com/agentic-underground/idea-to-production)** | Eight composable Claude Code plugins that carry software from the spark of an idea to production in one test-first value flow: discover ▸ refine ▸ design ▸ build ▸ assure ▸ secure ▸ publish ▸ operate. | Shell · MIT or Apache-2.0 |
| 🛡️ | **[skillsentry](https://github.com/agentic-underground/skillsentry)** | A static auditor for AI-agent skills — read it *before* you run it. Point it at a skill or plugin and get a verdict with receipts, without executing anything it scans: `npx skillsentry <git-url \| dir>` | TypeScript · MIT |
| ⚖️ | **[token-fairness](https://github.com/agentic-underground/token-fairness)** | `tf`, a token-aware scheduler as one fast Rust binary and a Claude Code plugin: it estimates a job's cost before it fans out, gates every wave against the live rate-limit window, and checkpoints before the ceiling, so a usage limit is never exhausted by surprise. | Rust |

## 🤗 On Hugging Face

The weights we fit are published at **[huggingface.co/agentic-underground](https://huggingface.co/agentic-underground)**,
gathered in the **[PrattleNot collection](https://huggingface.co/collections/agentic-underground/prattlenot-6af7ac5e95e0fc80de563d61)**:
bridges between model pairs, each pinned by commit and measured by the harness in its source
repository. Start with [`smollm2-135m-to-360m-bridge`](https://huggingface.co/agentic-underground/smollm2-135m-to-360m-bridge),
which runs in your browser, then [`smollm2-360m-to-1.7b-bridge`](https://huggingface.co/agentic-underground/smollm2-360m-to-1.7b-bridge), across a larger gap, and
[`qwen3-0.6b-to-1.7b-bridge`](https://huggingface.co/agentic-underground/qwen3-0.6b-to-1.7b-bridge), the second family, and
[`gemma-3-270m-to-1b-bridge`](https://huggingface.co/agentic-underground/gemma-3-270m-to-1b-bridge), the third — gated, as a Gemma Model Derivative under the [Gemma Terms of Use](https://ai.google.dev/gemma/terms) — and
[`qwen3.5-0.8b-to-2b-bridge`](https://huggingface.co/agentic-underground/qwen3.5-0.8b-to-2b-bridge), a hybrid model whose recurrent state crosses as it is.

## 🔭 Projects we follow

We keep forks of projects we evaluate and use alongside our own. All credit belongs to their authors —
follow the upstream links for the real thing.

- **Token and context efficiency** — [headroom](https://github.com/headroomlabs-ai/headroom) (compresses
  tool output before it reaches the model) · [rtk](https://github.com/rtk-ai/rtk) (a CLI proxy that trims
  common dev-command output) · [lean-ctx](https://github.com/yvgude/lean-ctx) (a context layer for agents)
- **Agent workflow** — [agent-ways](https://github.com/aaronsb/agent-ways) (session state for agent
  "ways") · [autoresearch](https://github.com/karpathy/autoresearch) (agents running research on
  single-GPU training)
- **Workload context** — [swc](https://github.com/ctracey/swc) (sessionless workload context) ·
  [rkss_pattern](https://github.com/ctracey/rkss_pattern)

## How we work

- 🔬 **Reproducible** — a number we publish comes with the harness that produced it.
- ✅ **Test-first** — a feature starts as a failing test that describes where it is going.
- 🙏 **Attributed** — derivative work says so, loudly; PrattleNot is downstream of
  [LatentPort](https://latentport.com/) by Simon Villani.
