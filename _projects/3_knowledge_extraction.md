---
layout: page
title: "Chemistry Knowledge Extraction – Unstructured Literature to Structured Records"
description: >
  Developed a reusable knowledge extraction framework converting unstructured chemistry
  literature into structured records of molecules, properties, mechanisms, and experimental
  context – extensible across chemistry domains for training data, molecular screening,
  and agentic tool use.
importance: 3
category: AI for Scientific Discovery
institution: SES AI
tags:
  - Knowledge Extraction
  - Scientific Dataset Curation
  - LLM Orchestration
  - Python
related_publications: false
---

## Overview

Scientific papers contain rich chemical knowledge, but that knowledge is locked in heterogeneous free text that downstream models cannot directly consume. This work presents a framework for converting chemistry literature into reusable structured records, starting from battery chemistry with a schema designed to generalize across molecule-centered domains.

---

## Contributions

**Reusable Extraction Schema**
The schema was designed around what is scientifically meaningful in molecule-centered chemistry: molecular identity, measured outcomes, relevant properties, and experimental context. The core structure is kept domain-agnostic, so domain-specific subcategories can be added without changing the underlying framework.

**Auto Keyword Generation for Rapid Domain Bootstrapping**
A few-shot prompting system was developed to automatically generate domain-specific retrieval keyword sets, enabling two new-domain databases to be built within two weeks.

**RFT Training Data Pipeline**
The extraction framework was extended to produce structured training data for a molecule recommendation model. The schema was redesigned to include richer context needed for domain-grounded recommendations, producing 1,342 structured entries across 465 unique additives.

---

## Technical Highlights

`Structured Knowledge Extraction` `Molecule-Centered Schema Design` `Few-Shot Prompting` `RFT Data Pipeline` `Relevance Filtering` `Scientific Dataset Curation` `Domain-Generalizable Framework`
