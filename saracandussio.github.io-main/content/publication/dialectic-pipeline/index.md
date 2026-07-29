---
title: "A Dialectic Pipeline for Improving LLM Robustness"
authors:
  - sara-candussio
date: "2026-01-28T00:00:00Z"
doi: "https://doi.org/10.48550/arXiv.2601.20659"
publishDate: "2026-01-28T00:00:00Z"
publication_types: ["thesis"]
publication: "MSc Thesis, University of Trieste"
publication_short: "MSc Thesis"
abstract: >
  We propose a dialectic pipeline that preserves LLMs' generalization abilities while improving answer quality via self-dialogue, enabling the model to reflect upon and correct tentative wrong answers. The pipeline is tested across different datasets and model families, with all stages enriched with relevant context in an oracle-RAG setting.
summary: >
  A multi-agent self-dialogue pipeline for reducing hallucinations in LLMs without fine-tuning or domain-specific verifiers.
tags:
  - Large Language Models
  - Hallucination
  - Multi-Agent Systems
  - Question Answering
featured: false
links:
- name: arXiv page
  url: "https://arxiv.org/abs/2601.20659"
url_pdf: "https://arxiv.org/pdf/2601.20659.pdf"

image:
  caption: ''
  focal_point: ''
  preview_only: false
---

Can LLMs improve their accuracy without further training, just through a dialectic way of questioning themselves, as Hegel suggested?

This was the core question behind my Master's thesis. The short answer: **yes, and by a lot**.

## The Idea

Inspired by Hegelian dialectics, the pipeline structures reasoning into three stages:

{{< figure src="dialectic.png" caption="The thesis–antithesis–synthesis pipeline." >}}

1. **Thesis**: the model produces an initial answer given the question, context, and options.
2. **Antithesis**: the model challenges its own answer, now also seeing the thesis.
3. **Synthesis**: the model produces a final answer, having seen both thesis and antithesis.

No fine-tuning. No domain-specific verifiers. Just structured self-dialogue.

## Results

The pipeline was tested on multi-hop QA benchmarks (HotpotQA, WikiHop) across five open-source models under 20B parameters (Phi-mini, Phi-medium, Gemma-2B, Gemma-9B, LLaMA-8B).

{{< figure src="results-table.png" caption="Accuracy improvements across models on HotpotQA." >}}

{{< figure src="results-donut.png" caption="From 53.4% to 80.7% on HotpotQA with Phi-mini (+27.3%)." >}}

Improvements of **up to 30%** on complex multi-hop questions, beating standard Chain-of-Thought prompting.

{{< figure src="results-wikihop.png" caption="CoT vs. pipeline on WikiHop across all models." >}}

## Key Takeaways

- **Self-debating is the main driver**: letting models reflect on and contrast their own reasoning significantly boosts performance, especially as question complexity increases.
- **Instruction following matters**: models that strictly follow instructions (Llama, Phi) benefit more than those that get "too creative" (Gemma-2).
- **Smart filtering > summarization**: when dealing with long contexts, filtering for relevant information beats summarization, which can hurt deductive reasoning.
- **Avoid overthinking**: for simpler tasks, too much deliberation can introduce errors. A touch of "impulsivity" sometimes helps.

{{< figure src="results-context.png" caption="Original vs. summarized vs. filtered context on WikiHop." >}}

This work also received an **Honorable Mention at the Emanuele Pianta Award (AILC)** for the best Italian NLP Master's thesis at CLiC-it 2025. 🏆

{{< figure src="clicit.png" caption="CLiC-it 2025, Cagliari." >}}

If you're interested in agentic reasoning, small language models, or multi-hop QA, feel free to reach out!
