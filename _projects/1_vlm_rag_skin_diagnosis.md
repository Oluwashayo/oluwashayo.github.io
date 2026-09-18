---
layout: page
title: VLM-RAG skin disease diagnosis and information system
description: Fine-tuned vision–language model paired with retrieval-augmented generation grounded in dermatological text.
img: assets/img/projects/vlm_rag_skin_diagnosis.jpg
importance: 1
category: research
related_publications: true
---

This project develops an end-to-end clinical decision-support framework that fine-tunes a multimodal vision–language model (VLM) for skin lesion analysis and couples it with a domain-specific retrieval-augmented generation (RAG) layer. By grounding generative diagnostic responses in real-time clinical literature, trusted medical portals, and dermatological guidelines, the system mitigates hallucination risks and provides verifiable, evidence-backed diagnostic explanations.

The primary clinical motivation is addressing acute diagnostic disparities in dermatology—particularly in Sub-Saharan Africa, where specialist dermatologists are severely constrained, traditional diagnostics (skin scraping, biopsy) cause costly delays, and generalist AI models risk generating ungrounded or misleading advice.

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/projects/vlm_rag_skin_diagnosis.jpg" title="V-SIDS Interface Analysis Snapshot" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  The V-SIDS conversational interface synthesizing lesion image analysis, condition differential matching, concise treatment summaries, and clinical safety disclaimers.
</div>

### Technical Architecture & Methodology

- **Model & Adaptation**: Fine-tuned **LLaVA-1.5** using Low-Rank Adaptation (LoRA: rank 128, alpha 256) on the **HAM10000** dataset (10,015 dermatoscopic images across seven pigmented-lesion classes). Instruction–response pairs were auto-generated with **DeepSeek-VL2** to specialize the assistant for dermatological vision-language reasoning.
- **Dynamic Retrieval Layer**: Replaced static vector databases with live search via the **Tavily API**, restricted to a trusted-domain allow-list (World Health Organization, Mayo Clinic, WebMD, American Academy of Dermatology). The top three retrieved passages are dynamically injected into the inference prompt to anchor the diagnosis in factual clinical consensus.
- **Deployment**: End-to-end production pipeline comprising the fine-tuned model checkpoint hosted on Hugging Face, an asynchronous **FastAPI** inference backend, and an interactive **Next.js Progressive Web App (PWA)** frontend.

### Quantitative & Human Evaluation

- **Lesion Classification**: Reached a **macro-F1 score of 0.89** on a held-out 20% test split, exceeding the project's 0.80 benchmark target.
- **Hallucination Suppression**: Benchmarked against frontier proprietary models and architectural ablations: factual correctness rose from **0.80** (VLM only) to **0.88** (static RAG) to **0.94** (live web RAG), outperforming **GPT-4o (0.67)** and **Gemini 2.0 Flash (0.53)**.
- **Clinical Human Review**: In a 50-case evaluation on real volunteer photographs evaluated by two independent reviewers, the system achieved **0.94 factual correctness, 0.92 safety, 0.86 clarity, and 0.84 helpfulness**.
- **Current Limitation**: Because initial training relied on the dermatoscopic HAM10000 dataset, the system is primarily trained on lighter skin tones and is undergoing further validation for darker skin phenotypes.

This research served as Emmanuel's final-year undergraduate thesis at the Federal University of Technology Akure (FUTA) supervised by Olukemi Victoria Olatunde, and forms the foundation of two academic publications: {% cite olatunde2026integrated %} and {% cite olatunde2026development %}.
