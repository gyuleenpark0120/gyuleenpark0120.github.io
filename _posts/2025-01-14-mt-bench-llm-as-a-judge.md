---
layout: post
title: "MT-Bench & LLM-as-a-Judge"
date: 2025-01-14
description: Formalized the LLM-as-a-Judge paradigm for evaluating open-ended responses, showing over 85% agreement with human expert judgments.
tags: [evaluation, LLM-as-a-judge, benchmark, MMLU, chatbot-arena]
categories: evaluation
thumbnail: /assets/img/posts/mt-bench/judge-comparison.png
---

<div class="paper-header">
  <div class="paper-badges">
    <span class="paper-venue-badge">NeurIPS</span>
    <span class="paper-year-badge">2023</span>
    <a href="https://arxiv.org/abs/2306.05685" class="paper-link-badge" target="_blank">arxiv ↗</a>
  </div>
  <p class="paper-full-title">Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena</p>
  <p class="paper-tldr">Proposed using a strong LLM (GPT-4) as an automated judge for open-ended responses, alongside MT-Bench and Chatbot Arena as evaluation platforms — demonstrating >85% agreement with human expert ratings.</p>
</div>

<figure class="paper-figure">
  <img src="/assets/img/posts/mt-bench/judge-comparison.png" alt="LLM-as-a-judge vs human agreement">
  <figcaption>Agreement rates between LLM judge and human expert ratings across task categories. (Zheng et al., 2023)</figcaption>
</figure>

<div class="paper-what">
  <div class="paper-section-label">What this paper does</div>

Some context first. **MMLU** (Hendrycks, 2020) assembled 15,000+ multiple-choice questions across 57 fields — medicine, law, history, math, chemistry — to measure how much LLMs know. At release, GPT-3 scored 43%: better than chance, far from expert-level. It became the standard metric for LLM knowledge breadth. Today, frontier models exceed 90%, effectively saturating the benchmark.

But MMLU-style tests measure knowledge with fixed correct answers. The capabilities that actually matter for AI assistants — writing, explaining complex topics, coding — don't have single right answers. So how do you evaluate those?

This paper's answer: use a powerful LLM as the judge. Show GPT-4 two model responses side-by-side and have it pick the better one — no expensive large-scale human evaluation needed. They introduced **MT-Bench** (80 questions across 8 categories covering multi-turn conversation) and **Chatbot Arena** (users vote directly on which model they prefer). Using GPT-4 as judge, they found over 85% agreement with human ratings — the first systematic evidence that this approach actually works.

</div>

<div class="paper-takeaway">
  <div class="paper-section-label">Takeaway</div>
  <div class="takeaway-item">
    <span class="ti-marker">◆</span>
    <span>The "LLM evaluating LLM" structure is self-referential. GPT-4 exhibits real self-enhancement bias — favoring responses stylistically similar to its own — and this has to be taken seriously in benchmark design. Designing rubrics to account for exactly this bias was central to my own battery science evaluation work.</span>
  </div>
  <div class="takeaway-item">
    <span class="ti-marker">◇</span>
    <span>MMLU measures knowledge breadth well but correlates poorly with actual assistant quality. MT-Bench filled that gap. That said, MT-Bench is still limited to general domains — specialized fields like battery science or chemistry need purpose-built benchmarks with domain expert ground truth.</span>
  </div>
</div>
