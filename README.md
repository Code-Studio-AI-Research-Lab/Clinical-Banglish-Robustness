# Robustness and Reliance: How Bangla–English Code-Mixing Affects Clinical Language Models and the Clinicians Who Use Them

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Framework: PyTorch](https://img.shields.io/badge/Framework-PyTorch-orange.svg)](https://pytorch.org/)
[![Domain: Clinical NLP](https://img.shields.io/badge/Domain-Clinical%20NLP%20%26%20XAI-red.svg)]()

This repository contains the dataset generation pipelines, evaluation framework, and empirical analysis for **Robustness and Reliance**, a research initiative investigating the intersection of multi-lingual code-mixing (Bangla-English) and critical healthcare AI. Our study quantifies how syntactically mixed clinical notes (Banglish/Code-Mixed) degrade the performance of State-of-the-Art (SOTA) Clinical Language Models and evaluates the downstream cognitive reliance of clinicians who interact with these potentially flawed AI outputs.

---

## 📌 Research Vision & Core Concept
In non-Western clinical settings like Bangladesh, physicians rarely document patient histories in a single, pure language. Instead, they produce highly code-mixed notes containing a fusion of English medical terminology and Bangla symptomatic descriptions. This project addresses two critical unmapped vulnerabilities:
1.  **Model Robustness:** Assessing how severely standard clinical models (e.g., ClinicalBERT, Med-PaLM, Llama-3-Med) degrade when processing non-standard, code-mixed clinical syntax.
2.  **Human Reliance:** Conducting user-study simulations to measure whether clinicians over-rely (Automation Bias) or under-rely (Algorithm Aversion) on AI explanations when models are confused by code-mixed inputs.

---

## 🛠️ Key Features & Methodology
1. **Synthetic Code-Mixing Generator:** Algorithms using linguistic switching-point laws to automatically transform standard English/Bangla clinical notes into realistic code-mixed medical logs.
2. **Robustness Stress-Testing:** Evaluation suite measuring token-level prediction dropouts, Named Entity Recognition (NER) failures, and clinical question-answering degradation.
3. **Clinician Telemetry Framework:** Framework to log clinician interactions, decision shifts, and error-catching rates during specialized clinical UI simulations.
4. **Perplexity & Confusion Metrics:** Automated calculation of Cross-Lingual Perplexity to benchmark which transformer layers collapse under heavy code-mixing.

---

## 📂 Repository Structure
```text
├── src/
│   ├── generator/          # Code-mixing synthesis pipelines (Linguistic switching rules)
│   ├── evaluation/         # Robustness metrics, NER evaluation, and Perplexity logs
│   ├── models/             # Adapters and wrappers for base Clinical BERT/LLMs
│   └── user_study/         # Clinician interaction metrics and decision telemetry tools
├── data/                   # Anonymized synthetic datasets and evaluation benchmarks
├── configs/                # Mix-ratio parameters and tokenization setups
├── notebooks/              # Statistical graphs, error heatmaps, and reliance curves
├── Literature_Review/      # Team research matrices and BibTeX reference files
└── README.md
