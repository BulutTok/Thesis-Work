# Thesis-Work Repository

This repository contains the LaTeX source files for my **Master’s Thesis** and all associated code used for experimentation, data processing, and validation. The thesis investigates two GPT-4-based chatbot configurations (general-purpose vs. fine-tuned) for academic advising tasks, focusing on **token usage**, **computational costs**, and **domain-specific fine-tuning**.

> **Title of Thesis**  
> **ENHANCING COST EFFICIENCY AND PERFORMANCE OF GPT-4O CHATBOTS: A CASE STUDY ON ACADEMIC ADVISOR SYSTEMS**  
> **University of North Carolina Wilmington**  
> **Master of Degree in Computer Science and Information Systems**  
> *By Bulut Tok, 2025*

## Overview
This project explores **cost-efficiency** and **performance** optimizations in GPT-4O-based chatbots tailored for academic advising. The repository includes:

- **Thesis LaTeX Source** – Full write-up, figures, tables, and references.  
- **Code for Catalog Parsing** – Scripts to parse course data and produce JSON caches.  
- **Fine-Tuning and Training Scripts** – Python scripts and `.jsonl` files for GPT-4O fine-tuning.  
- **Validation and Analysis** – Jupyter notebooks or Python scripts used for testing output tokens, cost calculations, and final comparative analysis.


## Thesis Highlights
1. **Comparative Analysis** – Evaluates a general-purpose GPT-4O vs. a domain-specific fine-tuned GPT-4O.  
2. **Cost & Token Usage** – Investigates how domain-specific fine-tuning can reduce tokens and thus operational costs.  
3. **Academic Advising Context** – Focuses on how chatbots can provide **degree audits**, **course recommendations**, and **personalized** academic advice.  
4. **Quantitative & Qualitative Metrics** – Employs token counts, cost analysis, and human evaluation (relevance, clarity) to measure performance.

---  

## 📁 Repository Structure

```
Thesis-Work/
├── Base Model.ipynb               # Demo of the base GPT‑4O model
├── Fine Tuning Code.ipynb         # Notebook for the fine‑tuning pipeline
├── CatalogParsing.ipynb           # UNCW course catalogue parser
├── Token_Calculations.ipynb       # Token usage & cost estimator
├── course_index_cache.json        # Cache for course lookups
├── training1.jsonl                # Domain-specific training data
├── validation1.jsonl              # Validation dataset
├── Thesis-Work-Latex-Document/    # LaTeX source for the full thesis
│   ├── main.tex                   # Master document
│   ├── chapters/                  # Individual chapter files (if split)
│   ├── figures_current/                   # All figures and diagrams
│   └── references_thesis/                # .bib files and bibliography
├── Questions-Asked/               # Test prompts and expected answers
├── Token-Calculation-Code/        # Scripts & notebooks for deeper token analysis
├── UNCW-2025-CATALOGUE-Parsing-Code/  # Parsing code for course catalog
└── Training-and-Validation-Files/ # Supporting JSONL files for fine‑tuning
```

---

## 🌿 Branch Overview

* **main**: Core notebooks and data files (base model, fine‑tuning, parsing, token calculations).
* **Thesis-Work-Latex-Document**: All LaTeX source (main.tex, chapters, figures, references).
* **Questions-Asked**: Test suite of identical evaluation questions and expected outputs.
* **Token-Calculation-Code**: In‑depth analysis scripts for token usage and cost breakdowns.
* **UNCW-2025-CATALOGUE-Parsing-Code**: Course catalog extraction and transformation pipeline.
* **Training-and-Validation-Files**: JSONL files and notebooks for creating & validating fine‑tuning data.

---

### 🔍 Branch Details

#### Question-Based Chatbot (Question-Based-LLM)
Contains Jupyter notebooks for the question-by-question chatbot workflow.  
- **Purpose:** Processes user queries in a Q&A format while measuring per-question token usage and cost.  
- **Key Files:**  
  - `Question-Based-Chatbot.ipynb` — Main notebook for interactive, question-driven analysis.  
  - `Token_Calculations.ipynb`      — Notebook that computes token counts and per-question cost.  

#### Thesis Assembly Source (Thesis-Collation-Code)
Organizes LaTeX source files, figures, and bibliography for thesis compilation.  
- **Purpose:** Assembles the complete thesis into a single PDF document.  
- **Key Files:**  
  - `main.tex`                      — Master LaTeX file that includes all chapters.  
  - `chapters/`                     — Contains individual chapter files (e.g., `introduction.tex`, `methodology.tex`).  
  - `figures/`                      — Figures and diagrams used throughout the thesis.  

#### Catalog Parsing Notebooks (IMDC-2023-CATALOG-Parsing-Code)
Parses university course catalog data into structured JSON.  
- **Purpose:** Converts raw PDF/HTML course listings into clean, queryable JSON formats.  
- **Key Files:**  
  - `CatalogParsing.ipynb`          — Jupyter notebook for extracting and structuring course data.  
  - `course_index_cache.json`       — Example JSON cache of parsed course metadata.  

#### Fine-Tuning & Validation Data (Training-and-Validation-Files)
Stores training and validation datasets along with fine-tuning scripts.  
- **Purpose:** Supports domain-specific fine-tuning and performance evaluation of GPT-4O.  
- **Key Files:**  
  - `training1.jsonl`               — JSONL file with training examples for fine-tuning.  
  - `validation1.jsonl`             — JSONL file containing validation samples.  
  - `Fine Tuning Code.ipynb`        — Notebook illustrating the fine-tuning process via the OpenAI API.
  '''
---

##  Getting Started

1. **Clone the repository**

   ```bash
   git clone git@github.com:BulutTok/Thesis-Work.git
   cd Thesis-Work
   ```

2. **Switch to the branch you need**

   ```bash
   git checkout Thesis-Work-Latex-Document
   # or any other branch
   ```

3. **Install dependencies** (Python, Jupyter, LaTeX)

   ```bash
   pip install -r requirements.txt      # Notebook dependencies
   # Ensure a LaTeX distribution (TeX Live or MikTeX) is installed
   ```

4. **Work with notebooks**

   ```bash
   jupyter lab                          # Launch Jupyter Lab
   ```

5. **Compile the thesis PDF**

   ```bash
   cd Thesis-Work-Latex-Document
   pdflatex main.tex
   bibtex main
   pdflatex main.tex
   pdflatex main.tex
   ```

---



## 📊 Key Results

This section highlights quantitative findings from both the base and fine‑tuned GPT‑4O models, including per‑question token usage, cost comparisons, and scenario‑based savings.

### 10.1 Comparative Cost Efficiency of Base vs. Fine‑Tuned Models

| Metric                   | Base Model | Fine‑Tuned Model | Reduction (%) |
| ------------------------ | ---------- | ---------------- | ------------- |
| Total Output Tokens      | 39,353     | 26,960           | 31.5%         |
| Total Cost (USD)         | \$0.39353  | \$0.26960        | 31.5%         |
| Average Tokens per Q     | 3,935.3    | 2,696.0          | 31.5%         |
| Average Cost per Q (USD) | \$0.039353 | \$0.026960       | 31.5%         |

* **Response Consistency:** Box plots (Figure 10.1) show median output‑token counts per question dropping substantially after fine‑tuning (e.g., Q4 from \~460 to \~240 tokens, Q6 from \~300 to \~170) and interquartile ranges narrowing.
* **Per‑Question Efficiency:** Bar charts (Figure 10.2) illustrate consistent token reductions across all ten questions, with the largest gains in Q4 (−203.1 tokens), Q5 (−144.0 tokens), and Q10 (−180.5 tokens).
* **Cost Comparison:** Cost charts (Figure 10.3) reflect lower average per‑question spending for the fine‑tuned model (e.g., Q1: \$0.00302 → \$0.00239; Q4: \$0.00460 → \$0.00257).

### 10.2 Scenario‑Based Cost Savings Analysis

Using engagement rates from Georgia State University and projected queries for a 75‑student cohort (3.5 queries/user/month), we estimate:

| Month     | Active Users | Queries | Base Cost (USD) | Tuned Cost (USD) | Savings (USD) |
| --------- | ------------ | ------- | --------------- | ---------------- | ------------- |
| September | 30           | 105     | \$4.13          | \$2.83           | \$1.30        |
| October   | 25           | 88      | \$3.46          | \$2.37           | \$1.09        |
| November  | 35           | 123     | \$4.84          | \$3.32           | \$1.52        |
| December  | 20           | 70      | \$2.75          | \$1.89           | \$0.87        |
| **Total** | —            | **386** | **\$15.19**     | **\$10.41**      | **\$4.78**    |

* **Per‑Query Savings:** Average savings of \$0.01239 per query (31.5%).
* **Semester Impact:** Fine‑tuning yields \$4.78 saved over 386 queries—funds that can be redirected to human‑in‑the‑loop review or further enhancements.

These results demonstrate that domain‑specific fine‑tuning substantially reduces token usage and costs while improving response consistency, making it highly beneficial for scalable academic‑advising deployments.

## Evaluation
- **Token Usage**: Detailed logs for both base and fine-tuned models are saved in `.csv` or `.ipynb` files.  
- **Cost Analysis**: Compares input vs. output tokens and calculates cost with OpenAI’s pricing model.  
- **Evaluation Figures**: Plots, bar charts, and box-whisker diagrams  embedded in the thesis.

---

### Compiling the Thesis (LaTeX)
1. Go to the `Thesis-Collation-Code` branch:
   ```bash
   git checkout Thesis-Collation-Code
   ```
2. Compile using your preferred LaTeX tool (e.g., `pdflatex`, `xelatex`, or an IDE like TeXStudio):
   ```bash
   pdflatex main.tex
   bibtex main
   pdflatex main.tex
   pdflatex main.tex
   ```
3. The output PDF (e.g., `Thesis.pdf`) should appear in the same directory.


## Contributing
Contributions, suggestions, or bug reports are welcome!  

1. **Fork** the repository.  
2. **Create a new branch** for your feature/bugfix (`git checkout -b feature/YourFeature`).  
3. **Commit** your changes (`git commit -m 'Add feature'`).  
4. **Push** to your branch (`git push origin feature/YourFeature`).  
5. Open a **Pull Request** describing your changes.

Please ensure that any code or documentation adheres to the repository’s style guidelines.

---


* **Author:** Bulut Tok
* **Email:** [buluttok2013@gmail.com](mailto:buluttok2013@gmail.com)
* **Affiliation:** UNCW, MS in Computer & Information Science (ʹ25)

---

Feel free to explore each branch for focused development, raise issues, or contribute via pull requests. Good luck and happy researching! 🎓

---
