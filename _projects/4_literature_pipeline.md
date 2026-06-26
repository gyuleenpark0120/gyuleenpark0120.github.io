---
layout: page
title: "Scientific Literature Pipeline"
description: >
  Built and scaled a large-scale scientific literature ingestion pipeline from 20k to
  500k papers (25×) by diagnosing a systematic API coverage bottleneck through
  root-cause analysis and redesigning retrieval workflows with automated filtering,
  deduplication, and metadata validation.
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

A high-quality scientific corpus is the foundation for RAG-based AI systems, knowledge extraction, and model training. I owned the end-to-end literature ingestion pipeline – from retrieval architecture to quality validation – and systematically grew and improved it to serve as a reliable backbone for downstream AI workflows.

---

## What I Built

**Root-Cause Analysis: The API 1,000-Limit Bug**
While testing bulk retrieval, I noticed the pipeline consistently hitting a 1,000-result ceiling regardless of query scope. Initial hypothesis (over-constrained keyword filters) was tested and ruled out. Formed a new hypothesis: the API itself had a hidden coverage limit. Split the query by metadata (top 50 journals, quarterly) to circumvent it – and discovered a new anomaly: Q1 always hit 1,000 while other quarters returned random small counts (50–200). This pointed to a metadata quality issue: papers with missing date metadata were being bucketed into Q1. Confirmed via direct metadata inspection. Identified and implemented a replacement API with comprehensive metadata support and no retrieval cap.

**Pipeline Redesign and Scale-Up**
Rebuilt the bulk retrieval workflow from first principles. Implemented:

- Automated relevance filtering (LLM-based, with model and input-scope choices made on recall/cost/quality tradeoffs)
- Metadata validation and cleaning
- Deduplication against the existing database
- Document-level quality checks for downstream usability

**Relevance Filtering on Noisy External Data**
When tasked with processing ~500k papers from an external institution (mixed domains, messy metadata), built a filtering pipeline to extract target-domain papers. Made explicit tradeoffs: title+abstract input over title-only (quality first), selected the higher-recall model over the lower-cost one (recall matters more for database completeness). Found ~9k additional battery-domain papers not in the existing 20k database – a **45% increase** in known coverage.

**Structured Search Query Generation**
Designed an agentic query-generation system producing structured POS/NEG keyword queries tailored to the target retrieval API, enabling direct injection into the pipeline without manual intervention.

---

## Technical Highlights

`Large-Scale Literature Mining` `API Root-Cause Diagnosis` `Relevance Filtering` `Metadata Validation` `Deduplication` `Corpus Quality Control` `Agentic Query Generation` `RAG Infrastructure`
