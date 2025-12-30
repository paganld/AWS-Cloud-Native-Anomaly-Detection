# Cloud-Native Network Anomaly Detection Pipeline

**Objective:** Engineered a robust, unsupervised learning pipeline to detect "Zero-Day" network intrusions using the NSL-KDD dataset. Designed for deployment as an AWS SageMaker endpoint.

## Architecture & Tech Stack

* **Deep Learning:** PyTorch Autoencoder (Reconstruction Error thresholding at 95th percentile).
* **Machine Learning:** Scikit-Learn Isolation Forest (Contamination parameter aligned to attack distribution).
* **MLOps:** Simulation of AWS SageMaker inference logic (`model_fn`, `input_fn`) with JSON schema enforcement.
* **Data Engineering:** Custom preprocessing pipeline with persistent artifact serialization (`scaler.pkl`).

## Key Results

* Successfully identified **95% of normal traffic patterns** to minimize false positives (Alert Fatigue).
* Implemented **"Fail-Fast" inference logic** to ensure production reliability.

## How to Run

1. Install dependencies:
   ```bash
   pip install -r requirements.txt

2. jupyter notebook notebooks/NSL_KDD_Pipeline.ipynb
