---
layout: post
title: "Attention Is All You Need"
date: 2025-03-18
description: Proposed the Transformer architecture using only attention — no RNNs — setting a new SOTA in machine translation and becoming the structural foundation for every modern LLM.
tags: [transformer, attention, NLP, deep-learning]
categories: foundations
# thumbnail: /assets/img/posts/attention/architecture.png
---

<div class="paper-header">
  <div class="paper-badges">
    <span class="paper-venue-badge">NeurIPS</span>
    <span class="paper-year-badge">2017</span>
    <a href="https://arxiv.org/abs/1706.03762" class="paper-link-badge" target="_blank">arxiv ↗</a>
  </div>
  <p class="paper-full-title">Attention Is All You Need</p>
  <p class="paper-tldr">Built a sequence model using only attention — no RNNs or CNNs — achieving state-of-the-art in machine translation and laying the structural foundation for GPT, BERT, and every modern LLM that followed.</p>
</div>

<figure class="paper-figure">
  <img src="/assets/img/posts/attention/architecture.png" alt="The Transformer model architecture">
  <figcaption>The Transformer model architecture. (Vaswani et al., 2017, Figure 1)</figcaption>
</figure>

<div class="paper-what">
  <div class="paper-section-label">What this paper does</div>

Before 2017, AI translation models processed sentences word by word, left to right. The longer the sentence, the more the model forgot earlier context. Words also couldn't be processed in parallel, making training slow.

The fix: drop sequential processing entirely and use only attention. Every word can simultaneously look at every other word. In "The cat sat on the mat because it was tired," the model connects "it" to "cat" by scanning the whole sentence at once. No sequential steps. Long-range relationships handled directly.

Result: faster training, better handling of long sentences, state-of-the-art translation at the time.

</div>

<div class="paper-takeaway">
  <div class="paper-section-label">Takeaway</div>
  <div class="takeaway-item">
    <span class="ti-marker">◆</span>
    <span>Self-attention solved both parallelization and long-range dependency at once. These were two problems RNNs couldn't structurally separate. Multi-head attention isn't just an ensemble trick; it lets the model learn different kinds of relationships (syntax, semantics, coreference) simultaneously in separate subspaces.</span>
  </div>
  <div class="takeaway-item">
    <span class="ti-marker">◇</span>
    <span>It started as a translation paper, but the architecture spread to vision (ViT), biology (AlphaFold), and chemistry. That level of universality was not obvious in 2017. The Transformer is now less a "model" and more the default substrate for any sequence-to-sequence problem.</span>
  </div>
</div>
