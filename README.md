# From genes to prognosis: predicting breast-cancer mortality from clinical and genomic data (METABRIC)

Machine Learning 1 capstone project — Tek-Up, ING-4 SDIA, Semester 7, 2026–2027
Instructor: Dr. Haythem Ghazouani

## Team

- Oumaima Hafiane
- Imen Hichri

## Central question

Do gene expression and mutations predict breast-cancer death better than clinical data alone, and better than the Nottingham Prognostic Index (NPI) that oncologists already use?

- Task: binary classification
- Target: `y = 1` if `death_from_cancer == "Died of Disease"`, else `0`
- Methods: classical machine learning only (scikit-learn, XGBoost, LightGBM)

## Dataset

- File: `data/raw/METABRIC_RNA_Mutation.csv` (1,904 patients × 693 columns), included in this repository
- Downloaded from Kaggle: https://www.kaggle.com/datasets/raghadalharbi/breast-cancer-gene-expression-profiles-metabric
- Original source: cBioPortal, study `brca_metabric` — https://www.cbioportal.org/study/summary?id=brca_metabric (ODbL licence)
- Patients are de-identified.

References:

- Curtis C. et al. (2012). The genomic and transcriptomic architecture of 2,000 breast tumours reveals novel subgroups. *Nature*, 486, 346–352.
- Pereira B. et al. (2016). The somatic mutation profiles of 2,433 breast cancers refine their genomic and transcriptomic landscapes. *Nature Communications*, 7, 11479.

## Project structure

```
metabric-ml1-project/
|-- data/
|   |-- raw/          # Original dataset (never modified)
|   |-- processed/    # Cleaned dataset
|-- notebooks/
|   |-- 01_eda.ipynb
|   |-- 02_preprocessing.ipynb
|   |-- 03_modeling.ipynb
|   |-- 04_final_pipeline.ipynb   # Single end-to-end notebook (the one to grade)
|-- report/
|   |-- report.pdf
|   |-- slides.pdf
|-- requirements.txt
|-- README.md
```

## How to run

Requires Python 3.10 or later.

```bash
# 1. Clone the repository
git clone https://github.com/Mayma9/metabric-ml1-project.git
cd metabric-ml1-project

# 2. Create and activate a virtual environment
python -m venv ml_project_env
# Windows:
ml_project_env\Scripts\activate
# macOS / Linux:
source ml_project_env/bin/activate

# 3. Install dependencies
pip install -r requirements.txt
```

Then open `notebooks/04_final_pipeline.ipynb` in VS Code, select the `ml_project_env` kernel, and choose **Restart Kernel and Run All**. All random seeds are set to 42.
