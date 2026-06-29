---
layout: post
title: "What ML Can and Can't Tell You About Batteries"
date: 2025-09-03
description: ML predicts and optimizes. But the mechanistic understanding that makes battery research actually work lives in text. That's a structural gap pure data-driven approaches can't close.
tags: [battery, machine-learning, LLM, reflection, electrolyte, SEI]
categories: materials-ml
---

<div class="paper-header">
  <div class="paper-badges">
    <span class="paper-venue-badge">Reflection</span>
    <span class="paper-year-badge">2025</span>
  </div>
  <p class="paper-full-title">What ML Can and Can't Tell You About Batteries</p>
  <p class="paper-tldr">Severson predicts; Attia optimizes. But mechanistic understanding (the part that makes battery research actually progress) lives in the text of papers, not in cycling numbers. That's the structural gap pure data-driven approaches can't close.</p>
</div>

## What ML does well

Severson and Attia showed convincingly what's possible: electrochemical time-series data can predict lifetime and guide protocol optimization. The loop of numerical data → pattern recognition → prediction or decision works, and it works well. These aren't marginal improvements: 9.1% lifetime prediction error and 98% reduction in experimental time are real results.

## The thing that keeps nagging me

Battery research, especially electrolyte design, is different from what those papers tackled. The question isn't just "how long does this cell last?" It's _why_ it lasts that long. Why did this electrolyte form a stable SEI? How does the solvation shell structure influence the interphase? What does this particular additive actually do at the electrode surface?

During my PhD, I spent years on exactly these questions: XPS, Raman, NMR, post-mortem analysis, all trying to understand the mechanistic picture behind numbers that, on their face, just said "this one cycles better." The answer to _why_ almost always came from connecting your experimental results to what others had seen and proposed in the literature. The mechanistic insight was in the papers, not in the cycling data.

## The structural problem with pure data-driven approaches

Battery ML faces a version of this problem systematically:

<div class="paper-takeaway">
  <div class="paper-section-label">Three structural limitations</div>
  <div class="takeaway-item">
    <span class="ti-marker">◆</span>
    <span><strong>Data scarcity.</strong> How many datasets exist with the same cell chemistry, cycling conditions, and characterization? The numerical data that battery ML trains on is fragmented across labs, formats, and conditions. Nowhere near the scale of ImageNet or language data.</span>
  </div>
  <div class="takeaway-item">
    <span class="ti-marker">◇</span>
    <span><strong>Missing context.</strong> A voltage curve doesn't tell you what electrolyte was used, what the cell history was, or what degradation mechanism the authors suspected. That context exists; it's just in the paper text, not the numbers.</span>
  </div>
  <div class="takeaway-item">
    <span class="ti-marker">◇</span>
    <span><strong>Poor generalization.</strong> A model trained on LFP cells in one electrolyte system doesn't transfer cleanly to NMC cells in another. The mechanistic assumptions are different. Without those assumptions made explicit, the model is brittle.</span>
  </div>
</div>

All of this context (decades of experimental results, mechanistic interpretations, failure mode analyses) is accumulated in the scientific literature.

## The shift: LLM as the missing piece

LLMs changed this. For the first time, it became possible to systematically extract structured knowledge from paper text at scale. Not just keyword search, but genuine information extraction: what electrolyte, what additive, what SEI composition, what cycling performance, what mechanism was proposed.

The combination I think matters is: numerical data for finding patterns, text data for understanding what those patterns mean. When those two are connected, data-driven materials science can do something it couldn't before: not just predict from numbers, but reason from the accumulated knowledge of a field.
