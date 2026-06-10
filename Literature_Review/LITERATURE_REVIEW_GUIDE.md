# 🩺 Onboarding Guide: Literature Review & Research Matrix for Clinical Code-Mixing & Robustness

Welcome to the **Code Studio AI Research Lab**. This guide outlines the mandatory workflow, literature logging standards, and Git guidelines for all team members working on our project: **"Robustness and Reliance: How Bangla–English Code-Mixing Affects Clinical Language Models and the Clinicians Who Use Them"**.

---

## 🔍 1. Where to Find High-Impact Papers
This project is highly interdisciplinary, blending Clinical NLP, Code-Switching, and Human-Computer Interaction (HCI). Do not use casual search engines; search exclusively on:
* **Google Scholar:** [scholar.google.com](https://scholar.google.com/) (Filter: *Since 2024/2025* for recent LLM evaluation metrics under code-mixing).
* **Top NLP Venues:** **ACL**, **EMNLP**, **NAACL**, and the specialized **BioNLP Workshop** (the gold standard for clinical text mining).
* **Medical Informatics Journals:** *JAMIA (Journal of the American Medical Informatics Association)* and *JMIR (Journal of Medical Internet Research)*.
* **Human-AI Collaboration Venues:** **CHI** and **CSCW** (to understand how doctors or professionals develop automation bias).

---

## 🛠️ 2. Advanced Search Queries & Operators
To find papers combining multi-lingual behavior with clinical safety, use these precise **Boolean Operators** (`AND`, `OR`, `""`):
* **Core Code-Mixing Query:** `"Clinical NLP" AND ("Code-mixing" OR "Code-switching" OR "Multilingual")`
* **Model Robustness Query:** `"Model robustness" AND "Linguistic perturbation" AND "Electronic Health Records"`
* **Human Reliance Query:** `("Automation bias" OR "Algorithm aversion") AND "Clinician reliance" AND "Large Language Models"`

---

## 📖 3. How to Read & Critically Evaluate a Paper
Clinical NLP requires a balanced critique of both language structures and human safety. Follow the **Three-Pass Method** and analyze:
1.  **Linguistic Metric Used:** Look at how the authors quantify mixed text. Did they use the **CMI (Code-Mixing Index)** or **SPF (Switch Point Frequency)**? We need to use these standards.
2.  **The Sub-word Tokenization Failure:** Look at their tokenization analysis. Did their WordPiece or BPE tokenizer break down mixed medical terms into meaningless fragments? *This is a core vulnerability we are targeting.*
3.  **The Human Element (The Gap):** Did the paper evaluate the model strictly using automated scores (F1, BLEU, Perplexity), or did they test how real-world clinicians make decisions when the model fails? *Our biggest competitive advantage is measuring downstream clinician reliance.*

---

## 📊 4. Maintaining the Central Research Matrix Table
Every paper you read must be logged immediately into `Literature_Review/Research_Matrix.md`. This table maps our collective research and prevents any duplicate work.

### The Matrix Format:
| Citation & Venue | Evaluation Objective | Language Pairs & Domain | Robustness Stress-Testing Method | Key Performance Drops | Found Limitations & Gaps (Our Opportunity) | Reviewer Name |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| *e.g., Khan et al., 2024 (EMNLP)* | Benchmark code-mixed sentiment analysis. | Bangla-English (Banglish) on Social Media. | Token probing and zero-shot LLM prompts. | F1-Score dropped by 35% under high mixing indexes. | Focused entirely on casual social media text (Tweets); did not touch high-stakes, structured clinical logs or medical syntax. | Rahim |
| **[Your Entry]** | | | | | | Your Name |

### How to add your entry:
1. Open `Literature_Review/Research_Matrix.md` in your text/code editor.
2. Scroll to the bottom of the table and add a new row using pipe (`|`) boundaries.
3. Write strictly in technical English and keep sentences point-wise.

---

## ✍️ 5. Writing the Literature Review Snippet (For LaTeX)
For every entry in the table, write a highly structured 4-sentence summary:
1.  **Sentence 1 (The Hook):** Mention the venue, authors, and objective. *(e.g., "In BioNLP 2024, Smith et al. evaluated the robustness of clinical transformers under syntactically perturbed inputs." )*
2.  **Sentence 2 (The Approach):** Detail their core evaluation framework. *(e.g., "They introduced a rule-based perturbation engine to inject spelling variants and dialectal shifts into standard electronic health records (EHR)." )*
3.  **Sentence 3 (The Discovery):** State their core failure metrics. *(e.g., "Their experiments revealed a 28% collapse in Named Entity Recognition (NER) accuracy when processing localized symptoms." )*
4.  **Sentence 4 (The Core Flaw):** Identify the gap our lab will exploit. *(e.g., "However, their framework was tested exclusively on monolingual Spanish-English corpora and lacks any mechanism to evaluate how expert clinicians adjust their reliance when exposed to these faulty model predictions." )*

---

## 📂 6. GitHub Directory Structure & Collaborative Git Rules
To avoid merge conflicts and maintain code cleanliness, adhere strictly to these repository rules:

### Folder Architecture:
```text
Clinical-Banglish-Robustness/
└── Literature_Review/
    ├── PDFs/                 # Store downloaded paper PDFs here
    │   └── Format: FirstAuthor_Year.pdf (e.g., Khan_2024.pdf)
    ├── BibTeX/               # Raw BibTeX snippets for LaTeX compilation
    │   └── citations.bib     # Open and append your BibTeX blocks here
    └── Research_Matrix.md    # The central markdown table file
