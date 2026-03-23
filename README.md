# mlops-pipeline-platform


---

# `Mlops-pipeline-platform`

## Folder Structure
```text
mlops-pipeline-platform/
├── README.md
├── requirements.txt
├── Dockerfile
├── .gitignore
├── src/
│   ├── data_ingestion.py
│   ├── train.py
│   ├── evaluate.py
│   ├── predict.py
│   └── config.py
├── notebooks/
│   └── experiments.ipynb
├── dvc.yaml
├── params.yaml
├── mlruns/
├── tests/
│   └── test_pipeline.py
├── .github/
│   └── workflows/
│       └── ci.yml
└── jenkins/
    └── Jenkinsfile
```
# MLOps Pipeline Platform

A reproducible end-to-end MLOps pipeline with experiment tracking, data versioning, CI/CD automation, and containerized deployment.

## Overview
This project demonstrates a production-style MLOps workflow for training, evaluating, versioning, and deploying machine learning models using modern infrastructure and automation tooling.

## Features
- Experiment tracking with MLflow
- Data and pipeline versioning with DVC
- Automated CI/CD workflows
- Dockerized model packaging
- Kubernetes-ready deployment
- Modular training and evaluation pipeline

## Tech Stack
- Python
- MLflow
- DVC
- Docker
- Kubernetes
- Jenkins
- GitHub Actions

## Project Structure
- `src/` modular pipeline steps
- `dvc.yaml` pipeline orchestration
- `params.yaml` configurable parameters
- `.github/workflows/` CI workflow
- `jenkins/` Jenkins pipeline config

## Run Locally
```bash
git clone https://github.com/hossain-sanowar/mlops-pipeline-platform
cd mlops-pipeline-platform
pip install -r requirements.txt
python src/train.py
```
## Pipeline

Typical workflow:

ingest data
preprocess data
train model
evaluate model
track experiments
package and deploy
Use Case

Built as a reference project for reproducible ML workflows and production-oriented model lifecycle management.

## Author

Md Sanowar Hossain
