---
layout: post
title: "Structured Information Extraction from Materials Science Papers"
date: 2025-09-16
description: Fine-tuned GPT-3 and Llama-2 to extract structured records from materials science text — demonstrating that LLMs can turn unstructured literature into queryable databases.
tags: [materials-science, information-extraction, LLM, NLP, knowledge-graph]
categories: materials-ml
thumbnail: /assets/img/posts/dagdelen/extraction-pipeline.png
---

<div class="paper-header">
  <div class="paper-badges">
    <span class="paper-venue-badge">Nature Communications</span>
    <span class="paper-year-badge">2024</span>
    <a href="https://arxiv.org/abs/2212.05238" class="paper-link-badge" target="_blank">arxiv ↗</a>
  </div>
  <p class="paper-full-title">Structured information extraction from scientific text with large language models</p>
  <p class="paper-tldr">Fine-tuned GPT-3 and Llama-2 to extract structured records — dopant-host links, MOF properties, composition/phase/application — from materials science text, outputting JSON at sentence and paragraph level.</p>
</div>

<figure class="paper-figure">
  <img src="/assets/img/posts/dagdelen/extraction-pipeline.png" alt="LLM-based structured extraction pipeline">
  <figcaption>Pipeline for LLM-based structured information extraction from scientific text. (Dagdelen et al., 2024, Figure 1)</figcaption>
</figure>

<div class="paper-what">
  <div class="paper-section-label">What this paper does</div>

Fine-tuned GPT-3 and Llama-2 on materials science literature to extract structured records from unstructured text. Three tasks were demonstrated: mapping dopant-host material relationships, cataloging metal-organic frameworks, and extracting composition/phase/morphology/application information. Processing happens at the sentence or paragraph level; output is JSON. Co-authors include Ceder, Persson, and Jain — the Materials Project team.

</div>

<div class="paper-takeaway">
  <div class="paper-section-label">Takeaway</div>
  <div class="takeaway-item">
    <span class="ti-marker">◆</span>
    <span>The first paper to rigorously demonstrate "paper text → structured data via LLM" in materials chemistry. This overlaps most directly with what I built at SES AI — same direction, applied to battery electrolyte chemistry. The approach differed: they used fine-tuning; I used few-shot prompting with iterative domain-specific schema refinement. Their output was general entity-relations; mine targeted structured records directly usable for downstream model training. Same problem, different engineering choices — and a useful lens for explaining why those choices matter.</span>
  </div>
  <div class="takeaway-item">
    <span class="ti-marker">◇</span>
    <span>The Materials Project co-authorship is not incidental. This is the same group that built the numerical database for inorganic materials — now extracting knowledge from text to complement it. The convergence of structured numerical data and structured textual knowledge is the long-term play.</span>
  </div>
</div>
