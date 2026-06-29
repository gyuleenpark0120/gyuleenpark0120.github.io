---
layout: post
title: "LLMB: From Battery Papers to ML-Ready Databases"
date: 2025-09-30
description: An LLM agent extracted 8,074 cells worth of battery data from Li-MB literature: including figures, at 96.4% accuracy, then connected it directly to ML capacity prediction.
tags: [battery, LLM, text-mining, database, machine-learning, electrolyte]
categories: materials-ml
thumbnail: /assets/img/posts/llmb/pipeline-overview.png
---

<div class="paper-header">
  <div class="paper-badges">
    <span class="paper-venue-badge">ACS Central Science</span>
    <span class="paper-year-badge">2025</span>
  </div>
  <p class="paper-full-title">LLMB: Automated Battery Information Extraction and Database Construction Using Large Language Models</p>
  <p class="paper-tldr">Combined LLM text mining with a graph digitizer in an agent pipeline to extract 8,074 cells of battery component + cyclability data from Li-MB literature at 96.4% accuracy, then connected it to ML capacity prediction.</p>
</div>

<figure class="paper-figure">
  <img src="/assets/img/posts/llmb/pipeline-overview.png" alt="LLMB pipeline from papers to ML">
  <figcaption>End-to-end pipeline: LLM extraction → structured database → ML prediction. (LLMB, 2025)</figcaption>
</figure>

<div class="paper-what">
  <div class="paper-section-label">What this paper does</div>

An agent combining LLM-based text mining and a graph digitizer processes Li-MB literature to automatically extract battery material information. 29 entity categories. 8,074 cells. Component and cyclability database. 96.4% extraction accuracy.

What's distinctive is that it also extracts data from cycling graphs embedded in papers, not just the prose. The resulting structured database is then fed directly into ML models for battery capacity prediction, closing the loop from text to numerical prediction.

</div>

<div class="paper-takeaway">
  <div class="paper-section-label">Takeaway</div>
  <div class="takeaway-item">
    <span class="ti-marker">◆</span>
    <span>This paper connects what came before in this series: ML for battery data (Severson, Attia) and LLM for literature extraction (Dagdelen), merged into a single workflow: text extraction → structured database → ML prediction → experimental validation. That end-to-end integration is what makes it more than the sum of its parts. It's the direction I think the field is moving.</span>
  </div>
  <div class="takeaway-item">
    <span class="ti-marker">◇</span>
    <span>The graph digitizer part is actually the more interesting detail. Battery papers carry a lot of information in figures: cycling curves, EIS plots, SEM/TEM images, XRD patterns. Text extraction alone misses most of it. For AI systems targeting battery R&D to be genuinely useful, multimodal extraction (figures, tables, and text together) isn't optional; it's where the meaningful data lives.</span>
  </div>
</div>
