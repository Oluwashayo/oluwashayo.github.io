---
layout: page
title: VLM-RAG skin disease diagnosis and information system
description: Fine-tuned vision–language model paired with retrieval-augmented generation grounded in dermatological text.
img: assets/img/projects/vlm_rag_skin_diagnosis.jpg
importance: 1
category: research
related_publications: true
---

This project develops an end-to-end clinical decision-support framework that fine-tunes a multimodal vision–language model (VLM) for skin lesion analysis and couples it with a domain-specific retrieval-augmented generation (RAG) layer. By grounding generative diagnostic responses in indexed clinical literature, textbooks, and dermatological guidelines, the system mitigates hallucination risks and provides verifiable, evidence-backed diagnostic explanations.

The core motivation is addressing diagnostic disparities in dermatology, particularly across diverse skin tones where traditional computer vision models frequently suffer performance degradation. The multimodal pipeline processes clinical lesion imagery alongside patient history, querying an external vector knowledge base to synthesize structured diagnostic summaries with referenced differential diagnoses.

This research served as Emmanuel's final-year undergraduate thesis at the Federal University of Technology Akure (FUTA) and forms the foundation of two 2026 academic publications with supervisor Olukemi Victoria Olatunde: {% cite olatunde2026integrated %} and {% cite olatunde2026development %}.

<!-- TODO(shayo) — datasets used, base model checkpoint, evaluation metric and result, repo link -->
