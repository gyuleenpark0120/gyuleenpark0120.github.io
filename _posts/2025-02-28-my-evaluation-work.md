---
layout: post
title: "Evaluating LLMs on Battery Science Q&A"
date: 2025-02-28
description: Built a Judge-Diagnose-Architect rubric optimization loop achieving ~82% agreement with 32 battery scientists across 2,390 real R&D questions.
tags: [evaluation, LLM-as-a-judge, rubric, battery-science, scientific-benchmarking]
categories: evaluation
---

<div class="paper-header">
  <div class="paper-badges">
    <span class="paper-venue-badge">My Work</span>
    <span class="paper-year-badge">2025</span>
  </div>
  <p class="paper-full-title">Domain-Specific LLM Evaluation for Battery Science: A Judge-Diagnose-Architect Framework</p>
  <p class="paper-tldr">Used ratings from 32 battery scientists as ground truth to iteratively optimize an LLM judge rubric — achieving ~82% agreement and Krippendorff's α = 0.92 across 2,390 real R&D questions.</p>
</div>

<div class="paper-what">
  <div class="paper-section-label">What I built</div>

MMLU requires fixed answers. MT-Bench evaluates general assistants. But evaluating whether an LLM "correctly explained the SEI formation mechanism in lithium battery electrolytes while synthesizing relevant evidence" requires neither — there's no single correct answer, and without domain expertise you can't even tell if a response is good.

To fill this gap, I built a **Judge-Diagnose-Architect** iterative rubric optimization loop. An LLM judge scores responses; those scores are compared against expert human ratings to identify where and why they diverge; the rubric is revised accordingly — and repeated. I optimized a 4-dimension rubric against ratings from 32 battery scientists on 2,390 real R&D questions:

- **Factual correctness** — is the technical information accurate?
- **Evidence use** — are relevant literature and data appropriately cited?
- **Reasoning quality** — is the logical structure sound?
- **Domain specificity** — does the response engage with electrochemistry and materials science context?
</div>

<div class="paper-takeaway">
  <div class="paper-section-label">Takeaway</div>
  <div class="takeaway-item">
    <span class="ti-marker">◆</span>
    <span>Rubric quality determines judge quality. With the initial rubric, agreement with human experts was around 60%. After three iterations of the Judge-Diagnose-Architect loop, it reached 82%. Which model to use as judge mattered less than how the rubric was designed.</span>
  </div>
  <div class="takeaway-item">
    <span class="ti-marker">◇</span>
    <span>Domain-specific evaluation fundamentally requires human ground truth from people who know the domain. Recruiting 32 experts, aligning their scoring criteria, and verifying inter-rater reliability (Krippendorff's α = 0.92) was as important as any model design decision.</span>
  </div>
</div>
