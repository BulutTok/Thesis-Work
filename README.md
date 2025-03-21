# Enhancing Cost Efficiency and Performance of GPT-4O Chatbots: A Case Study on Academic Advisor Systems

This repository contains the LaTeX source files for my **Master’s Thesis** and all associated code used for experimentation, data processing, and validation. The thesis investigates two GPT-4-based chatbot configurations (general-purpose vs. fine-tuned) for academic advising tasks, focusing on **token usage**, **computational costs**, and **domain-specific fine-tuning**.

> **Title of Thesis**  
> **ENHANCING COST EFFICIENCY AND PERFORMANCE OF GPT-4O CHATBOTS: A CASE STUDY ON ACADEMIC ADVISOR SYSTEMS**  
> **University of North Carolina Wilmington**  
> **Master of Science in Computer Science and Information Systems**  
> *By Bulut Tok, 2025*

---

## Table of Contents
1. [Overview](#overview)  
2. [Repository Structure](#repository-structure)  
3. [Branches](#branches)  
   - [main](#main)  
   - [Thesis-Work-Latex-Document](#thesis-work-latex-document)  
   - [Questions-Asked](#questions-asked)  
   - [Token-Calculation-Code](#token-calculation-code)  
   - [UNCW-2025-CATALOGUE-Parsing-Code](#uncw-2025-catalogue-parsing-code)  
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

- **Thesis LaTeX Source** – A single file, `main.tex`, which contains all sections of the thesis.  
- **Catalog Parsing Code** – Jupyter notebooks to parse course data and produce JSON caches.  
- **Fine-Tuning Scripts and Data** – Jupyter notebooks and `.jsonl` files for GPT-4O fine-tuning.  
- **Validation and Analysis** – Notebooks or Python scripts used for testing output tokens, cost calculations, and final comparative analysis.

---

## Repository Structure

A high-level look at the repository:

```
Thesis-Work/
├── README.md                   <-- This file
├── main.tex                    <-- Main LaTeX file with all sections of the thesis
├── chapters/                   <-- (Optional) If you split sections into separate .tex files
├── figures/                    <-- Figures, diagrams, images
├── references/                 <-- .bib file(s) for bibliography
├── scripts/                    <-- Python scripts or notebooks for data parsing, token analysis, etc.
└── ...
```





## Branches

### main
This branch includes the core Jupyter notebooks for both the **base model** and the **fine-tuned** GPT-4O model, as well as the primary data files:

- **Key Files**:
  - `Base Model.ipynb` – Demonstrates the usage of the base GPT-4O model for academic advising tasks.  
  - `Fine Tuning Code.ipynb` – Shows the fine-tuning process, including data loading and model updates.  
  - `CatalogParsing.ipynb` – Parses the UNCW 2025 course catalog (or similar) into a structured format.  
  - `Token_Calculations.ipynb` – Calculates token usage and estimates operational costs.  
  - `course_index_cache.json` – Cache file used by the chatbots to retrieve course information.  
  - `tarining1.jsonl` – Domain-specific training file for fine-tuning GPT-4O.  
  - `validation1.jsonl` – Validation dataset for performance evaluation.

### Thesis-Work-Latex-Document
Contains the LaTeX source for the thesis, including the main `main.tex` file (which has all sections). If you split out chapters, they would also reside here:

- **Key Files**:
  - `main.tex` – Main LaTeX file that includes all thesis sections.
  - `chapters/` – (Optional) Additional chapter files if needed.
  - `figures/` – Figures and diagrams used in the thesis.
  - `references/` – Bibliography files (`.bib`).

### Questions-Asked
Holds text files and examples used to test and validate chatbot performance. These files typically include identical questions and expected outputs.

### Token-Calculation-Code
Contains additional notebooks or scripts focused on calculating token usage and analyzing cost efficiency in detail.

- **Key Files**:
  - `token_calculation.ipynb` – Notebook that computes per-query token usage and cost.

### UNCW-2025-CATALOGUE-Parsing-Code
Contains a notebook or scripts dedicated to parsing the 2025 UNCW course catalog and preparing data for fine-tuning or other analyses.

- **Key Files**:
  - `CatalogParsing.ipynb` – Notebook that extracts course data from PDF/HTML sources and outputs JSON or CSV files.

### Training-and-Validation-Files
Stores the data and scripts related to GPT-4O fine-tuning, typically in `.jsonl` format.

- **Key Files**:
  - `tarining1.jsonl` – Domain-specific training examples for customization.
  - `validation1.jsonl` – Validation set for performance metrics.
  - `Fine Tuning Code.ipynb` – Notebook demonstrating how to run the fine-tuning process via OpenAI’s API.

---

## Thesis Highlights
1. **Comparative Analysis** – Evaluates a general-purpose GPT-4O vs. a domain-specific fine-tuned GPT-4O.  
2. **Cost & Token Usage** – Investigates how domain-specific fine-tuning can reduce token counts and operational costs.  
3. **Academic Advising Context** – Focuses on how chatbots can provide **degree audits**, **course recommendations**, and **personalized** academic advice.  
4. **Quantitative & Qualitative Metrics** – Employs token counts, cost analysis, and human evaluation (relevance, clarity) to measure performance.

---

## Getting Started

### Prerequisites
- **Python 3.8+**  
- **LaTeX Distribution** (e.g., TeX Live, MikTeX) for compiling the thesis  
- Python libraries (install via `pip install -r requirements.txt`), such as:  
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
1. Switch to the `Thesis-Work-Latex-Document` branch:
   ```bash
   git checkout Thesis-Work-Latex-Document
   ```
2. Compile using your preferred LaTeX tool (e.g., `pdflatex`, `xelatex`, or an IDE like TeXStudio):
   ```bash
   pdflatex main.tex
   bibtex main
   pdflatex main.tex
   pdflatex main.tex
   ```
3. The output PDF (e.g., `main.pdf`) will be generated in the same directory.

### Running the Code

1. **Main Branch**:
   - Open `Base Model.ipynb` in Jupyter to see how the base GPT-4O model is run.
   - Open `Fine Tuning Code.ipynb` in Jupyter to perform the fine-tuning steps.  
   - Ensure `course_index_cache.json` is present if your chatbot relies on it for course data.

2. **UNCW-2025-CATALOGUE-Parsing-Code**:
   ```bash
   git checkout UNCW-2025-CATALOGUE-Parsing-Code
   jupyter notebook CatalogParsing.ipynb
   ```
   - Adjust as needed to parse and export catalog data (e.g., to `course_index_cache.json`).

3. **Training-and-Validation-Files**:
   ```bash
   git checkout Training-and-Validation-Files
   jupyter notebook Fine\ Tuning\ Code.ipynb
   ```
   - This branch contains the `.jsonl` files (`tarining1.jsonl` and `validation1.jsonl`) for training and validation.

4. **Token-Calculation-Code**:
   ```bash
   git checkout Token-Calculation-Code
   jupyter notebook token_calculation.ipynb
   ```
   - A notebook for detailed token usage and cost analysis.

---

## Data and Fine-Tuning
- **Fine-Tuning Data**: Found in `Training-and-Validation-Files` (or in the main branch). The files are named `tarining1.jsonl` (training set) and `validation1.jsonl` (validation set).  
- **Scripts/Notebooks**: Demonstrates how to upload data to OpenAI, parse training logs, and compare the final fine-tuned model with the base GPT-4O model.

---

## Results and Evaluation
- **Token Usage**: Detailed logs and notebooks for both base and fine-tuned models.  
- **Cost Analysis**: Compares input vs. output tokens and calculates costs with OpenAI’s pricing model.  
- **Evaluation Figures**: Plots, bar charts, and box-whisker diagrams are either found in notebooks or embedded in the thesis.

---

## Contributing
Contributions, suggestions, or bug reports are welcome!

1. **Fork** the repository.  
2. **Create a new branch** for your feature/bugfix:
   ```bash
   git checkout -b feature/YourFeature
   ```
3. **Commit** your changes:
   ```bash
   git commit -m 'Add feature'
   ```
4. **Push** to your branch:
   ```bash
   git push origin feature/YourFeature
   ```
5. **Open a Pull Request** describing your changes.

Please ensure that any code or documentation adheres to the repository’s style guidelines.

---

## License
This project is licensed under the [MIT License](LICENSE). Feel free to modify or distribute, but please give appropriate credit and include the license in any derivative works.

---

## Contact
For questions, feedback, or further collaboration:
- **Name**: Bulut Tok  
- **Email**: [bt6631.email@uncw.edu](mailto:bt6631.email@uncw.edu)  
- **GitHub**: [github.com/BulutTok](https://github.com/BulutTok)

---

*Thank you for checking out this project. I hope this helps other researchers, students, and developers explore how domain-specific fine-tuning can significantly optimize GPT-based chatbots—especially in academic advising scenarios.*
```
