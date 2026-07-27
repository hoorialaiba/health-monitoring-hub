# 🩺 Health Monitoring Hub (HMH)

![Frontend](https://img.shields.io/badge/Frontend-React-blue)
![Backend](https://img.shields.io/badge/Backend-Node.js-green)
![Database](https://img.shields.io/badge/Database-PostgreSQL-blueviolet)
![OCR](https://img.shields.io/badge/OCR-PaddleOCR-red)
![ML](https://img.shields.io/badge/ML-Random%20Forest-orange)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
[![Live Demo](https://img.shields.io/badge/Live-Demo-success?style=flat-square)](https://health-monitoring-hub-navy.vercel.app/)

Health Monitoring Hub (HMH) is a full-stack AI-powered web application developed as a Final Year Project to simplify Complete Blood Count (CBC) report analysis. The system extracts values from uploaded CBC reports using OCR, predicts possible hematological disorders using machine learning, provides AI-generated health recommendations, and helps users track health trends over time.

## Live Demo

A deployed version of Health Monitoring Hub is available here:

https://health-monitoring-hub-navy.vercel.app/

> **Disclaimer:** This project is intended for educational and awareness purposes only. It is not a substitute for professional medical advice, diagnosis, or treatment.

---

## Project Highlights

- Upload CBC reports as JPG or PNG images.
- Extract CBC values automatically using OCR.
- Enter CBC values manually if OCR is unavailable.
- Detect abnormal blood parameters using reference ranges.
- Predict possible hematological disorders using a trained Random Forest model.
- Generate lifestyle and diet recommendations.
- Store report history in PostgreSQL.
- Visualize health trends over time.
- Provide a clean and modern user interface.

---

## Overview

Health Monitoring Hub combines OCR, machine learning, and generative AI to make CBC report interpretation easier for users.

The workflow is:

1. User uploads a CBC report.
2. OCR extracts text from the report.
3. CBC values are parsed into structured form.
4. Values are checked against reference ranges.
5. A Random Forest model predicts possible disorders.
6. AI-generated explanations and recommendations are shown.
7. Reports are stored for history and trend analysis.

---

## Features

### Report Upload & OCR

- Upload CBC reports as JPG or PNG images.
- Use PaddleOCR to extract report text automatically.
- Fall back to manual entry when OCR extraction is not enough.

### Abnormality Detection

- Compare CBC parameters against reference ranges.
- Flag normal, low, high, and critical values.
- Show an overall severity summary.

### ML Prediction

- Predict possible hematological conditions using a trained Random Forest model.
- Show prediction output in a clear and patient-friendly format.

### AI Recommendations

- Generate dietary and lifestyle suggestions.
- Provide readable explanations for CBC abnormalities.
- Show informational medicine suggestions where applicable.

### History & Trends

- Store reports in PostgreSQL.
- Display previous CBC reports.
- Visualize trends over time using charts.

### User Experience

- Clean React UI.
- Responsive layout.
- Secure login and logout flow.

---

## Technology Stack

### Frontend
- React.js
- Vite
- Tailwind CSS

### Backend
- Node.js
- Express.js

### Database
- PostgreSQL

### OCR & AI
- Python
- PaddleOCR
- Scikit-learn
- Random Forest Classifier
- Mistral Small Latest

### Other
- JWT Authentication
- Recharts
- Git & GitHub

---

## My Contribution

My primary role in this project was the AI/ML pipeline.

I worked on:

- OCR text extraction using PaddleOCR
- CBC parsing and preprocessing
- Random Forest model training for hematological disorder prediction
- Integration of the trained model with the backend
- Integration of Mistral-based recommendations
- Python AI services

---

## Machine Learning Model

The disease prediction module uses a supervised Random Forest classifier trained on CBC-related features.

### Input Features
- RBC
- WBC
- Hemoglobin (Hb)
- Hematocrit (HCT)
- Platelets
- MCV
- MCH
- MCHC
- RDW

---

## OCR Pipeline

1. User uploads a CBC report.
2. PaddleOCR extracts text from the image.
3. Custom parsing logic identifies CBC parameters.
4. Structured values are passed to the analysis module.
5. Results are displayed on the analysis page.

---

## System Architecture

```text
User
  ↓
React Frontend
  ↓
Node.js / Express API
  ↓
Python OCR Service (PaddleOCR)
  ↓
CBC Parsing + Preprocessing
  ↓
Random Forest Prediction
  ↓
Mistral Recommendations
  ↓
PostgreSQL Storage
```

---

## Repository Structure

```text
health-monitoring-hub/
│
├── backend/
│   ├── routes/
│   ├── services/
│   ├── ocr-code/
│   ├── ocr-service/
│   ├── server.js
│   └── package.json
│
├── frontend/
│   ├── src/
│   ├── components/
│   ├── pages/
│   └── package.json
│
├── screenshots/
│   ├── home.jpeg
│   ├── upload.jpeg
│   ├── analysis.png
│   ├── recommendations.png
│   └── trends.png
│
└── README.md
```

---

## Screenshots

### Home Page
![Home](screenshots/home.jpeg)

### Upload / Manual Entry
![Upload](screenshots/upload.jpeg)

### CBC Analysis
![Analysis](screenshots/analysis.png)

### AI Recommendations
![Recommendations](screenshots/recommendations.png)

### Health Trends
![Trends](screenshots/trends.png)

---

## How It Works

1. Log in to the application.
2. Upload a CBC report or enter values manually.
3. View extracted CBC values and abnormal findings.
4. See the machine learning-based prediction.
5. Read AI-generated recommendations.
6. Review previous reports and health trends.

---

## Setup

### Frontend

```bash
cd frontend
npm install
npm run dev
```

### Backend

```bash
cd backend
npm install
npm start
```

### OCR Service

```bash
cd backend/ocr-service
pip install -r requirements.txt
python app.py
```

### Database

Make sure PostgreSQL is running and the connection details are configured in the backend environment file.

Example:

```env
DATABASE_URL=postgres://username:password@localhost:5432/health_monitoring_hub
```

---
## 🌐 Live Demo

🚀 Try the application here:

**https://health-monitoring-hub-navy.vercel.app/**

or simply click:

👉 **[Health Monitoring Hub Live Demo](https://health-monitoring-hub-navy.vercel.app/)**

> The deployed application allows you to explore the user interface and core workflow of the project.

---
## Future Improvements

- Support more CBC report formats.
- Improve OCR accuracy for different lab layouts.
- Expand the machine learning model with larger datasets.
- Add doctor and hospital dashboards.
- Improve trend analytics and reporting.
- Add PDF export for analysis reports.

---

## Academic Information

Developed as a Final Year Project for the Bachelor of Software Engineering program at the University of the Punjab.

---

## Author

**Hooria Laiba**  
Software Engineering Graduate  
University of the Punjab (PUCIT)
