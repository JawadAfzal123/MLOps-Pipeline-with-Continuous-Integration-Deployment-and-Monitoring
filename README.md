## Overview

This project implements a robust **MLOps pipeline**, enabling **continuous integration (CI)**, **continuous deployment (CD)**, and **continuous monitoring (CM)** of machine learning models. By leveraging modern cloud infrastructure such as **AWS**, **Kubernetes**, and open-source tools, this pipeline ensures **scalability**, **reproducibility**, and **maintainability** throughout the machine learning lifecycle.

![MLOps Architecture](https://github.com/Chandru-21/MLOps_Project/assets/64595758/123511be-fe66-424d-8776-513b908840fe)

---

## MLOps Maturity Level: 4

This project is designed at **MLOps Maturity Level 4**, which includes highly automated processes for the full machine learning lifecycle, ensuring streamlined integration, deployment, and monitoring.

---

## Key Features

* **Data Versioning (DVC):** Manages data versions using DVC (Data Version Control) to ensure reproducibility of training data.

* **Continuous Integration (CI):** Automated code building, testing (via Pytest), and Docker image pushing to **AWS ECR** are triggered via **GitHub Actions**.

* **Experiment Tracking / Model Versioning (MLflow):** Tracks experiments and versions models with **MLflow**, enabling easy comparison of model performance.

* **Continuous Deployment (CD):** Deploys a **FastAPI** application in **AWS EKS (Kubernetes)** for both real-time and batch predictions.

* **Continuous Monitoring (CM):** Exposes FastAPI metrics for **Prometheus** integration and visualizes metrics with **Grafana**.

* **Continuous Training (CT):** Automatically triggers code execution in response to new data being pushed to remote DVC repositories, with commits to GitHub.

* **Drift Monitoring:** A **Streamlit** app monitors **data drift**, **target drift**, and conducts **data quality checks** to ensure model stability and quality.

---

## Architecture

This architecture integrates various components to provide a seamless and scalable MLOps pipeline:

1. **Data Ingestion and Versioning:** Data is versioned using DVC for reproducibility.
2. **Model Training and Experiment Tracking:** MLflow is used for tracking experiments and model versions.
3. **Deployment on Kubernetes (AWS EKS):** The FastAPI application is deployed on AWS EKS for real-time and batch processing.
4. **Monitoring and Metrics:** FastAPI exposes metrics to Prometheus for monitoring and Grafana for visualization.
5. **Continuous Integration and Delivery:** GitHub Actions automates the build, test, and deployment process.

---

## Data Monitoring

### Data Drift Monitoring:

![Data Drift](https://github.com/Chandru-21/MLOps_Project/assets/64595758/af0df23d-9980-4ee4-94c0-ddebdb923237)

### Data Quality Checks:

![Data Quality](https://github.com/Chandru-21/MLOps_Project/assets/64595758/c1c62d64-9b69-4ca7-ba45-45ae226a7620)

---

## Continuous Monitoring (CM)

### Exposing "/metrics" on FastAPI for Prometheus Integration:

![FastAPI Metrics](https://github.com/Chandru-21/MLOps_Project/assets/64595758/09b18b44-8cb1-4a86-9172-c79082cb77c8)

### FastAPI Integrated into Prometheus:

![FastAPI Prometheus](https://github.com/Chandru-21/MLOps_Project/assets/64595758/4b21c089-bef3-4e39-b5e1-04cb8e026345)

### Grafana for Visualization:

Monitoring FastAPI methods on Grafana:

![FastAPI Continuous Monitoring](https://github.com/Chandru-21/MLOps_Project/assets/64595758/930f0a9a-352f-41f9-8106-9b6735af8ce4)

### Monitoring Kubernetes Resources on Grafana:

![Grafana Kubernetes Dashboard](https://github.com/Chandru-21/MLOps_Project/assets/64595758/d046d9f9-1477-4975-9041-f4aa128bb0f3)

---

## Conclusion

This project provides an automated, scalable MLOps pipeline that includes data versioning, continuous integration, deployment, monitoring, and continuous training of machine learning models. By utilizing tools like **AWS**, **Kubernetes**, **MLflow**, and **GitHub Actions**, it facilitates the seamless management of machine learning workflows from training to deployment and monitoring.

---

