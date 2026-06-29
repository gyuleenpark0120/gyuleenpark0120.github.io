---
layout: post
title: "Predicting Battery Lifetime Before It Declines"
date: 2025-08-05
description: Using only the first 100 cycles of voltage data, ML predicted final battery lifetime (150–2,300 cycles) with 9.1% test error — months before visible capacity fade.
tags: [battery, machine-learning, lifetime-prediction, electrochemistry, LFP]
categories: materials-ml
thumbnail: /assets/img/posts/severson/prediction-vs-actual.png
---

<div class="paper-header">
  <div class="paper-badges">
    <span class="paper-venue-badge">Nature Energy</span>
    <span class="paper-year-badge">2019</span>
    <a href="https://doi.org/10.1038/s41560-019-0356-8" class="paper-link-badge" target="_blank">paper ↗</a>
  </div>
  <p class="paper-full-title">Data-driven prediction of battery cycle life before capacity degradation</p>
  <p class="paper-tldr">Trained ML on voltage curve shapes from the first 100 fast-charge cycles to predict final lifetime across a 15x range — achieving 9.1% test error and reducing what once took months of cycling to an early-stage prediction.</p>
</div>

<figure class="paper-figure">
  <img src="/assets/img/posts/severson/prediction-vs-actual.png" alt="Predicted vs actual battery cycle life">
  <figcaption>Predicted vs. actual cycle life using early-cycle voltage features. (Severson et al., 2019, Figure 3)</figcaption>
</figure>

<div class="paper-what">
  <div class="paper-section-label">What this paper does</div>

124 LFP cells were fast-charged and cycled to end-of-life. The question: can you predict final lifetime (150 to 2,300 cycles) from the first 100 cycles alone, before capacity visibly declines?

The input is subtle: the change in the voltage discharge curve between cycle 10 and cycle 100. Invisible to the naked eye, but carrying early signatures of degradation already underway. ML picked up on this. Test error: 9.1%. What used to require months of cycling to evaluate could be predicted from early-stage data.

</div>

<div class="paper-takeaway">
  <div class="paper-section-label">Takeaway</div>
  <div class="takeaway-item">
    <span class="ti-marker">◆</span>
    <span>The convincing part isn't just the accuracy. The input feature is subtle: shape changes in voltage curves that look numerically fine to a human. The model was already distinguishing lifetimes in data I would have called unremarkable.</span>
  </div>
  <div class="takeaway-item">
    <span class="ti-marker">◇</span>
    <span>But the model doesn't explain why. Which degradation mechanism creates that voltage signal? ML found the pattern. Bridging that gap between data-driven prediction and mechanistic understanding is one of the core open problems in AI for battery development.</span>
  </div>
</div>
