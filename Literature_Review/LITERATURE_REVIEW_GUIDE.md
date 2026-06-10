# 🩺 Onboarding Guide: Literature Review Workflow for Clinical Code-Mixing Research

Welcome to the **Code Studio AI Research Lab**. This guide establishes the mandatory workflow for conducting the Literature Review for our project: **"Robustness and Reliance: How Bangla–English Code-Mixing Affects Clinical Language Models and the Clinicians Who Use Them"**.

---

## 🔍 1. Where to Find High-Impact Papers
This project sits at the intersection of Clinical NLP, Code-Switching, and Human-Computer Interaction (HCI). Search these specific venues:
* **Top NLP/AI Conferences:** **ACL**, **EMNLP**, **NAACL**, **COLING**.
* **Clinical NLP Workshops:** **BioNLP** (co-located with ACL), **JAMIA** (Journal of American Medical Informatics Association).
* **Human-AI Collaboration Venues:** **CHI** (ACM Conference on Human Factors in Computing Systems), **CSCW**.

---

## 🛠️ 2. Search Strategy & Keywords
Use advanced Boolean syntax to cross-reference these diverse fields:
* **Query 1:** `"Clinical NLP" AND ("Code-mixing" OR "Code-switching")`
* **Query 2:** `"Model robustness" AND "Linguistic perturbation" AND "Electronic Health Records"`
* **Query 3:** `"Automation bias" AND "Clinician reliance" AND "Large Language Models"`

---

## 📖 3. How to Read & Critically Evaluate a Code-Mixing Paper
1. **The Code-Mixing Metric:** Check if the paper used a formal linguistic metric like **CMI (Code-Mixing Index)** or **SPF (Switch Point Frequency)** to score the text.
2. **The Evaluation Task:** Did they evaluate simple tasks like Sentiment Analysis, or hard generative tasks like Clinical Summarization/Entity Extraction? 
3. **The Human Element Missing:** Did they test the model in a vacuum (purely looking at F1-scores), or did they study how *human experts* react to the model's errors? *Our biggest contribution is combining model evaluation with a clinician reliance study.*

---

## 📂 4. GitHub Directory Management Rules
```text
Clinical-Banglish-Robustness/
└── Literature_Review/
    ├── PDFs/                 # Store paper PDFs (Format: FirstAuthor_Year.pdf, e.g., Khan_2024.pdf)
    ├── BibTeX/               # Append raw BibTeX blocks to `citations.bib`
    └── Research_Matrix.md    # Update the markdown matrix table
