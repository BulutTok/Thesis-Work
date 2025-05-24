# Thesis-Work Repository

Welcome to the **Thesis-Work** repository, which houses all of the code, data, and LaTeX source for Bulut Tok’s Master’s thesis on cost and performance optimization of GPT‑4O academic-advisor chatbots.

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
│   ├── figures/                   # All figures and diagrams
│   └── references/                # .bib files and bibliography
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

## 🚀 Getting Started

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

## 📧 Contact

* **Author:** Bulut Tok
* **Email:** [buluttok2013@gmail.com](mailto:buluttok2013@gmail.com)
* **Affiliation:** UNCW, MS in Computer & Information Science (ʹ25)

---

Feel free to explore each branch for focused development, raise issues, or contribute via pull requests. Good luck and happy researching! 🎓

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





**Enhancing Cost Efficiency and Performance of GPT-4O Chatbots: A Case Study on Academic Advisor Systems**

This repository contains the LaTeX source files for my **Master’s Thesis** and all associated code used for experimentation, data processing, and validation. The thesis investigates two GPT-4-based chatbot configurations (general-purpose vs. fine-tuned) for academic advising tasks, focusing on **token usage**, **computational costs**, and **domain-specific fine-tuning**.

> **Title of Thesis**  
> **ENHANCING COST EFFICIENCY AND PERFORMANCE OF GPT-4O CHATBOTS: A CASE STUDY ON ACADEMIC ADVISOR SYSTEMS**  
> **University of North Carolina Wilmington**  
> **Master of Degree in Computer Science and Information Systems**  
> *By Bulut Tok, 2025*

---

## Table of Contents
1. [Overview](#overview)  
2. [Repository Structure](#repository-structure)  
3. [Branches](#branches)  
   - [Question-based-LLM](#question-based-llm)  
   - [Thesis-Collation-Code](#thesis-collation-code)  
   - [IMDC-2023-CATALOG-Parsing-Code](#imdc-2023-catalog-parsing-code)  
   - [Training-and-Validation-Files](#training-and-validation-files)  
4. [Thesis Highlights](#thesis-highlights)  
5. [Getting Started](#getting-started)  
   - [Prerequisites](#prerequisites)  
   - [Installation](#installation)  
6. [Usage](#usage)  
   - [Compiling the Thesis (LaTeX)](#compiling-the-thesis-latex)  
   - [Running the Code](#running-the-code)  
7. [Data and Fine-Tuning](#data-and-fine-tuning)  
8. [Results and Evaluation](#results-and-evaluation)  
9. [Contributing](#contributing)  
10. [License](#license)  
11. [Contact](#contact)  

---

## Overview
This project explores **cost-efficiency** and **performance** optimizations in GPT-4O-based chatbots tailored for academic advising. The repository includes:

- **Thesis LaTeX Source** – Full write-up, figures, tables, and references.  
- **Code for Catalog Parsing** – Scripts to parse course data and produce JSON caches.  
- **Fine-Tuning and Training Scripts** – Python scripts and `.jsonl` files for GPT-4O fine-tuning.  
- **Validation and Analysis** – Jupyter notebooks or Python scripts used for testing output tokens, cost calculations, and final comparative analysis.  

---

## Repository Structure

A high-level look at the repository:

```
Thesis-Work/
├── README.md                  <-- You are here!
├── main.tex                   <-- Main LaTeX file for the thesis
├── chapters/                  <-- Chapter-wise LaTeX files
├── figures/                   <-- Figures, diagrams, images
├── references/                <-- .bib file(s) for bibliography
├── scripts/                   <-- Python scripts for data parsing, token analysis, etc.
└── ...
```

- **Branches**:  
  - *Question-based-LLM*  
  - *Thesis-Collation-Code*  
  - *IMDC-2023-CATALOG-Parsing-Code*  
  - *Training-and-Validation-Files*  

Use `git checkout <branch-name>` to switch among them.

---

## Branches

### Question-based-LLM
Contains code related to the question-by-question chatbot approach.  
- **Purpose**: Demonstrates how user queries are processed in a Q&A format, focusing on cost measurements for each question.  
- **Key Files**:  
  - `scripts/question_based_chatbot.py` – The main script for question-driven interactions.  
  - `analysis/token_calculations.ipynb` – A notebook that calculates per-question token usage.  

### Thesis-Collation-Code
Collects LaTeX files, figure references, and the final structure used to build the thesis PDF.  
- **Purpose**: This is the “master” branch for assembling the thesis text.  
- **Key Files**:  
  - `main.tex` – Main LaTeX file.  
  - `chapters/` – Contains `introduction.tex`, `methodology.tex`, etc.  
  - `figures/` – Figures used throughout the thesis.  

### IMDC-2023-CATALOG-Parsing-Code
Holds the scripts that parse the 2023 course catalog (or any relevant university course data) into JSON format.  
- **Purpose**: To transform raw PDF or HTML-based course listings into structured JSON data.  
- **Key Files**:  
  - `parse_catalog.py` – Python script that extracts course data from PDF/HTML.  
  - `catalog_cache.json` – Example JSON output for course info.  

### Training-and-Validation-Files
Stores the `.jsonl` files for training, validation, and fine-tuning of GPT-4O.  
- **Purpose**: Central location for your **fine-tuning** data and scripts.  
- **Key Files**:  
  - `training_data.jsonl` – Training examples for domain-specific customization.  
  - `validation_data.jsonl` – Held-out set for validation metrics.  
  - `fine_tune_script.py` – Example script to run the fine-tuning process via OpenAI’s API.  

---

## Thesis Highlights
1. **Comparative Analysis** – Evaluates a general-purpose GPT-4O vs. a domain-specific fine-tuned GPT-4O.  
2. **Cost & Token Usage** – Investigates how domain-specific fine-tuning can reduce tokens and thus operational costs.  
3. **Academic Advising Context** – Focuses on how chatbots can provide **degree audits**, **course recommendations**, and **personalized** academic advice.  
4. **Quantitative & Qualitative Metrics** – Employs token counts, cost analysis, and human evaluation (relevance, clarity) to measure performance.

---

## Getting Started

### Prerequisites
- **Python 3.8+**  
- **LaTeX Distribution** (e.g., TeX Live, MikTeX) for compiling the thesis  
- Libraries (install via `pip install -r requirements.txt`):
  - `PyPDF2`, `pandas`, `numpy`, `openai`, `tiktoken`, `nltk`, etc.  

### Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/YourUsername/Thesis-Work.git
   ```
2. **Navigate to the project directory**:
   ```bash
   cd Thesis-Work
   ```
3. **Set up a virtual environment** *(optional but recommended)*:
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/Mac
   venv\Scripts\activate     # Windows
   ```
4. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

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
3. The output PDF (e.g., `main.pdf`) should appear in the same directory.

### Running the Code

1. **Catalog Parsing** (IMDC-2023-CATALOG-Parsing-Code branch):  
   ```bash
   git checkout IMDC-2023-CATALOG-Parsing-Code
   python parse_catalog.py
   ```
   - This generates a structured JSON file of course data.

2. **Fine-Tuning** (Training-and-Validation-Files branch):  
   ```bash
   git checkout Training-and-Validation-Files
   python fine_tune_script.py --train_file training_data.jsonl --valid_file validation_data.jsonl
   ```
   - Adjust arguments as needed for your environment.

3. **Question-Based LLM** (Question-based-LLM branch):  
   ```bash
   git checkout Question-based-LLM
   python question_based_chatbot.py
   ```
   - Interactively ask academic advising questions, measure token usage, and compare costs.

---

## Data and Fine-Tuning
- **Fine-Tuning Data**: Found in `Training-and-Validation-Files` branch. Contains domain-specific Q&A examples in `.jsonl` format.  
- **Scripts**: Demonstrates how we upload data to OpenAI, parse logs for training loss, and compare the final fine-tuned model with the base GPT-4O model.

---

## Results and Evaluation
- **Token Usage**: Detailed logs for both base and fine-tuned models are saved in `.csv` or `.ipynb` files.  
- **Cost Analysis**: Compares input vs. output tokens and calculates cost with OpenAI’s pricing model.  
- **Evaluation Figures**: Plots, bar charts, and box-whisker diagrams found under `analysis/` or embedded in the thesis.

---

## Contributing
Contributions, suggestions, or bug reports are welcome!  

1. **Fork** the repository.  
2. **Create a new branch** for your feature/bugfix (`git checkout -b feature/YourFeature`).  
3. **Commit** your changes (`git commit -m 'Add feature'`).  
4. **Push** to your branch (`git push origin feature/YourFeature`).  
5. Open a **Pull Request** describing your changes.

Please ensure that any code or documentation adheres to the repository’s style guidelines.

---

## License
This project is licensed under the [MIT License](LICENSE). Feel free to modify or distribute, but please give appropriate credit and include the license in any derivative works.

---

## Contact
For questions, feedback, or further collaboration:
- **Name**: Bulut Tok  
- **Email**: [your.email@uncw.edu](mailto:bt6631.email@uncw.edu)  
- **GitHub**: [github.com/YourUsername](https://github.com/BulutTok)

---

*Thank you for checking out this project. I hope this helps other researchers, students, and developers explore how domain-specific fine-tuning can significantly optimize GPT-based chatbots—especially in academic advising scenarios.*
