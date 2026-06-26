---
layout: page
title: "Chemistry Knowledge Extraction – Unstructured Literature to Structured Records"
description: >
  Designed a reusable knowledge extraction framework converting unstructured chemistry
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

Unstructured scientific papers contain rich chemical knowledge – claimed molecules, experimental outcomes, mechanistic explanations, molecular properties – but this information is locked in heterogeneous free text that no ML model can directly consume. I designed a framework to systematically convert this literature into reusable, structured records, starting from battery chemistry and architected for extensibility across any molecule-centered chemistry domain.

---

## Contributions

**Reusable Extraction Schema**
Defined a five-category schema applicable across chemistry domains:

1. **Domain** (e.g., battery electrolyte, coolant, lubricant)
2. **Claimed molecule** (compound identity, IUPAC/common name, SMILES when available)
3. **Outcome** (performance results, quantitative metrics, comparative claims)
4. **Molecular information** (properties, safety data, DFT-derived descriptors)
5. **Context** (synthesis route, mechanism, experimental conditions)

The schema was designed so that any single-molecule chemistry domain can instantiate its own domain-specific subcategories on top of this backbone – enabling reuse without re-architecting.

**Auto Keyword Generation for Rapid Domain Bootstrapping**
When facing a 2-week deadline to build databases for two new domains (no domain scientists in-house), I reverse-engineered the logic behind human-curated positive/negative keyword sets and translated it into a few-shot prompt. The auto-generation system produced domain-specific POS/NEG keyword sets for retrieval, with two mitigation layers:

1. Sanity-checked against the existing battery keyword set (known-good reference)
2. Built a downstream relevance filter to catch any retrieval degradation post-deployment

Result: ~150k papers per domain bootstrapped in two weeks; both databases shipped to customers and trials initiated.

**RFT Training Data Pipeline**
Extended the extraction framework to produce RFT-ready structured data for a molecule recommendation model. Recognized that the prior approach (additive + performance label pairs) lacked the battery system context needed for user-tailored recommendations. Redesigned the data schema to include: (1) battery system information (anode, cathode), (2) mechanistic reasoning connecting molecule to performance, structured via a rule-based augmented reasoning prompt to ensure consistency across papers. Output: 1,342 structured entries across 465 unique additives – RFT-ready and accepted as a new team capability.

---

## Technical Highlights

`Structured Knowledge Extraction` `Molecule-Centered Schema Design` `Few-Shot Prompting` `RFT Data Pipeline` `Relevance Filtering` `Scientific Dataset Curation` `Domain-Generalizable Framework`
