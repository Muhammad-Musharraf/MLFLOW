# 🚀 MLflow Experiments & Tracking

> An end-to-end MLOps learning repository demonstrating **experiment tracking**, **model management**, **binary classification**, and **remote logging with DagsHub** — all powered by MLflow.

---

## 📌 About

This repository is a hands-on exploration of [MLflow](https://mlflow.org/), an open-source Machine Learning Operations (MLOps) platform. It covers the full ML experiment lifecycle — from running your first tracked experiment to logging runs remotely via DagsHub — with practical Jupyter Notebooks you can run and extend.

---

## 📁 Repository Structure

```
MLFLOW/
├── First Experiments/              # Introductory MLflow experiment notebooks
├── ml_flow_binary_classification/  # Binary classification with MLflow tracking
├── ml_flow_dagshub.ipynb           # Remote experiment tracking via DagsHub
├── .gitignore
└── README.md
```

---

## ✨ Features

| Feature | Description |
|---|---|
| 🔬 **Experiment Tracking** | Log parameters, metrics, and artifacts across runs |
| 📊 **MLflow UI** | Visualize and compare experiments locally or remotely |
| 🗂️ **Model Registry** | Version and manage trained models |
| 🔁 **Binary Classification** | End-to-end ML pipeline with tracked training runs |
| ☁️ **DagsHub Integration** | Remote MLflow server for team collaboration and sharing |

---

## 🛠️ Prerequisites

- Python 3.8+
- pip

Install the required packages:

```bash
pip install mlflow dagshub scikit-learn pandas numpy jupyter
```

---

## ⚡ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Muhammad-Musharraf/MLFLOW.git
cd MLFLOW
```

### 2. Launch Jupyter

```bash
jupyter notebook
```

### 3. Run First Experiments

Open any notebook inside `First Experiments/` to see MLflow's core tracking in action — logging parameters, metrics, and inspecting runs in the MLflow UI.

```bash
# Start the local MLflow UI (in a separate terminal)
mlflow ui
# Then visit: http://localhost:5000
```

---

## 🤖 Binary Classification

The `ml_flow_binary_classification/` folder contains a complete ML pipeline where MLflow tracks:

- **Parameters** — model hyperparameters (e.g. `n_estimators`, `max_depth`)
- **Metrics** — accuracy, precision, recall, F1-score, AUC-ROC
- **Artifacts** — trained model files, confusion matrices
- **Run comparisons** — side-by-side experiment comparison in the MLflow UI

---

## ☁️ DagsHub Integration

`ml_flow_dagshub.ipynb` demonstrates logging experiments to a **remote MLflow server** hosted by DagsHub, enabling easy sharing and team collaboration without any server setup.

### Setup

```python
import dagshub
import mlflow

dagshub.init(repo_owner="Muhammad-Musharraf", repo_name="MLFLOW", mlflow=True)

with mlflow.start_run():
    mlflow.log_param("model", "RandomForest")
    mlflow.log_metric("accuracy", 0.92)
```

Access the remote MLflow UI at:

```
https://dagshub.com/Muhammad-Musharraf/MLFLOW.mlflow
```

> **Note:** You'll need to set your DagsHub credentials via environment variables or the DagsHub client before logging experiments remotely.

---

## 🔑 Environment Variables

For DagsHub authentication, set the following before running remote notebooks:

```bash
export MLFLOW_TRACKING_USERNAME=your_dagshub_username
export MLFLOW_TRACKING_PASSWORD=your_dagshub_token_or_password
```

---

## 🧰 Tech Stack

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)
![MLflow](https://img.shields.io/badge/MLflow-tracking-orange?logo=mlflow)
![DagsHub](https://img.shields.io/badge/DagsHub-remote%20server-purple)
![Jupyter](https://img.shields.io/badge/Jupyter-notebooks-orange?logo=jupyter)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-yellow?logo=scikit-learn)

---

## 📖 MLflow Core Concepts

| Concept | Description |
|---|---|
| **Run** | A single execution of your ML code with logged params & metrics |
| **Experiment** | A named group of related runs |
| **Artifact** | Files associated with a run (models, plots, datasets) |
| **Model Registry** | Centralized store to manage model versions and stages |

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## 📬 Contact

**Muhammad Musharraf**
GitHub: [@Muhammad-Musharraf](https://github.com/Muhammad-Musharraf)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

⭐ If you found this helpful, please give the repo a star!
