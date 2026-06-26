---
layout: page
title: "Multi-Agent AI Assistant for Scientific R&D"
description: >
  Architected an LLM-orchestrated multi-agent AI system (Deepspace) for battery and materials R&D,
  enabling complex expert questions to be decomposed into coordinated workflows across
  a scientific literature corpus and a millions-scale molecular properties database (DFT-computed)
  to accelerate molecule discovery. Achieved 6× latency reduction and launched as a core product feature.
importance: 1
category: AI for Scientific Discovery
institution: SES AI
tags:
  - Multi-Agent Systems
  - LLM Orchestration
  - Scientific Dataset Curation
related_publications: false
---

## Overview

[Deepspace](https://www.nasdaq.com/press-release/ses-ai-launches-agentic-capability-latest-molecular-universe-release-increase-value) is a multi-agent scientific AI system designed for battery and materials scientists. The goal was to move beyond a single-LLM chatbot toward a system that could coordinate specialized agents – each responsible for a distinct subtask – and synthesize their outputs into coherent, evidence-grounded answers to complex R&D questions.

The system operates over two complementary knowledge bases: a large scientific literature corpus and a millions-scale molecular properties database derived from DFT calculations. By grounding agent reasoning in both experimental evidence from literature and first-principles computed molecular descriptors, Deepspace was designed to accelerate molecule discovery workflows – helping scientists identify candidate materials faster than manual literature review or single-source querying alone.

I conceived and architected Deepspace at a time when agentic AI was in its early stages, identifying the paradigm as the right approach to leverage these heterogeneous scientific data sources more intelligently.

---

## Contributions

**Agent Architecture Design**
Defined agent roles, instructions, tool use, and inter-agent interaction logic from scratch. The system decomposes an incoming R&D question into subtasks – literature retrieval, molecular property lookup, evidence synthesis, domain-specific reasoning – each handled by a task-specialized agent operating over the appropriate data source (literature corpus or DFT-computed molecular database).

**Capability Roadmap**
Translated domain battery research needs into a prioritized expansion roadmap covering data analysis, visualization, literature-grounded reasoning, and domain-specific tool integration.

**Latency Optimization (2 hr → 20 min, 6×)**
Diagnosed the bottleneck at task level: identified parallelizable downstream tasks (e.g., literature retrieval vs. user-need extraction) and applied DAG-based parallelization. Then ablated at agent level – identified a supplementary-info agent whose output heavily overlapped with the main context and disabled it, recovering significant latency with minimal impact on answer quality. Validated the trade-off explicitly before shipping.

**Internal Evaluation and Launch**
Ran systematic internal scientist testing comparing Deepspace against the prior single-LLM baseline. Demonstrated improvements in evidence use, reasoning decomposition, and domain-grounded synthesis. Shipped to the product engineering team; Deepspace became the main feature of the next product version.

---

## Technical Highlights

`Multi-Agent Orchestration` `DAG-based Task Parallelization` `Tool-Use Design` `Agent-Level Ablation` `Prompt Optimization` `LLM-Orchestrated Workflows` `Scientific Reasoning` `DFT Molecular Database` `Molecule Discovery`
