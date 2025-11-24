Project by - Kunal Jagtap MSAIS

1. Project Overview

PulseAI predicts cardiovascular risk using user inputs such as age, cholesterol, blood pressure, chest pain type, smoking habits, and other clinical markers.

The app:

Classifies Low / Moderate / High heart risk
Provides drug recommendations and lifestyle suggestions
Displays SHAP explainability plots
Includes separate modules for drug recommendation, heart disease classifier, and medical chatbot
Runs locally via Streamlit using home.py

2. Repository Structure

Predictive-Analytics-For-Health-Monitoring/
│
├── Drug Recommendation/              # Drug/drug-class suggestion module
├── heart_disease_risk_assessment/    # Heart disease ML pipeline & assets
├── medibot/                          # Medical chatbot / vector DB logic
├── models/                           # Saved ML models (.pkl)
├── pages/                            # Additional Streamlit sub-pages
├── vectorstore/                      # Chroma/FAISS embeddings for chatbot
│
├── .dockerignore
├── .env                              # Environment variables (not committed)
├── constraints.txt
├── Dockerfile                        # For containerization
├── home.py                           # MAIN APPLICATION ENTRY POINT
├── README.md
└── requirements.txt

Folder Purpose Summary

Folder / File	Description
home.py	Main Streamlit entry point. Launches full PulseAI application.
Drug Recommendation/	Logic for recommending drug categories based on symptoms or risk.
heart_disease_risk_assessment/	Full ML pipeline, preprocessing, SHAP explainability, risk classifier.
models/	All serialized ML models (.pkl) including EasyEnsembleClassifier.
medibot/	LLM-driven medical guidance bot + vector store retrieval.
pages/	Streamlit multipage routes (UI subpages).
utils/	Helper scripts, feature engineering, metadata logger, data tools.
vectorstore/	Embeddings storage for medical Q&A.
Dockerfile	Containerization setup for future Docker deployment.
requirements.txt	All Python dependencies.

3. System Entry Point

Entire application is started using:

streamlit run home.py

Run Locally
pip install -r requirements.txt
streamlit run home.py

Run With Virtual Environment (recommended)
python -m venv venv
venv\Scripts\activate       # Windows
pip install -r requirements.txt
streamlit run home.py


4. Video Demonstration


Heart-disease risk assessment walkthrough

Drug recommendation module

SHAP visual explanations

Medical chatbot functionality



5. Deployment Strategy

Current Deployment
Runs locally via Streamlit using home.py
Lightweight, CPU-friendly ML models
Ideal for prototypes & academic demonstrations

Future (Optional) Deployment
Docker → AWS EC2 / Streamlit Cloud

6. Monitoring & Metrics

PulseAI includes performance monitoring & risk evaluation strategies:

Tools

Streamlit logging 
Manual latency + drift monitoring
SHAP explainability for model transparency
Metrics Tracked
Accuracy, Recall, AUC-ROC
Inference latency (<1 sec target)
Input distribution drift
Feature importance (SHAP)
Model confidence scores

7. Project Documentation

All reports/templates are stored in:

documentation/
Performance & Metrics Report
Final Report

8. Acknowledgements

Datasets from:

UCI Heart Disease Dataset
Kaggle Heart Attack Dataset

Models and frameworks:

scikit-learn, imbalanced-learn
LightGBM
SHAP
Streamlit