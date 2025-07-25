# ALAS1 Gene Expression and Read Count Analysis Mini-Projects

This repository contains two Jupyter Notebook-based mini-projects analyzing **ALAS1 gene expression levels** and **read counts** across strains, using a 1000-row RNA-Seq dataset sourced from the Bgee database. As a Biochemistry graduate (Second Class Upper), I’m pursuing a machine learning (ML) developer path with a focus on bioinformatics. These projects compute a combined expression metric by normalizing and averaging `Expression level` and `Read count` columns to identify the strain with the highest expression, relevant to heme biosynthesis studies. The Jupyter Notebook format enables interactive data exploration and visualization, ideal for sharing with the bioinformatics community.

## Project Overview

### 1. ALAS1 Expression Analyzer
- **Description**: A Jupyter Notebook analyzing ALAS1 gene expression levels and read counts across strains (e.g., HeLa, HepG2, MCF7 cell lines) from a 1000-row dataset. It normalizes the `Expression level` and `Read count` columns using min-max scaling, computes a combined expression metric (`Expression_combined`), calculates statistics (mean, median, standard deviation, max, min), and visualizes the distribution using a histogram. The strain with the highest combined expression is identified.
- **Purpose**: Demonstrates interactive data manipulation and visualization with Pandas and Matplotlib, preparing biochemical data for ML preprocessing in bioinformatics.
- **Files**:
  - `alas1_expression_analyser.ipynb`: Jupyter Notebook for analysis and visualization.
  - `alas1_expression_data.csv`: 1000-row dataset with `Gene name,Expression level,Read count,Strain,Time_min,Expression_combined`.
  - `alas1_expression_distribution.png`: Histogram of combined expression distribution.
  - `requirements.txt`: Python library dependencies.

### 2. ALAS1 Read Count Visualizer
- **Description**: A Jupyter Notebook visualizing the combined ALAS1 expression metric (`Expression_combined`, mean of normalized `Expression level` and `Read count`) over time using a generated `Time_min` column (0–999 minutes) across a 1000-row dataset. It calculates statistics, detects trends via linear regression, and plots trends with trend lines. The strain with the highest combined expression is identified.
- **Purpose**: Practices time-series analysis interactively, a key skill for ML tasks like forecasting in biochemical contexts.
- **Files**:
  - `alas1_read_count.ipynb`: Jupyter Notebook for analysis and visualization.
  - `dff.csv`: 1000-row dataset with  `Gene name,Expression level,Read count,Strain,Time_min,Expression_combined`.
  - `alas1_read_count_trends.png`: Plot of combined expression trends over time.
  - `requirements.txt`: Python library dependencies.

## Getting Started

### Prerequisites
- Python 3.8 or higher
- Jupyter Notebook or JupyterLab (`pip install jupyter`)
- Install required libraries: `pip install -r requirements.txt` (from either project folder)
- Libraries: `pandas>=1.5.0`, `numpy>=1.24.0`, `matplotlib>=3.7.0`, `jupyter>=1.0.0`

### How to Run
1. Clone or download this repository:
   - Clone: `git clone https://github.com/your-username/biochemistry_ml_mini_projects.git`
   - Or download as a ZIP from the GitHub repository page.
2. Navigate to a project folder:
   ```bash
   cd biochemistry_ml_mini_projects/alas1_expression_analyzer