# mlops-pipeline-platform

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Docker](https://img.shields.io/badge/Docker-Enabled-blue)
![MLOps](https://img.shields.io/badge/MLOps-Production-green)

---

# `Mlops-pipeline-platform`

# 🚀 MLOps & AI Portfolio

This repository serves as a central hub for my Machine Learning, MLOps, and AI projects.

---

## 📂 Featured Projects

### ⚙️ MLOps & Production Pipelines
- 🔹 [MLOps Pipeline Platform](https://github.com/hossain-sanowar/mlops-pipeline-platform)  
  End-to-end ML pipeline with MLflow, DVC, Docker, Kubernetes, CI/CD, Prometheus, Grafana (PyTorch, TensorFlow, Scikit-learn, AWS, GCP)

- 🔹 [NLP Sentiment MLOps Pipeline](https://github.com/hossain-sanowar/nlp-sentiment-mlops-pipeline)  
  Production NLP pipeline with MLflow, DVC, Docker, Kubernetes, CI/CD (GitHub Actions, Jenkins), monitoring with Prometheus & Grafana

---

### 🏭 Machine Learning Systems
- 🔹 [Consignment Product Prediction](https://github.com/hossain-sanowar/Consignment-Product-Prediction)  
  End-to-end ML system with ETL pipelines, Airflow, DVC, Docker, AWS (S3, EC2), Hadoop, TensorFlow, and web UI

- 🔹 [Kidney Disease Classification](https://github.com/hossain-sanowar/end-end-Kidney_Disease_Classification)  
  ML pipeline with DVC, CI/CD on AWS, and user-facing application for medical prediction

---

### 🤖 LLM & Generative AI Systems
- 🔹 [Flipkart LLM Production System](https://github.com/hossain-sanowar/llm_flipkart_production)  
  RAG-based LLM system using Groq, HuggingFace, LangChain, AstraDB with Docker, Kubernetes, and monitoring stack

- 🔹 [AI Study Agent](https://github.com/hossain-sanowar/llm_aiStudy_agent)  
  Multi-agent LLM system with LangChain, Groq, Kubernetes, Jenkins, WebHooks, and scalable API deployment

- 🔹 [AI Music Composer](https://github.com/hossain-sanowar/llm_AImusic_composer)  
  AI-powered music generation system using Music21, Groq, LangChain with Docker, Kubernetes (GKE), and cloud deployment

---

## 🎯 Key Skills Demonstrated
- MLOps (CI/CD, Docker, Kubernetes)
- LLM Systems (RAG, Agents, LangChain)
- End-to-End ML Pipelines
- Production Deployment

---

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
