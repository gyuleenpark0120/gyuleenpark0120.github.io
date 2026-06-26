---
layout: page
title: "Deepspace – Multi-Agent Scientific AI System"
description: >
  Architected an LLM-orchestrated multi-agent AI system for battery and materials R&D,
  enabling complex expert questions to be decomposed into coordinated workflows for
  literature retrieval, evidence synthesis, and traceable scientific reasoning.
  Achieved 6× latency reduction and launched as a core product feature.
importance: 1
category: AI for Scientific Discovery
tags:
  - Multi-Agent Systems
  - LLM API Integration
  - Scientific Dataset Curation
related_publications: false
---

## Overview

Deepspace is a multi-agent scientific AI system designed for battery and materials scientists. The goal was to move beyond a single-LLM chatbot toward a system that could coordinate specialized agents – each responsible for a distinct subtask – and synthesize their outputs into coherent, evidence-grounded answers to complex R&D questions.

I conceived and architected Deepspace at a time when agentic AI was in its early stages, identifying the paradigm as the right approach to leverage our large scientific literature corpus more intelligently.

---

## What I Built

**Agent Architecture Design**
Defined agent roles, instructions, tool use, and inter-agent interaction logic from scratch. The system decomposes an incoming R&D question into subtasks – literature retrieval, evidence synthesis, domain-specific reasoning – each handled by a task-specialized agent.

**Capability Roadmap**
Translated domain battery research needs into a prioritized expansion roadmap covering data analysis, visualization, literature-grounded reasoning, and domain-specific tool integration.

**Latency Optimization (2 hr → 20 min, 6×)**
Diagnosed the bottleneck at task level: identified parallelizable downstream tasks (e.g., literature retrieval vs. user-need extraction) and applied DAG-based parallelization. Then ablated at agent level – identified a supplementary-info agent whose output heavily overlapped with the main context and disabled it, recovering significant latency with minimal impact on answer quality. Validated the trade-off explicitly before shipping.

**Internal Evaluation and Launch**
Ran systematic internal scientist testing comparing Deepspace against the prior single-LLM baseline. Demonstrated improvements in evidence use, reasoning decomposition, and domain-grounded synthesis. Shipped to the product engineering team; Deepspace became the main feature of the next product version.

---

## Impact

- **6× end-to-end latency reduction** (2 hr → 20 min) without significant loss in answer quality
- **Product launch**: became a core feature; two major battery tech companies contacted the company after release
- Prompted company leadership to expand the LLM team (now ~15 scientists), directly attributable to Deepspace's reception
- Established the foundation for ongoing agentic AI development within the Battery-AI team

---

## Technical Highlights

`Multi-Agent Orchestration` `DAG-based Task Parallelization` `Tool-Use Design` `Agent-Level Ablation` `Prompt Optimization` `LLM-Orchestrated Workflows` `Scientific Reasoning`
