# Iris Species Classification

A **minimal, clean, and reproducible traditional machine learning project** using the Iris dataset.

This repository is designed as a **reference implementation and starter template** for classical ML workflows, following widely accepted practices from projects such as scikit-learn examples and Google ML templates.

---

## Overview

The project demonstrates a complete ML workflow:

- Structured data organization
- Deterministic preprocessing
- Baseline model training
- Evaluation and artifact persistence

The focus is on **clarity, simplicity, and extensibility**, rather than framework complexity.

---

## Project Structure

```
project/
├── data/
│   ├── raw/
│   │   └── iris.csv
│   └── processed/
│
├── src/
│   ├── config/
│   ├── data/
│   ├── models/
│   ├── pipelines/
│   └── utils/
│
├── experiments/
├── models_artifacts/
├── reports/
├── scripts/
├── requirements.txt
└── README.md
```

Each directory has a single responsibility and avoids cross-layer coupling.

---

## Dataset

- **Name**: Iris Species Dataset  
- **Format**: CSV  
- **Location**: `data/raw/iris.csv`  
- **Target**: `species`

### Feature Columns

- `sepal_length`
- `sepal_width`
- `petal_length`
- `petal_width`

**Data handling rules**:
- Raw data is treated as **read-only**
- All transformations are written to `data/processed/`

---

## Model

- **Algorithm**: Logistic Regression  
- **Task**: Multiclass Classification  
- **Library**: scikit-learn

Logistic Regression is used as a **baseline** due to its interpretability, stability, and suitability for small structured datasets.

---

## Environment Setup

### (Optional) Create Virtual Environment

```powershell
python -m venv .venv
.\.venv\Scripts\activate
```

### Install Dependencies

```powershell
pip install -r requirements.txt
```

### Core Dependencies

- pandas
- numpy
- scikit-learn
- joblib
- pyyaml

---

## Usage

### Train and Evaluate

```powershell
.\scripts\train.ps1
```

This command executes the full pipeline:

1. Load data from `data/raw/iris.csv`
2. Perform stratified train/validation/test split
3. Persist processed data to `data/processed/`
4. Train the model
5. Save the trained model to `models_artifacts/final/model.joblib`
6. Write evaluation metrics to `reports/results.md`

---

### Evaluate Only

```powershell
.\scripts\evaluate.ps1
```

Runs evaluation using an existing trained model without retraining.

---

## Reproducibility

This project emphasizes reproducibility through:

- Fixed random seeds
- Deterministic preprocessing steps
- Explicit dependency specification
- Serialized model artifacts

---

## Extensibility

The structure is intentionally simple but supports extension to:

- Additional classical ML algorithms
- Hyperparameter tuning
- Experiment tracking
- Batch or API-based inference
- CI/CD-enabled ML workflows

---

## License

This project is licensed under the terms specified in the `LICENSE` file.
