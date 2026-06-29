---
layout: post
title: "Searching for Ideal Electrolytes in the Molecular Universe"
date: 2025-07-22
description: 30 years of battery research explored ~700 electrolyte chemicals. The molecular universe contains ~10^60. SES AI built a 121-million-molecule DFT database and a battery-domain LLM to start closing that gap.
tags: [battery, electrolyte, molecular-discovery, AI-for-science, DFT, LLM]
categories: ai-for-science
thumbnail: /assets/img/posts/hannah2025/molecular-universe.png
---

<div class="paper-header">
  <div class="paper-badges">
    <span class="paper-venue-badge">ECS Interface</span>
    <span class="paper-year-badge">2025</span>
    <span class="paper-venue-badge" style="background: var(--global-theme-color); color: white;">My Team</span>
    <a href="https://doi.org/10.1149/2.F07252IF" class="paper-link-badge" target="_blank">paper ↗</a>
  </div>
  <p class="paper-full-title">Searching for Ideal Electrolytes in the Molecular Universe</p>
  <p class="paper-tldr">Battery researchers have explored ~700 unique electrolyte chemicals in 30 years. The molecular universe for electrolytes is ~10^60. SES AI built a 121-million-molecule DFT database and a battery-domain LLM to systematically search that space, producing AI-generated candidates that outperform human-designed formulations.</p>
</div>

<figure class="paper-figure">
  <img src="/assets/img/posts/hannah2025/molecular-universe.png" alt="Scale of molecular universe vs. explored electrolytes">
  <figcaption>The molecular universe dwarfs both explored electrolyte space and the number of stars in the observable universe. (Hannah et al., 2025, Fig. 1)</figcaption>
</figure>

<div class="paper-what">
  <div class="paper-section-label">What this paper does</div>

The number that anchors this paper: in 30 years of electrolyte research, battery scientists explored roughly 700 unique chemicals. The molecular universe for electrolytes (CNOSX elements, up to 30 heavy atoms) is estimated at ~10^60, larger than the total number of stars in the observable universe. Fewer unique molecules explored than stars in the Milky Way, against a chemical space bigger than the observable universe.

Three components make up the approach. First, DFT calculations accelerated ~10^5x over traditional CPU-based methods (GPU parallelism + ML force fields + ML inference), bringing 10^11 molecular property computations into the realm of feasibility. As of Q1 2025, a DFT database of 121 million molecules was built; the largest in the world. Second, molecular dynamics (MD) simulations predict solution-level properties: ion transport, solvation structure, conductivity. Third, a battery-domain LLM pretrained on published literature works in closed loop with the computational pipeline to identify and generate candidate molecules. AI-generated co-solvents and additives have already started outperforming human-designed electrolyte formulations in both LMBs and Si-based LIBs.

</div>

<div class="paper-takeaway">
  <div class="paper-section-label">Takeaway</div>
  <div class="takeaway-item">
    <span class="ti-marker">◆</span>
    <span>The "molecular universe" framing is genuinely useful, not just rhetorical. Electrolyte development has been bottlenecked less by effort than by sampling an impossibly narrow chemical space. The DFT database doesn't just enable better ML models; it reframes the problem from "optimize within what we know" to "explore what we haven't touched." That's a different kind of scientific progress.</span>
  </div>
  <div class="takeaway-item">
    <span class="ti-marker">◇</span>
    <span>My contribution was helping build out the database infrastructure. Separately, I was building Deepspace, a multi-agent system designed to reason over exactly this kind of database alongside the scientific literature. The computational pipeline described in this paper and the agentic reasoning layer are two sides of the same system: one generates the data, the other makes it queryable and interpretable at the level of scientific questions.</span>
  </div>
</div>
