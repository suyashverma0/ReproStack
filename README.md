
# ReproStack — End-to-End MLOps Pipeline

An end-to-end Machine Learning Operations (MLOps) project demonstrating a reproducible, configuration-driven ML pipeline using a spam detection model as the use case.

ReproStack integrates YAML-based configuration management, DVC pipeline orchestration, experiment tracking, and Amazon S3 storage to establish a structured and reproducible machine learning workflow.

## Overview

Building a machine learning model is only one part of the ML lifecycle. Managing data, tracking experiments, organizing pipeline stages, and maintaining reproducibility are equally important.

ReproStack demonstrates these practices through a modular spam detection pipeline, with an emphasis on experiment management, version control, and cloud storage integration.

## Key Features

- **End-to-End ML Pipeline:** Organizes the machine learning workflow into structured stages.
- **YAML Configuration:** Manages pipeline parameters and configuration separately from the source code.
- **DVC Integration:** Supports data versioning, pipeline orchestration, and reproducible experiments.
- **Experiment Tracking:** Records model evaluation metrics to help compare experiments.
- **Amazon S3 Integration:** Uses cloud storage for the project's configured data or artifacts.
- **Spam Detection:** Applies machine learning techniques to classify spam and non-spam messages.

## Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Pandas & NumPy | Data processing |
| Scikit-learn | Machine learning and evaluation |
| Jupyter Notebook | Data exploration and model development |
| YAML | Configuration management |
| DVC | Data versioning and pipeline orchestration |
| Amazon S3 | Cloud storage |
| Experiment tracking | Tracking model parameters and performance |

## Project Workflow

1. **Data Ingestion:** Load the spam detection dataset.
2. **Preprocessing:** Clean and prepare the data for model training.
3. **Feature Engineering:** Transform the text into features suitable for machine learning.
4. **Model Training:** Train the selected classification model.
5. **Model Evaluation:** Evaluate performance using appropriate classification metrics.
6. **Experiment Tracking:** Record and compare model results.
7. **Pipeline Orchestration:** Use DVC to manage and reproduce pipeline stages.
8. **Cloud Storage:** Integrate Amazon S3 for the configured storage workflow.

*The workflow above describes the logical pipeline; individual stages depend on the project's actual implementation.*

## Project Structure

```text
ReproStack/
├── data/
├── notebooks/
│   └── spam_detection.ipynb
├── src/
│   ├── data_ingestion.py
│   ├── preprocessing.py
│   ├── feature_engineering.py
│   ├── model_training.py
│   └── model_evaluation.py
├── params.yaml
├── dvc.yaml
├── dvc.lock
├── requirements.txt
└── README.md
```

*Adjust the structure to match the actual files in your repository.*

## Getting Started

### 1. Clone the repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd <YOUR_PROJECT_FOLDER>
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows:

```powershell
.\venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

Ensure that DVC, its required S3 support, and the experiment-tracking library used by the project are included in your dependencies.

### 4. Configure cloud storage

Configure AWS credentials securely using an appropriate AWS profile, environment variables, or IAM role. Configure the DVC remote according to your repository's setup.

Never commit AWS access keys, secret keys, or other credentials to GitHub.

### 5. Run the pipeline

```bash
dvc repro
```

If the project uses DVC experiments, run:

```bash
dvc exp run
```

Inspect experiment results with:

```bash
dvc exp show
```

Use the commands supported by your actual DVC configuration.

## Evaluation Metrics

Model performance should be evaluated using suitable classification metrics, such as:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix

Actual results should be added here after running the pipeline. No performance figures are reported until they have been measured.

## Reproducibility

ReproStack demonstrates how configuration management, versioned data, pipeline definitions, and experiment tracking can improve the reproducibility and maintainability of machine learning workflows.

Results may still depend on the dataset version, software environment, random seeds, and external dependencies.

## Future Improvements

- Automated pipeline testing with GitHub Actions
- Data validation and schema checks
- Docker-based packaging
- FastAPI model serving
- Prediction logging and model monitoring
- Automated model evaluation and comparison

## Learning Outcomes

- Understanding core MLOps concepts
- Building modular ML pipelines
- Managing configuration through YAML
- Using DVC for versioning and pipeline orchestration
- Tracking and comparing ML experiments
- Integrating Amazon S3 into an ML workflow

## Author

**Suyash Verma**

- GitHub:
