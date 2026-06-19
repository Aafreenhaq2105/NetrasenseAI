# Automated Ophthalmic Disease Detection System
### Using Deep Learning and Retinal Imaging
#### Powered by RetinaScan AI Engine

![Status](https://img.shields.io/badge/Status-Active_Development-orange?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python)
![Flask](https://img.shields.io/badge/Flask-3.0-black?style=for-the-badge&logo=flask)
![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0-EE4C2C?style=for-the-badge&logo=pytorch)
![Blockchain](https://img.shields.io/badge/Blockchain-Ethereum-3C3C3D?style=for-the-badge&logo=ethereum)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Contributors](https://img.shields.io/badge/Team-4_Members-purple?style=for-the-badge)

---

## The Problem

According to WHO 2023 over 2.2 billion people globally suffer from
vision impairment. In India alone there is 1 ophthalmologist for
every 70,000 people. 80% of all blindness cases are preventable if
detected at an early stage. Rural clinics across developing nations
lack access to specialist equipment and trained professionals. By the
time diseases like Diabetic Retinopathy or Glaucoma are identified
through traditional methods irreversible damage has already occurred.
There exists a critical need for an automated accessible and
explainable diagnostic system that can function without specialist
supervision.

---

## What This Project Does

A nurse at a rural clinic takes a photo of a patient eye and uploads
it to our system. Within seconds the AI identifies which diseases are
present highlights exactly where in the eye the problem is located
and generates a full clinical report the doctor can read and act on
immediately. Every diagnosis is permanently recorded on Blockchain
for a tamper proof audit trail. Patient vitals from IoT connected
devices stream directly into the system for complete diagnosis.

---

## Diseases Detected

| Disease | Description |
|---|---|
| Diabetic Retinopathy | Blood vessel damage caused by diabetes |
| Glaucoma | Optic nerve damage leading to blindness |
| Hypertensive Retinopathy | Retinal damage from high blood pressure |
| Macular Degeneration | Central vision loss common after age 50 |
| Normal | No disease detected healthy eye |

---

## System Architecture

Eye Photo Uploaded by Clinic Worker
-> Image Preprocessing using OpenCV and CLAHE Enhancement
-> EfficientNetB4 Deep Learning Model analyzes the image
-> Multi Label Classification outputs probability for each disease
-> Grad-CAM generates heatmap showing exact disease location in eye
-> XGBoost model processes patient clinical data age BP sugar levels
-> Fusion Layer combines image result and clinical data result
-> RAG Engine searches 500 medical research papers using LangChain and FAISS
-> Mistral LLM generates structured clinical explanation
-> PDF Report automatically created and saved
-> Ethereum Blockchain permanently logs the diagnosis
-> PostgreSQL Database saves full patient history
-> MCP Agent handles intelligent doctor queries and follow up questions
-> React Dashboard displays everything to the doctor

---

## AI and ML Pipeline

Step 1 - Raw fundus eye image is uploaded by clinic worker
Step 2 - OpenCV removes noise and enhances contrast using CLAHE
Step 3 - Image resized to 224x224 pixels and normalized
Step 4 - EfficientNetB4 with ImageNet pretrained weights analyzes image
Step 5 - Model outputs probability score for each of 5 diseases
Step 6 - Grad-CAM highlights which region of retina triggered prediction
Step 7 - XGBoost processes patient age blood pressure blood sugar levels
Step 8 - Fusion layer combines both model outputs into final prediction
Step 9 - LangChain retrieves relevant content from medical PDF database
Step 10 - Mistral 7B LLM writes human readable clinical report
Step 11 - Report exported as PDF and stored in database
Step 12 - Web3.py logs diagnosis hash to Ethereum smart contract
Step 13 - MCP Agent answers follow up questions from doctor intelligently
Step 14 - Doctor views full results on React dashboard

---

## Model Performance

Results will be updated as training progresses

| Disease | Accuracy | AUC-ROC | F1 Score | Precision | Recall |
|---|---|---|---|---|---|
| Diabetic Retinopathy | updating | updating | updating | updating | updating |
| Glaucoma | updating | updating | updating | updating | updating |
| Hypertensive Retinopathy | updating | updating | updating | updating | updating |
| Macular Degeneration | updating | updating | updating | updating | updating |
| Overall System | updating | updating | updating | updating | updating |

---

## Evaluation Strategy

| Metric | Purpose |
|---|---|
| AUC-ROC per disease | Measures model discrimination ability |
| F1 Score | Balances precision and recall for imbalanced data |
| Confusion Matrix | Shows exact correct and wrong predictions per disease |
| Grad-CAM Score | Validates explainability heatmap quality |
| Precision and Recall | Measures false positive and false negative rate |
| Cohen Kappa Score | Measures agreement with ophthalmologist diagnosis |
| Classification Report | Full breakdown of model performance per class |

---

## Tech Stack

| Category | Technologies Used |
|---|---|
| Deep Learning | EfficientNetB4, PyTorch, Transfer Learning, Fine Tuning |
| Explainability | Grad-CAM Heatmap Visualization |
| Classical ML | XGBoost, Scikit-learn, Feature Engineering |
| Feature Engineering | Pandas, NumPy, StandardScaler, LabelEncoder |
| RAG Pipeline | LangChain, FAISS, ChromaDB, Vector Embeddings |
| LLM | Mistral 7B via HuggingFace |
| GenAI Libraries | HuggingFace Transformers, Diffusers, PEFT, LoRA |
| Embeddings | Sentence Transformers |
| AI Agent | Claude MCP for intelligent doctor query handling |
| Backend | Flask, SQLAlchemy, JWT Authentication, REST API |
| Database | PostgreSQL |
| Blockchain | Solidity Smart Contract, Web3.py, Ethereum, Ganache |
| IoT Integration | MQTT Protocol, Paho-MQTT, Simulated BP Monitor, Glucometer and SpO2 Sensor Data Streaming |
| Frontend | React.js 18, Tailwind CSS, Chart.js, Axios |
| Deployment | Docker, Vercel, Railway, HuggingFace Spaces |
| Training | Google Colab T4 GPU Free Tier |
| Version Control | Git and GitHub with Branch Strategy |

---

## Dataset

| Dataset | Total Images | Disease Coverage | Source |
|---|---|---|---|
| APTOS 2019 | 3662 images | Diabetic Retinopathy 5 severity levels | Kaggle |
| ODIR 2019 | 10000 patients | 8 eye conditions including Glaucoma and AMD | Kaggle |
| RFMiD | 3200 images | 45 retinal diseases multi label | Kaggle |

All datasets are publicly available and free to download on Kaggle.
All model training performed on Google Colab using free T4 GPU.
Training notebooks available in the notebooks folder of this repository.

---

## Project Structure

retinascan-ai/
|
|-- notebooks/
|   |-- 01_EDA_Visualization.ipynb
|   |-- 02_Preprocessing_CLAHE.ipynb
|   |-- 03_CNN_EfficientNet_Training.ipynb
|   |-- 04_GradCAM_Explainability.ipynb
|   |-- 05_Feature_Engineering.ipynb
|   |-- 06_Evaluation_Metrics.ipynb
|   |-- 07_RAG_Pipeline.ipynb
|
|-- backend/
|   |-- app.py
|   |-- config.py
|   |-- routes/
|   |-- models/
|   |-- rag/
|   |-- blockchain/
|   |-- database/
|
|-- frontend/
|   |-- src/
|       |-- pages/
|       |-- components/
|
|-- smart_contracts/
|   |-- RetinaAudit.sol
|
|-- iot_simulator/
|   |-- vitals_stream.py
|
|-- docs/
|-- docker-compose.yml
|-- requirements.txt
|-- .env.example
|-- CONTRIBUTING.md
|-- README.md

---

## Live Demo

Deployment in progress - links will be updated in final phase

Frontend Dashboard - coming soon on Vercel
Backend API - coming soon on Railway
AI Model - coming soon on HuggingFace Spaces

---

## Development Roadmap

- [x] Project planning and system design
- [x] GitHub repository setup
- [x] README documentation
- [x] Team collaboration setup
- [ ] Dataset download and exploration on Kaggle
- [ ] Image preprocessing pipeline with CLAHE
- [ ] EfficientNetB4 model training on Google Colab
- [ ] Grad-CAM explainability implementation
- [ ] Clinical data feature engineering
- [ ] XGBoost clinical prediction model
- [ ] Multimodal fusion layer combining both models
- [ ] RAG pipeline setup with medical research papers
- [ ] Mistral LLM clinical report generation
- [ ] Flask REST API development
- [ ] PostgreSQL database integration
- [ ] Blockchain audit logging with Ethereum
- [ ] IoT vitals simulator with MQTT
- [ ] MCP agent integration for doctor queries
- [ ] React.js dashboard development
- [ ] UI UX design on Figma before coding frontend
- [ ] Docker containerization
- [ ] Cloud deployment on Vercel and Railway
- [ ] Evaluation metrics and model comparison report
- [ ] SRS document preparation
- [ ] Final presentation and demo video recording
- [ ] Final testing and submission

---

## Team

| Name | Role | GitHub | LinkedIn |
|---|---|---|---|
| Aafreen Haq - Lead | Project Lead, Deep Learning, System Architecture | https://github.com/Aafreenhaq2105 | https://www.linkedin.com/in/aafreen-haq-a27580373 |
| Vrutant Kar | Backend Development, Flask API, Database, RAG | https://github.com/vrutantkar550-png | https://www.linkedin.com/in/vrutant-kar-5898b229a |
| Sanskar Shinde | Frontend Development, React Dashboard, UI UX | https://github.com/sanskarshinde2906 | https://www.linkedin.com/in/sanskar-shinde-216a643a0 |
| Chandra Mouli | Blockchain, IoT Integration, Docker, Deployment | https://github.com/ChandraMouli21 | https://www.linkedin.com/in/chandra-mouli-143344270 |

Institution - Sandip University
Degree - Final Year B.Tech Artificial Intelligence and Machine Learning
Academic Year - 2025-2026
Project Guide - To be allotted

---

## Research References

1. WHO Global Vision Report 2023 - Vision Atlas
2. APTOS 2019 Blindness Detection Challenge - Kaggle
3. ODIR 2019 Ocular Disease Intelligent Recognition - ICHA
4. EfficientNet Rethinking Model Scaling for CNNs - Tan and Le 2019
5. Grad-CAM Visual Explanations from Deep Networks - Selvaraju 2017
6. Retrieval Augmented Generation for Knowledge Intensive NLP - Lewis et al 2020
7. Ethereum Whitepaper - Vitalik Buterin
8. LangChain Framework for LLM Applications - Chase 2022
9. XGBoost A Scalable Tree Boosting System - Chen and Guestrin 2016
10. MQTT Protocol Standard - OASIS 2019

---

## License

This project is licensed under the MIT License.
See the LICENSE file for full details.

---

Automated Ophthalmic Disease Detection System
Final Year Capstone Project - Group of 4
Built for rural healthcare access across India
Sandip University - Academic Year 2025-2026
