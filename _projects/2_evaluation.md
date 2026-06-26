---
layout: page
title: "LLM Evaluation Framework – Judge-Diagnose-Architect"
description: >
  Designed and deployed an automated evaluation system for open-ended scientific Q&A,
  achieving ~82% alignment with expert scores via iterative rubric optimization.
  Benchmarked frontier and internal LLMs on 2,390 real R&D questions;
  inter-annotator reliability confirmed at Krippendorff's α = 0.92.
importance: 2
category: AI for Scientific Discovery
tags:
  - LLM-as-a-Judge
  - Rubric Optimization
  - Multi-Dimensional Evaluation
  - Inter-Annotator Reliability
  - Scientific Benchmarking
related_publications: false
---

## Overview

Evaluating LLM responses to complex, open-ended scientific questions is fundamentally different from evaluating factual Q&A. There is no single correct answer, domain correctness requires expert judgment, and running manual human evaluation at every model update is not scalable. I designed a complete evaluation system to solve this problem – from rubric design through automated judge deployment through inter-annotator reliability certification.

---

## What I Built

**Judge-Diagnose-Architect: Iterative Rubric Optimization**
The core insight: rather than writing a rubric once and hoping it works, use an iterative LLM loop to automatically align the rubric to human scoring behavior.

- **Judge** scores a model response using the current rubric (outputs score + reasoning)
- **Diagnose** compares judge output to human gold (outputs a divergence report: where and why they differ)
- **Architect** reads the divergence report and updates the rubric (acts as optimizer)

This loop runs against a small human gold set, converging on a rubric that imitates human scoring tendency without requiring human effort at inference time.

**Multi-Dimensional Rubric Design**
Insisted on replacing a single 1–10 score with multi-dimensional criteria – factual correctness, evidence use, reasoning quality, domain specificity – enabling failure-mode diagnosis rather than just aggregate scoring.

**Human Gold Dataset Construction**
Earned cross-team trust to collect expert annotations. Ran weekly syncs explaining the value of human gold in the LLM evaluation era, which converted skeptical scientists into active annotators. Collected 32 calibration samples used for rubric optimization.

**Inter-Annotator Reliability (Krippendorff's α = 0.92)**
Pushed for measuring inter-annotator agreement despite initial pushback ("isn't this overkill?"). Argued that client-facing benchmark numbers require reliability evidence, and that downstream evaluation credibility depended on it. Implemented 8-sample overlap across 4 annotators; α = 0.92 confirmed strong consistency. This directly paid off in a client meeting where reliability was questioned.

**Benchmarking at Scale**
Deployed the optimized rubric to benchmark internal and frontier LLMs on 2,390 real-world R&D questions across battery and adjacent domains. Results used in product promotion and client demos.

---

## Impact

- **~82% alignment** with expert scores (normalized MAE complement) – model updates now evaluated in minutes vs. manual effort
- **Krippendorff's α = 0.92** – reliability metric that defended benchmark credibility in live client meetings
- Benchmark results on 2,390 real R&D questions actively used in product promotion
- Established the inter-annotator reliability step as standard protocol for all future human evaluations in the team

---

## Technical Highlights

`LLM-as-a-Judge` `Rubric Optimization` `Multi-Dimensional Evaluation` `Inter-Annotator Reliability` `Krippendorff's α` `Scientific Benchmarking` `Expert Evaluation Protocols` `Failure-Mode Diagnosis`
