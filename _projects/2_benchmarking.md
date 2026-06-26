---
layout: page
title: "LLM Benchmarking Framework"
description: >
  Designed an automated evaluation framework for open-ended scientific Q&A,
  covering iterative rubric optimization, multi-dimensional scoring,
  and human gold dataset construction for automated scientific evaluation.
importance: 2
category: AI for Scientific Discovery
institution: SES AI
tags:
  - LLM-as-a-Judge
  - Scientific Benchmarking
  - Python
related_publications: false
---

## Overview

Evaluating LLM responses to open-ended scientific questions is fundamentally different from factual Q&A: there is no single correct answer, domain correctness requires expert judgment, and manual evaluation cannot keep pace with iterative model development. This work presents an automated evaluation framework covering rubric design, LLM-based judging, and human gold dataset construction.

---

## Contributions

**Iterative Rubric Optimization**
An LLM-in-the-loop pipeline was developed to iteratively refine evaluation rubrics against human scoring behavior. Rather than hand-crafting criteria once and hoping they generalize, the rubric is treated as an artifact that can be systematically improved toward expert alignment.

**Multi-Dimensional Rubric Design**
Scoring was structured across multiple criteria rather than a single aggregate score, making it possible to diagnose where and how a model falls short rather than just reporting an overall number.

**Human Gold Dataset Construction**
Expert annotations were collected as calibration data, providing a reliable reference for rubric optimization and benchmark validity.

**Benchmarking at Scale**
The optimized rubric was deployed to evaluate frontier and internal LLMs on a large set of real-world scientific R&D questions.

---

## Technical Highlights

`LLM-as-a-Judge` `Rubric Optimization` `Multi-Dimensional Evaluation` `Scientific Benchmarking` `Expert Evaluation Protocols` `Failure-Mode Diagnosis`
