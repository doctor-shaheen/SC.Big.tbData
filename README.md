# Big Clinica Tabular Databases

**Big Clinica** is an open-source clinical data toolkit designed for scalable analysis of large tabular datasets from real-world clinical studies. It supports both **R** and **Python** packages, built with GPU acceleration in mind, to make clinical research faster, reproducible, and accessible to both data scientists and clinical researchers.

Our goal is to create a comprehensive ecosystem for handling high-dimensional clinical data such as:

- **NIS** (National Inpatient Sample)
- **NSQIP** (National Surgical Quality Improvement Program)
- **PhysioNet** (MIMIC, eICU)
- **SEER** (Surveillance, Epidemiology, and End Results)

With consistent APIs across both R and Python, Big Clinica helps streamline:

- 🔍 **Data Retrieval & Wrangling**
- 🧹 **Data Cleaning Pipelines**
- ❓ **Missing Data Imputation**
- 📊 **Exploratory & Statistical Visualization**
- 🧪 **Statistical Modeling & Feature Selection**
- 🧠 **Machine Learning with GPU Acceleration**

---

## 🛠 Project Structure

### `clinical-data-toolkit/`

<details>
<summary>📦 R-package/</summary>

```text
R-package/
├── DESCRIPTION
├── NAMESPACE
├── LICENSE
├── README.md
├── .Rbuildignore
├── inst/
│   └── extdata/
├── man/
├── tests/
│   ├── testthat/
│   └── testthat.R
├── vignettes/
│   ├── introduction.Rmd
│   ├── data_processing.Rmd
│   └── analysis_examples.Rmd
└── R/
    ├── datasets/
    │   ├── dataset_base.R
    │   ├── nis.R
    │   ├── nsqip.R
    │   ├── physionet.R
    │   └── helpers/
    │       ├── icd_utils.R
    │       └── cpt_utils.R
    ├── preprocessing/
    │   ├── cleaner.R
    │   ├── feature_engineering.R
    │   ├── normalization.R
    │   ├── encoding.R
    │   └── imputation/
    │       ├── imputation_base.R
    │       ├── mice_wrapper.R
    │       ├── knn_imputation.R
    │       └── ml_imputation.R
    ├── analysis/
    │   ├── univariate.R
    │   ├── multivariate.R
    │   ├── survival.R
    │   ├── feature_selection.R
    │   └── statistical_tests.R
    ├── visualization/
    │   ├── exploratory.R
    │   ├── clinical_plots.R
    │   ├── survival_plots.R
    │   ├── forest_plots.R
    │   ├── model_diagnostics.R
    │   └── themes.R
    ├── ml/
    │   ├── engines/
    │   │   ├── h2o_engine.R
    │   │   └── gpu_engine.R
    │   ├── models/
    │   │   ├── logistic.R
    │   │   ├── random_forest.R
    │   │   ├── gbm.R
    │   │   └── deep_learning.R
    │   └── evaluation/
    │       ├── metrics.R
    │       ├── cross_validation.R
    │       └── calibration.R
    ├── utils/
    │   ├── parallel.R
    │   ├── gpu_detection.R
    │   └── logging.R
    └── package.R
```
<details> 
<summary>🐍 python-package/</summary>

```
python-package/
├── pyproject.toml
├── setup.py
├── setup.cfg
├── MANIFEST.in
├── LICENSE
├── README.md
├── docs/
│   ├── conf.py
│   ├── index.rst
│   └── tutorials/
├── tests/
│   ├── __init__.py
│   ├── conftest.py
│   ├── test_datasets.py
│   ├── test_preprocessing.py
│   └── test_ml.py
├── examples/
│   ├── nis_examples.ipynb
│   ├── nsqip_examples.ipynb 
│   └── physionet_examples.ipynb
└── clinical_data_toolkit/
    ├── __init__.py
    ├── config.py
    ├── datasets/
    │   ├── __init__.py
    │   ├── base.py
    │   ├── nis.py
    │   ├── nsqip.py
    │   ├── physionet/
    │   │   ├── __init__.py
    │   │   ├── mimic.py
    │   │   └── eicu.py
    │   └── utils/
    │       ├── __init__.py
    │       ├── icd_utils.py
    │       └── cpt_utils.py
    ├── preprocessing/
    │   ├── __init__.py
    │   ├── cleaner.py
    │   ├── feature_engineering.py
    │   ├── normalization.py
    │   ├── encoding.py
    │   ├── imputation/
    │   │   ├── __init__.py
    │   │   ├── base.py
    │   │   ├── simple.py
    │   │   ├── iterative.py
    │   │   ├── knn.py
    │   │   └── ml.py
    │   └── acceleration/
    │       ├── __init__.py
    │       ├── base.py
    │       ├── cuda.py
    │       └── metal.py
    ├── analysis/
    │   ├── __init__.py
    │   ├── univariate.py
    │   ├── multivariate.py
    │   ├── survival.py
    │   ├── feature_selection.py
    │   └── statistical_tests.py
    ├── visualization/
    │   ├── __init__.py
    │   ├── exploratory.py
    │   ├── clinical_plots.py
    │   ├── survival_plots.py
    │   ├── forest_plots.py
    │   ├── model_diagnostics.py
    │   └── themes.py
    ├── ml/
    │   ├── __init__.py
    │   ├── engines/
    │   │   ├── __init__.py
    │   │   ├── sklearn_engine.py
    │   │   ├── h2o_engine.py
    │   │   └── accelerated/
    │   │       ├── __init__.py
    │   │       ├── cuml_engine.py
    │   │       └── jax_engine.py
    │   ├── models/
    │   │   ├── __init__.py
    │   │   ├── logistic.py
    │   │   ├── random_forest.py
    │   │   ├── gbm.py
    │   │   └── deep_learning.py
    │   └── evaluation/
    │       ├── __init__.py
    │       ├── metrics.py
    │       ├── cross_validation.py
    │       └── calibration.py
    └── utils/
        ├── __init__.py
        ├── parallel.py
        ├── gpu_utils.py
        └── logging.py
```
-------------
**👥 Maintained by Shaheen-Clinic-Open-Source Team**
We're building tools to make clinical data science fast, modular, and GPU-native.
Interested in contributing? Open an issue or submit a PR!

**Contact us to contribute: 
ahmeds1999haheen@gmail.com


-------------
**📄 License**
This project is licensed under the MIT License.



