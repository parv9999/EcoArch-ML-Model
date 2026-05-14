# 🌿 EcoArch-ML-API

[![Live Demo](https://img.shields.io/badge/Live%20Demo-eco--arch--ml--api.vercel.app-brightgreen?style=for-the-badge&logo=vercel)](https://eco-arch-ml-api.vercel.app)
![Python](https://img.shields.io/badge/Python-67.9%25-3776AB?style=for-the-badge&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-32.1%25-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![ML](https://img.shields.io/badge/ML-Random%20Forest-orange?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-Frontend-black?style=for-the-badge&logo=next.js)

> An AI-powered API that predicts **energy consumption**, **carbon footprint**, **cooling load**, and **roof type recommendations** for architectural projects — bringing machine learning to sustainable building design.

---

## 🌐 Live Demo

🔗 **[eco-arch-ml-api.vercel.app](https://eco-arch-ml-api.vercel.app)**

---

## 📋 Table of Contents

- [About](#about)
- [Features](#features)
- [ML Models](#ml-models)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [API Endpoints](#api-endpoints)
- [Deployment](#deployment)
- [Author](#author)

---

## 📖 About

**EcoArch-ML-API** is a full-stack application combining a **Python ML backend** with a **Next.js frontend** to help architects and engineers make eco-conscious design decisions. By inputting building parameters, users receive ML-driven predictions on sustainability metrics.

---

## ✨ Features

- 🔋 **Energy Consumption Prediction** — Estimate a building's energy usage
- 🌫️ **Carbon Footprint Estimation** — Predict CO₂ emissions from building design
- ❄️ **Cooling Load Forecasting** — Calculate cooling requirements based on design inputs
- 🏠 **Roof Type Recommendation** — ML-based suggestion for optimal roof type
- ⚡ **REST API** — Clean endpoints powered by Python (Flask/FastAPI)
- 🖥️ **Interactive UI** — Next.js frontend for easy model interaction

---

## 🤖 ML Models

All models are trained using **Random Forest** algorithms and serialized as `.pkl` files:

| Model File | Predicts | Algorithm |
|---|---|---|
| `energy_model.pkl` | Energy consumption (kWh) | Random Forest Regressor |
| `carbon_model.pkl` | Carbon emissions (CO₂ kg) | Random Forest Regressor |
| `cooling_model.pkl` | Cooling load (kW) | Random Forest Regressor |
| `roof_type_model.pkl` | Optimal roof type | Random Forest Classifier |
| `roof_type_mapping.pkl` | Roof label encoding | Label Encoder |

> Models evaluated using **Mean Absolute Error (MAE)** and **Accuracy Score** metrics.

---

## 🛠️ Tech Stack

### Backend
- **Python** — Core ML logic
- **scikit-learn** — Random Forest models
- **Flask / FastAPI** — REST API server
- **pandas / numpy / seaborn** — Data processing & analysis
- **pickle** — Model serialization

### Frontend
- **Next.js** — React-based frontend framework
- **JavaScript** — Client-side interactivity

### Infrastructure
- **Vercel** — Deployment platform

---

## 📁 Project Structure

```
EcoArch-ML-API/
│
├── pages/                    # Next.js pages (frontend routes)
│
├── app.py                    # Python backend — API server & ML inference
├── requirements.txt          # Python dependencies
│
├── energy_model.pkl          # Trained energy prediction model
├── carbon_model.pkl          # Trained carbon footprint model
├── cooling_model.pkl         # Trained cooling load model
├── roof_type_model.pkl       # Trained roof type classifier
├── roof_type_mapping.pkl     # Roof type label encoder
│
├── next.config.js            # Next.js configuration
├── package.json              # Node.js dependencies
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Node.js 16+
- npm or yarn

### 1. Clone the Repository

```bash
git clone https://github.com/parv9999/EcoArch-ML-API.git
cd EcoArch-ML-API
```

### 2. Set Up the Python Backend

```bash
# Install Python dependencies
pip install -r requirements.txt

# Start the backend server
python app.py
```

### 3. Set Up the Next.js Frontend

```bash
# Install Node dependencies
npm install

# Run the development server
npm run dev
```

Visit `http://localhost:3000` in your browser.

---

## 📡 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/predict/energy` | Predict energy consumption |
| `POST` | `/predict/carbon` | Predict carbon footprint |
| `POST` | `/predict/cooling` | Predict cooling load |
| `POST` | `/predict/roof` | Recommend roof type |

### Example Request

```json
POST /predict/energy
{
  "building_area": 2500,
  "floors": 4,
  "orientation": "south",
  "glazing_ratio": 0.4,
  "insulation_thickness": 0.15
}
```

### Example Response

```json
{
  "predicted_energy_kwh": 48320.5,
  "model": "energy_model",
  "status": "success"
}
```

---

## ☁️ Deployment

This project is deployed on **Vercel** with 18+ deployments.

To deploy your own instance:

```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
vercel
```

> **Note:** Ensure your Python backend is separately hosted (e.g., on Railway, Render, or AWS) and update the API base URL in the frontend config.

---

## 📦 Requirements

Key Python dependencies (`requirements.txt`):

```
scikit-learn
pandas
numpy
seaborn
flask
pickle-mixin
jupyter_client
```

---

## 👤 Author

**parv9999**

- GitHub: [@parv9999](https://github.com/parv9999)
- Live Site: [eco-arch-ml-api.vercel.app](https://eco-arch-ml-api.vercel.app)

---

## 📝 License

This project is open source and available for educational and research use.

---

<p align="center">🌱 Building a greener future with Machine Learning & Architecture</p>
