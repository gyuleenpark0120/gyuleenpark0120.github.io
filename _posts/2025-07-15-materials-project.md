---
layout: post
title: "The Materials Project: Data Infrastructure for Materials AI"
date: 2025-07-15
description: High-throughput DFT calculations on 150,000+ inorganic materials, freely released as an open database — the data foundation that made GNoME and most of materials AI possible.
tags: [materials-database, DFT, open-science, infrastructure, high-throughput]
categories: materials-ml
thumbnail: /assets/img/posts/materials-project/platform.png
---

<div class="paper-header">
  <div class="paper-badges">
    <span class="paper-venue-badge">APL Materials</span>
    <span class="paper-year-badge">2013</span>
    <a href="https://doi.org/10.1063/1.4812323" class="paper-link-badge" target="_blank">paper ↗</a>
  </div>
  <p class="paper-full-title">Commentary: The Materials Project: A materials genome approach to accelerating materials innovation</p>
  <p class="paper-tldr">Built a free, open database of 150,000+ inorganic materials with DFT-computed properties — the data infrastructure that underlies GNoME, the vast majority of materials ML research, and the modern materials genome initiative.</p>
</div>

<figure class="paper-figure">
  <img src="/assets/img/posts/materials-project/platform.png" alt="The Materials Project platform overview">
  <figcaption>The Materials Project platform and high-throughput computational workflow. (Jain et al., 2013, Figure 1)</figcaption>
</figure>

<div class="paper-what">
  <div class="paper-section-label">What this paper does</div>

For AI models like GNoME to train, they need data. The Materials Project created that data.

It ran high-throughput DFT simulations on tens of thousands of inorganic materials — computing crystal structure, formation energy, electronic properties, and more — and released everything as a free, open-access database. It now contains data on over 150,000 materials, and the vast majority of materials AI papers use it. The database started in 2013 made GNoME in 2023 possible.

</div>

<div class="paper-takeaway">
  <div class="paper-section-label">Takeaway</div>
  <div class="takeaway-item">
    <span class="ti-marker">◆</span>
    <span>This is infrastructure-as-science. The Materials Project didn't produce a single novel material on its own, but it enabled an entire research field to exist. Open data accelerated the field far more than any single closed result would have — the database is a public good in the truest sense.</span>
  </div>
  <div class="takeaway-item">
    <span class="ti-marker">◇</span>
    <span>The 10-year lag between 2013 and GNoME is a useful data point: ROI on scientific infrastructure is long-term and compounding. When designing AI systems for materials, the data layer deserves as much investment as the model architecture.</span>
  </div>
</div>
