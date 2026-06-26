---
layout: post
title: "Closed-Loop Optimization of Fast-Charging Protocols"
date: 2025-08-19
description: Bayesian optimization autonomously searched the fast-charging parameter space, cutting experimental time by 98% and identifying high-performance protocols from 224 candidates.
tags: [battery, bayesian-optimization, fast-charging, machine-learning, closed-loop]
categories: materials-ml
thumbnail: /assets/img/posts/attia/optimization-convergence.png
---

<div class="paper-header">
  <div class="paper-badges">
    <span class="paper-venue-badge">Nature</span>
    <span class="paper-year-badge">2020</span>
    <a href="https://doi.org/10.1038/s41586-020-1994-5" class="paper-link-badge" target="_blank">paper ↗</a>
  </div>
  <p class="paper-full-title">Closed-loop optimization of fast-charging protocols for batteries with machine learning</p>
  <p class="paper-tldr">Extended Severson's prediction framework into closed-loop optimization: Bayesian optimization autonomously iterated experiment design → test → feedback to find high-performance fast-charging protocols, cutting experimental time by 98%.</p>
</div>

<figure class="paper-figure">
  <img src="/assets/img/posts/attia/optimization-convergence.png" alt="Bayesian optimization convergence across protocols">
  <figcaption>Bayesian optimization converging on high-performance protocols from the 224-candidate search space. (Attia et al., 2020, Figure 2)</figcaption>
</figure>

<div class="paper-what">
  <div class="paper-section-label">What this paper does</div>

Severson predicted lifetime from early-cycle data. Attia goes one step further: have ML autonomously find the optimal charging protocol itself.

Bayesian optimization searches the 6-step fast-charging parameter space — automatically cycling through experiment design → test → incorporate results → next design. No human decisions between iterations. From 224 candidate protocols, it efficiently identified high-performance combinations. Result: 98% reduction in experimental time compared to conventional approaches.

</div>

<div class="paper-takeaway">
  <div class="paper-section-label">Takeaway</div>
  <div class="takeaway-item">
    <span class="ti-marker">◆</span>
    <span>If Severson is "prediction," this is "optimization." ML starts deciding the <em>what</em> of experiments — not just interpreting results, but directing the next step. That's a meaningful shift in the human–AI division of labor in research.</span>
  </div>
  <div class="takeaway-item">
    <span class="ti-marker">◇</span>
    <span>And yet the same gap remains: why this charging protocol performs better — what the electrochemical mechanism is — stays outside the model. To actually understand and improve the optimized protocol, you need mechanistic knowledge. That knowledge lives in papers, not in cycling data.</span>
  </div>
</div>
