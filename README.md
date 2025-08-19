# Enhancing Cost Efficiency and Performance of GPT-4O Chatbots: A Case Study on Academic Advisor Systems

This repository contains the LaTeX source files for my **Master’s Thesis** and all associated code used for experimentation, data processing, and validation. The thesis investigates two GPT-4O-based chatbot configurations (general-purpose vs. fine-tuned) for academic advising tasks, focusing on **token usage**, **computational costs**, and **domain-specific fine-tuning**.

> **Title of Thesis**  
> **ENHANCING COST EFFICIENCY AND PERFORMANCE OF GPT-4O CHATBOTS: A CASE STUDY ON ACADEMIC ADVISOR SYSTEMS**  
> **University of North Carolina Wilmington**  
> **Master of Science in Computer Science and Information Systems**  
> *By Bulut Tok, 2025*

---

## 📑 Table of Contents
1. [Repository Structure](#repository-structure)  
2. [Overview](#overview)  
3. [Branch Details](#branch-details)
4. [Frontend](#frontend)
5. [Getting Started](#getting-started)  
6. [Contact](#contact)  
7. [Key Results](#key-results)  


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
  - 'index.html' - User interface
  

### Thesis-Work-Latex-Document
Contains the LaTeX source for the thesis, including the main `main.tex` file (which has all sections). If you split out chapters, they would also reside here:

- **Key Files**:
  - `main.tex` – Main LaTeX file that includes all thesis sections.
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

### Frontend 
This is a simple `index.html` file that works as the frontend for my Academic Advisor backend.  
It lets me chat with the advisor, upload PDFs, and see responses in a clean chat interface.

## How to use
1. Start the backend API (Flask) on `http://localhost:5000`.  
   Example: `python server.py` or `flask --app server run --port 5000`
2. Open `index.html` in a browser. That’s it.

## Notes
- Chat requests go to `/api/chat`  
- PDF uploads go to `/api/upload`  
- Session is saved in the browser so the conversation stays.

Super lightweight — just open and use.
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

## Key Results

This section highlights quantitative findings from both the base and fine-tuned GPT-4O models, including per-question token usage, cost comparisons, and scenario-based savings.

### 10.1 Comparative Cost Efficiency of Base vs. Fine-Tuned Models

| Metric                   | Base Model      | Fine-Tuned Model | Reduction (%)  |
|--------------------------|-----------------|------------------|----------------|
| Total Output Tokens      | 39,353          | 26,960           | 31.5%          |
| Total Cost (USD)         | $0.39353        | $0.26960         | 31.5%          |
| Average Tokens per Q     | 3,935.3         | 2,696.0          | 31.5%          |
| Average Cost per Q (USD) | $0.039353       | $0.026960        | 31.5%          |

- **Response Consistency:** Box plots show median output-token counts per question dropping substantially after fine-tuning (e.g., Q4 from ~460 to ~240 tokens, Q6 from ~300 to ~170) with narrower interquartile ranges.
- **Per-Question Efficiency:** Bar charts illustrate consistent token reductions across all ten questions, with the largest gains in Q4 (−203.1 tokens), Q5 (−144.0 tokens), and Q10 (−180.5 tokens).
- **Cost Comparison:** Cost charts reflect lower average per-question spending for the fine-tuned model (e.g., Q1: $0.00302 → $0.00239; Q4: $0.00460 → $0.00257).

### 10.2 Scenario-Based Cost Savings Analysis

Using engagement rates from Georgia State University and projected queries for a 75-student cohort (3.5 queries/user/month), we estimate:

| Month     | Active Users | Queries | Base Cost (USD) | Tuned Cost (USD) | Savings (USD) |
|-----------|--------------|---------|-----------------|------------------|---------------|
| September | 30           | 105     | $4.13           | $2.83            | $1.30         |
| October   | 25           | 88      | $3.46           | $2.37            | $1.09         |
| November  | 35           | 123     | $4.84           | $3.32            | $1.52         |
| December  | 20           | 70      | $2.75           | $1.89            | $0.87         |
| **Total** | —            | **386** | **$15.19**      | **$10.41**       | **$4.78**     |

- **Per-Query Savings:** Average savings of \$0.01239 per query (31.5%).
- **Semester Impact:** Fine-tuning yields \$4.78 saved over 386 queries—funds that can be redirected to human-in-the-loop review or further enhancements.

These results demonstrate that domain-specific fine-tuning substantially reduces token usage and costs while improving response consistency, making it highly beneficial for scalable academic-advising deployments.


## Evaluation
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
- **Email**: [buluttok2013@gmail.com](mailto:buluttok2013@gmail.com)  
- **GitHub**: [github.com/BulutTok](https://github.com/BulutTok)

---

*Thank you for checking out this project. I hope this helps other researchers, students, and developers explore how domain-specific fine-tuning can significantly optimize GPT-based chatbots—especially in academic advising scenarios.*
```
