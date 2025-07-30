# ALAS1 Gene Expression and Read Count Analysis Mini-Projects

This repository contains four Jupyter Notebook-based mini-projects analyzing **ALAS1 gene expression levels** and **read counts** across strains, using a 1000-row RNA-Seq dataset from the Bgee database. As a Biochemistry graduate, I’m pursuing an ML developer path with a focus on bioinformatics. These projects support heme biosynthesis studies and my Phase 2 and 3 ML roadmap.

## Project Overview

### 1. ALAS1 Expression Analyzer
- **Description**: Normalizes `ALAS1_Expression` and `ALAS1_Read_Count` to compute `ALAS1_Combined`, calculates statistics, and visualizes distribution via histogram.
- **Files**:
  - `alas1_expression_analyzer.ipynb`
  - `alas1_expression_data.csv`
  - `alas1_expression_distribution.png`
  - `requirements.txt`

### 2. ALAS1 Read Count Visualizer
- **Description**: Visualizes `ALAS1_Combined` over time (`Time_min`), with linear and robust (Huber) regression to handle outliers (e.g., at ~150 minutes).
- **Files**:
  - `alas1_read_count_visualizer.ipynb`
  - `alas1_read_counts.csv`, `alas1_read_counts_clean.csv` (optional)
  - `alas1_read_count_trends.png`, `alas1_outlier_analysis.png`, `alas1_robust_trend.png`
  - `requirements.txt`

### 3. ALAS1 Strain Clustering
- **Description**: Uses K-means clustering to group strains by `ALAS1_Combined`, evaluates with silhouette score, and analyzes outliers.
- **Files**:
  - `alas1_strain_clustering.ipynb`
  - `alas1_expression_data.csv`
  - `alas1_cluster_scatter.png`
  - `requirements.txt`
 
### 3. ALAS1 Strain Clustering Without Outliers
- **Description**: Uses IQR method to analyses the outliers which 37 and fixed it to reduce the dataset to 963 rows.
- **Files**:
  - `alas1_strain_clustering.ipynb`
  - `alas1_expression_clean_data.csv`
  - `alas1_cluster_scatter.png`
  - alas1_cluater_cleaned.png'
  - 'alas1_combined_boxplot_with_outliers.png'
  - `requirements.txt'

### 4. ALAS1 Expression Classifier
- **Description**: Uses Random Forest to classify strains into high, medium, or low `ALAS1_Combined` levels, evaluates with accuracy and F1-score, and analyzes outlier classification.
- **Purpose**: Identifies strain expression patterns for heme biosynthesis, responding to community feedback on outliers.
- **Files**:
  - `alas1_xpression_classifier.ipynb`
  - `alas1_expression_data.csv`
  - `alas1_confusion_matrix.png`, `alas1_feature_importance.png`
  - `requirements.txt`
### 4. ALAS1 Expression Classifier
- **Description**: Uses Random Forest to classify strains into high, medium, or low `ALAS1_Combined` levels, evaluates with accuracy and F1-score, and analyzes outlier classification.
- **Purpose**: Identifies the outliers and fixed it to generate new dataset without outliers, responding to community feedback on outliers.
- **Files**:
  - `alas1_xpression_classifier.ipynb`
  - `alas1_expression_data.csv`
  - 'alas1_expression_data_without_outliers.csv'
  - 'alas1_combineed_classfier_boxplot_with_outliers'
  - 'alas1_confusion_matrix_without_outliers.png', 'alas1_feature_importance_without_outliers.png'
  - `alas1_confusion_matrix.png`, `alas1_feature_importance.png`
  - `requirements.txt`
    
## Getting Started
- **Prerequisites**: Python 3.8+, Jupyter (`pip install jupyter`), libraries (`pip install -r requirements.txt`): `pandas>=1.5.0`, `numpy>=1.24.0`, `matplotlib>=3.7.0`, `jupyter>=1.0.0`, `scikit-learn>=1.2.0`, `seaborn>=0.12.0`.
- **Run**: Clone/download repo, navigate to project folder, run `jupyter notebook`, and execute `.ipynb` files.
- **Data**: 1000-row Bgee RNA-Seq dataset for ALAS1 (Ensembl ID: ENSG00000023330), with `Strain_ID`, `Strain_Name`, `ALAS1_Expression`, `ALAS1_Read_Count`, `ALAS1_Combined`. Data: Bgee, CC BY 4.0, https://www.bgee.org.

## License
- **Code**: [MIT License](LICENSE).
- **Data**: CC BY 4.0, cite: “Data from Bgee, CC BY 4.0, https://www.bgee.org, accessed July 2025.”

