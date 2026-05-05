---
title: "Reading Between the Tokens: Uncovering the Semantic Minima of AI Monologues"
event: "Linguistics Lunch, CLCG"
event_url: "https://www.rug.nl/research/clcg/colloquia_discussiongroups_linguisticevents/linguistics_lunch/"

location: Collaboratory A, Faculty of Arts, University of Groningen
address:
  city: Groningen
  country: The Netherlands

summary: >
  Invited talk at the CLCG Linguistics Lunch on identifying the load-bearing tokens in LLM Chain-of-Thought reasoning.

abstract: >
  To get modern AI models to solve difficult puzzles, we typically ask them to generate a "Chain of Thought" — a step-by-step written explanation of their reasoning. But is every word in that chain equally important? Beneath the fluent, highly articulate surface of AI text lies a deeply unequal distribution of meaning. Only a tiny fraction of the generated text carries the actual reasoning checkpoints, while the vast majority serves as connective tissue, maintaining discourse cohesion rather than propositional content. By mapping the model's internal states, we decode its own implicit representation of word importance. This gives us an "online detector" capable of identifying these crucial, load-bearing words in real time, exactly as the language is being produced. Remarkably, if you discard almost everything the AI says — erasing up to 95% of the monologue — the sparse, disjointed words left behind still perfectly predict the correct answer.

date: "2026-04-24T12:05:00Z"
date_end: "2026-04-24T12:30:00Z"
all_day: false

publishDate: "2026-04-24T00:00:00Z"

authors:
  - sara-candussio

tags:
  - Large Language Models
  - Interpretability
  - Chain of Thought
  - Invited Talk

featured: true

image:
  caption: ''
  focal_point: Right

url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""
---

Invited talk at the [CLCG Linguistics Lunch](https://www.rug.nl/research/clcg/colloquia_discussiongroups_linguisticevents/linguistics_lunch/) at the University of Groningen.

Chain-of-Thought prompting asks models to reason step by step — but most of what they write is filler. This talk presents work on identifying the semantic minima of AI reasoning: the tiny subset of tokens that actually carry predictive weight, detectable in real time from the model's internal states. Erasing up to 95% of the output leaves a sparse set of words that still perfectly predicts the correct answer.
