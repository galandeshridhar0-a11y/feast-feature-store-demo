# Feast Feature Store

This repository contains notebooks for learning and experimenting with Feast-based feature stores and MLflow model tracking. The notebooks demonstrate feature engineering, feature retrieval, and model training workflows using sample data.

## Repository contents

- `Feast_MLflow_Iris_Feature_Store.ipynb`: Iris classification example using Feast and MLflow
- `Feast_Regression_Diabetes_Feature_Store.ipynb`: regression example using Feast feature store workflows
- `Feast_Feature_Store_Exercise.ipynb`: hands-on exercise notebook for practicing Feast concepts
- `requirements.txt`: Python dependencies for the notebooks
- `.gitignore`: ignore rules for virtual environments, notebook checkpoints, and generated artifacts

## What is Feast?

Feast is an open-source feature store that simplifies building and operating feature pipelines for machine learning. In this project, Feast is used to:

- define and store reusable features
- keep feature values consistent between training and inference
- manage feature schemas and entity relationships

The notebooks show how to define Feast entities and features, materialize feature data, and retrieve feature values for model training.

## What is MLflow?

MLflow is an open-source platform for managing the machine learning lifecycle. It helps you:

- track experiments, parameters, and metrics
- log models and artifacts
- compare runs across different experiments

The notebooks in this repo log training runs to MLflow so you can inspect model metrics and artifacts while working with Feast-powered feature workflows.

## Setup on Windows

From the repository root:

```powershell
python -m venv .venv
.\.venv\Scripts\activate
pip install -r requirements.txt
```

## Run MLflow locally

If you want to use MLflow tracking while running the notebooks, start the server from the repository root:

```powershell
mlflow server --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./mlruns --host 127.0.0.1 --port 5000
```

Then open:

```text
http://127.0.0.1:5000
```

## Notes

- `mlruns/` and `*.db` files are generated at runtime and should be ignored by version control.
- The notebooks are the primary source files for exercises.
- `.venv/` and `.ipynb_checkpoints/` are also ignored by `.gitignore`.

## Push to GitHub

```bash
git init
git add .
git commit -m "Add Feast feature store notebooks"
git branch -M main
git remote add origin https://github.com/galandeshridhar0-a11y/feast-feature-store-demo.git
git push -u origin main
```
