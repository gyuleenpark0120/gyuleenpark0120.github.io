---
layout: page
title: "Scientific Literature Pipeline"
description: >
  Developed a scientific literature ingestion pipeline for domain-specific corpus construction,
  with a focus on retrieval quality through structured keyword generation, LLM-based relevance
  filtering, and systematic metadata validation.
importance: 4
category: AI for Scientific Discovery
institution: SES AI
tags:
  - RAG Pipelines
  - Corpus Quality Control
  - Scientific Dataset Curation
  - Python
related_publications: false
---

## Overview

Building a domain-specific literature corpus for AI applications is not simply a matter of bulk retrieval. Decisions about query construction, relevance assessment, and metadata quality have compounding effects on what downstream systems can reliably do. This work focuses on those quality-oriented processes, treating corpus construction as a methodological problem rather than a data collection task.

---

## Contributions

**Structured Search Query Generation**
A system was developed to automatically generate domain-specific retrieval queries that encode meaningful distinctions between relevant and irrelevant content. This made retrieval consistent and reproducible across new domains without relying on manual keyword curation each time.

**LLM-Based Relevance Filtering**
A relevance filtering pipeline was built to determine whether retrieved papers belong to the target domain, particularly for large external corpora where metadata is noisy or incomplete. Model selection and input scope were chosen based on explicit recall-precision tradeoffs appropriate to the use case.

**Metadata Validation and Quality Control**
Systematic metadata inspection was incorporated to surface and address coverage gaps introduced by upstream data quality issues. The pipeline includes deduplication and document-level checks designed to ensure the corpus is usable for RAG, knowledge extraction, and model training.

---

## Technical Highlights

`Domain-Specific Corpus Construction` `Relevance Filtering` `Agentic Query Generation` `Metadata Validation` `Deduplication` `Corpus Quality Control` `RAG Infrastructure`
