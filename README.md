# Big Clinica Tabular Databases

**Big Clinica** is an open-source toolkit developed for large-scale clinical tabular datasets, with robust support for GPU acceleration. This library enables streamlined data processing, visualization, and analysis for commonly used clinical databases including:

- **NIS** (National Inpatient Sample)  
- **NSQIP** (National Surgical Quality Improvement Program)  
- **PhysioNet** datasets  
- **SEER** (Surveillance, Epidemiology, and End Results)

### 🚀 Key Features

- **Fast Data Retrieval** — Efficient loading and querying of large datasets  
- **Data Cleaning Pipelines** — Modular tools to clean and standardize messy real-world clinical data  
- **Handling Missing Data** — Includes KNN, MICE, and ML-based imputation strategies  
- **Visualization Tools** — Exploratory and clinical-specific plots for insight generation  
- **Statistical Modeling** — Built-in support for univariate, multivariate, and survival analyses  
- **Feature Selection** — Automated methods to help identify relevant variables for modeling

---

## 📁 Project Structure
clinical-data-toolkit/ ├── R-package/ # R package root │ ├── DESCRIPTION # Package metadata │ ├── NAMESPACE # Function exports │ ├── LICENSE # License file │ ├── README.md # Package documentation │ ├── .Rbuildignore # Build ignore file │ ├── inst/ # Package resources │ │ └── extdata/ # Example data │ ├── man/ # Package documentation │ ├── tests/ │ │ ├── testthat/ # Unit tests │ │ └── testthat.R # Test runner │ ├── vignettes/ # Usage examples and tutorials │ │ ├── introduction.Rmd │ │ ├── data_processing.Rmd │ │ └── analysis_examples.Rmd │ └── R/ │ ├── datasets/ # Dataset-specific modules │ │ ├── dataset_base.R │ │ ├── nis.R │ │ ├── nsqip.R │ │ ├── physionet.R │ │ └── helpers/ │ │ ├── icd_utils.R │ │ └── cpt_utils.R │ ├── preprocessing/ │ │ ├── cleaner.R │ │ ├── feature_engineering.R │ │ ├── normalization.R │ │ ├── encoding.R │ │ └── imputation/ │ │ ├── imputation_base.R │ │ ├── mice_wrapper.R │ │ ├── knn_imputation.R │ │ └── ml_imputation.R │ ├── analysis/ │ │ ├── univariate.R │ │ ├── multivariate.R │ │ ├── survival.R │ │ ├── feature_selection.R │ │ └── statistical_tests.R │ ├── visualization/ │ │ ├── exploratory.R │ │ ├── clinical_plots.R │ │ ├── survival_plots.R │ │ ├── forest_plots.R │ │ ├── model_diagnostics.R │ │ └── themes.R
