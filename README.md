# 🫀 PulseAI - Cardiovascular Risk Assessment System

**Project by:** Kunal Jagtap | MSAIS

---

## 📋 Overview

PulseAI is an intelligent cardiovascular risk assessment platform that leverages machine learning to predict heart disease risk. The system analyzes clinical markers including age, cholesterol levels, blood pressure, chest pain type, smoking habits, and other vital indicators to provide comprehensive health insights.

### Key Features

- **🎯 Risk Classification**: Categorizes cardiovascular risk as Low, Moderate, or High
- **💊 Drug Recommendations**: Suggests appropriate medications and drug classes based on risk profile
- **📊 SHAP Explainability**: Visual explanations of model predictions for transparency
- **🤖 Medical Chatbot**: AI-powered medical guidance system
- **📈 Lifestyle Suggestions**: Personalized health recommendations

---

## 🏗️ System Architecture

```
Predictive-Analytics-For-Health-Monitoring/
│
├── 📁 Drug Recommendation/           # Drug/drug-class suggestion module
├── 📁 heart_disease_risk_assessment/ # ML pipeline & model assets
├── 📁 medibot/                       # Medical chatbot & vector DB
├── 📁 models/                        # Serialized ML models (.pkl)
├── 📁 pages/                         # Streamlit sub-pages
├── 📁 vectorstore/                   # Embeddings for chatbot retrieval
├── 📁 utils/                         # Helper scripts & utilities
├── 📁 documentation/                 # Reports & documentation
│
├── 🐳 Dockerfile                     # Container configuration
├── 🏠 home.py                        # Main application entry point
├── 📄 requirements.txt               # Python dependencies
├── 📄 .env                           # Environment variables
└── 📖 README.md
```

### Component Overview

| Component | Purpose |
|-----------|---------|
| **home.py** | Main Streamlit application entry point |
| **Drug Recommendation/** | Symptom-based drug category suggestions |
| **heart_disease_risk_assessment/** | Complete ML pipeline with SHAP explainability |
| **models/** | EasyEnsembleClassifier and other trained models |
| **medibot/** | LLM-driven medical Q&A with vector retrieval |
| **pages/** | Multi-page Streamlit UI routes |
| **vectorstore/** | Medical knowledge embeddings storage |
| **utils/** | Feature engineering & data processing tools |

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- pip package manager

### Installation & Setup

#### Option 1: Quick Start

```bash
# Install dependencies
pip install -r requirements.txt

# Launch application
streamlit run home.py
```

#### Option 2: Virtual Environment (Recommended)

```bash
# Create virtual environment
python -m venv venv

# Activate environment
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run application
streamlit run home.py
```

#### Option 3: Docker (Future Deployment)

```bash
# Build image
docker build -t pulseai .

# Run container
docker run -p 8501:8501 pulseai
```

---

## 🎥 Demo & Features

The system demonstrates:

- ✅ **Interactive Risk Assessment** - Real-time cardiovascular risk prediction
- ✅ **Drug Recommendation Engine** - Intelligent medication suggestions
- ✅ **SHAP Visualizations** - Model explainability and feature importance
- ✅ **Medical Chatbot** - Context-aware health guidance

---

## 📊 Monitoring & Performance

### Metrics Tracked

- **Model Performance**: Accuracy, Recall, AUC-ROC
- **Inference Speed**: Target latency < 1 second
- **Data Quality**: Input distribution drift detection
- **Explainability**: SHAP feature importance scores
- **Confidence**: Model prediction confidence levels

### Monitoring Tools

- Streamlit built-in logging
- Manual latency tracking
- SHAP explainability dashboards
- Distribution drift monitoring

---

## 🔬 Technical Stack

### Machine Learning

- **scikit-learn** - Core ML framework
- **imbalanced-learn** - Class imbalance handling
- **LightGBM** - Gradient boosting models
- **SHAP** - Model interpretability

### Application Framework

- **Streamlit** - Interactive web interface
- **Python 3.8+** - Core programming language

### Data Sources

- UCI Heart Disease Dataset
- Kaggle Heart Attack Dataset

---

## 📁 Documentation

Comprehensive project documentation available in `documentation/`:

- Performance & Metrics Report
- Final Project Report
- Model Evaluation Results

---

## 🚀 Deployment Strategy

### Current Setup
- **Local Deployment**: Streamlit application via `home.py`
- **Lightweight Models**: CPU-friendly inference
- **Use Case**: Prototyping and academic demonstrations

### Future Roadmap
- **Containerization**: Docker deployment
- **Cloud Hosting**: AWS EC2 or Streamlit Cloud
- **Scalability**: Multi-user concurrent access

---

## 🙏 Acknowledgements

This project builds upon excellent open-source resources and datasets:

- **Datasets**: UCI Machine Learning Repository, Kaggle Community
- **Frameworks**: scikit-learn, Streamlit, SHAP contributors
- **Community**: Open-source ML and healthcare informatics communities

---

## 📧 Contact

**Kunal Jagtap**  
MSAIS Program  

---

<div align="center">

**⭐ If you find this project useful, please consider giving it a star!**

Made with ❤️ for better cardiovascular health outcomes

</div>
