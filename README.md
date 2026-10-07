# MLOps Pipeline Platform

A reproducible machine-learning pipeline: data versioning and pipeline stages with **DVC**, experiment tracking with **MLflow**, packaging with **Docker**, and CI with **GitHub Actions** and **Jenkins**.

![Python](https://img.shields.io/badge/Python-3.10-blue)
![DVC](https://img.shields.io/badge/DVC-pipeline-945DD6)
![MLflow](https://img.shields.io/badge/MLflow-tracking-0194E2)
![Docker](https://img.shields.io/badge/Docker-container-2496ED)

---

## What it does

```
data_ingestion → train → evaluate → (MLflow tracks params, metrics, models)
        ▲                    │
   params.yaml          dvc.yaml stages, re-run only what changed
```

- **One command runs the whole pipeline:** `dvc repro`
- **Every run is tracked:** parameters, metrics and model artefacts are logged to MLflow, so runs can be compared and reproduced
- **Configuration in one place:** hyper-parameters live in `params.yaml`; changing a value re-runs only the affected stages
- **Tested and built automatically:** CI runs the tests on every push (GitHub Actions; an equivalent Jenkins pipeline is in `jenkins/`)
- **Containerised:** the `Dockerfile` packages the pipeline and prediction code into one image

## Tech stack

Python · DVC · MLflow · Docker · GitHub Actions · Jenkins · pytest

## Project structure

```
mlops-pipeline-platform/
├── src/
│   ├── data_ingestion.py    # load and split data
│   ├── train.py             # train model, log to MLflow
│   ├── evaluate.py          # compute metrics, log to MLflow
│   ├── predict.py           # inference
│   └── config.py
├── dvc.yaml                 # pipeline stages
├── params.yaml              # hyper-parameters
├── tests/test_pipeline.py
├── notebooks/experiments.ipynb
├── Dockerfile
├── .github/workflows/ci.yml
└── jenkins/Jenkinsfile
```

## Run locally

```bash
git clone https://github.com/hossain-sanowar/mlops-pipeline-platform
cd mlops-pipeline-platform
pip install -r requirements.txt

dvc repro          # run the full pipeline
mlflow ui          # open http://localhost:5000 to compare runs
pytest tests/      # run the tests
```

Run with Docker:

```bash
docker build -t mlops-pipeline .
docker run --rm mlops-pipeline
```

## Next steps

- Serve `predict.py` behind a small REST API
- Deploy the container to Kubernetes with a Helm chart
- Add Prometheus metrics for latency and prediction counts

---

**Author:** Md Sanowar Hossain · [LinkedIn](https://www.linkedin.com/in/HossainSanowar) · [GitHub](https://github.com/hossain-sanowar)
