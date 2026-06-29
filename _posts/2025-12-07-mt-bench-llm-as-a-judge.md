---
layout: post
title: "MT-Bench & LLM-as-a-Judge"
date: 2025-12-07
description: Formalized the LLM-as-a-Judge paradigm for evaluating open-ended responses, showing over 85% agreement with human expert judgments.
tags: [evaluation, LLM-as-a-judge, benchmark]
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

**MMLU** (Hendrycks, 2020) tests knowledge with multiple-choice questions across 57 fields. GPT-3 scored 43% at release; frontier models now exceed 90%, basically saturated. But MMLU only works where there's a fixed correct answer. Writing, explaining, coding don't have that.

So how do you evaluate open-ended responses at scale without expensive human annotation? This paper's answer: let a strong LLM (GPT-4) be the judge. They built **MT-Bench** (80 multi-turn questions across 8 categories) and **Chatbot Arena** (real users voting on side-by-side responses), then showed GPT-4 as judge agreed with human expert ratings over 85% of the time. That agreement rate was the key result; it made the whole paradigm credible.

</div>

<div class="paper-takeaway">
  <div class="paper-section-label">Takeaway</div>
  <div class="takeaway-item">
    <span class="ti-marker">◆</span>
    <span>The "LLM evaluating LLM" structure is self-referential. GPT-4 exhibits real self-enhancement bias, favoring responses stylistically similar to its own, and that has to be taken seriously in benchmark design. Designing rubrics to account for exactly this bias was central to my own battery science evaluation work.</span>
  </div>
  <div class="takeaway-item">
    <span class="ti-marker">◇</span>
    <span>MMLU and MT-Bench are both improvements, but they're still general-domain benchmarks. For specialized work like battery science, you need ground truth from people who actually know the domain. That's what makes the evaluation problem genuinely hard.</span>
  </div>
</div>
