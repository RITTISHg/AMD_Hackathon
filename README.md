<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=28&duration=3000&pause=1000&color=EF4444&center=true&vCenter=true&multiline=true&repeat=true&width=700&height=100&lines=%E2%9A%A1+EcoWatch+%E2%80%94+Edge+AI+Power+Monitor;AMD+Hackathon+2026+Submission+%F0%9F%8F%86" alt="AMD Hackathon Title" />
</div>

<p align="center">
  <img src="https://img.shields.io/badge/AMD-Hackathon-EF4444?style=for-the-badge&logo=amd&logoColor=white" />
  <img src="https://img.shields.io/badge/React-18.3-61DAFB?style=for-the-badge&logo=react&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3.11-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/ONNX-Edge_AI-005C8A?style=for-the-badge&logo=onnx&logoColor=white" />
  <img src="https://img.shields.io/badge/ESP32-Hardware-222222?style=for-the-badge&logo=espressif&logoColor=white" />
</p>

---

## 🎯 Project Overview

This is the official submission for the **AMD Hackathon**. 

**EcoWatch** is a full-stack, end-to-end hardware and software solution designed to monitor, track, and optimize power and water consumption across campuses, hostels, and lab facilities. By combining **ESP32 Edge Hardware**, **Machine Learning Models (optimized via ONNX)**, and a **Gamified React Dashboard**, this project actively reduces energy waste and encourages sustainable behavior.

> ⚡ **Edge AI & Performance:** All machine learning models (Isolation Forest, Ridge Regression, K-Means) have been optimized and converted to **ONNX format** to ensure blazing-fast inference speeds, making it ideal for deployments on AMD-powered edge servers.

<br/>

## ✨ Core Features

### 🔌 1. Hardware-in-the-Loop (ESP32)
- **Live Telemetry:** Tracks real-time Current, Voltage, and Power at the source.
- **Serial / MQTT Bridge:** Directly pushes high-frequency consumption data to the backend.

### 🧠 2. Edge AI & Machine Learning Backend
- **Anomaly Detection (Isolation Forest):** Instantly flags equipment left running, leaks, or unusual power spikes.
- **Consumption Forecasting (Ridge Regression):** Predicts energy and water usage 24–72 hours into the future.
- **Pattern Classification (K-Means Clustering):** Clusters different campus zones into 'Efficient', 'Normal', 'Wasteful', or 'Erratic' profiles.
- **ONNX Inference Engine:** Models are exported to `.onnx` for minimal latency and lower compute overhead!

### 🎮 3. Gamified & Role-Based Dashboard
- **Live Usage Cards:** Beautiful glassmorphism UI showing energy tracking and RAG (Red/Amber/Green) statuses.
- **Eco-Leaderboards:** Students and floors earn points and "streaks" for reducing baseline energy use.
- **Role-Based Access:** 
  - 🎓 **Students:** View floor data, personal rank, and receive localized nudges.
  - 🔬 **Lab In-Charge:** Analyze heavy machinery power loops and costs.
  - 🏢 **Facility Manager:** Campus-wide insights, CO2 reduction summaries, and ML savings potentials.
- **Smart Nudges:** Instantly pings users when anomalies (like a heater left on) are detected.

### 🔒 4. Enterprise-Grade Security
- API securely decoupled with Rate Limiting, strict CORS rules, and secure HTTP Headers embedded directly in the Flask application.

<br/>

## 🛠️ Technology Stack

| Domain | Tech |
|---|---|
| **Frontend** | React 18, TypeScript, Tailwind CSS, Vite, Recharts, Lucide Icons |
| **Backend API**| Python 3, Flask, CORS, Ratelimit Security |
| **AI / ML** | Scikit-Learn, ONNX Runtime, Pandas, Numpy |
| **Hardware** | ESP32 Microcontroller, C++, Serial Communication |

<br/>

## 📁 Repository Structure

```text
📦 AMD_Hackathon
├── 📂 harware_code/        ← 🔌 ESP32 Firmware & Sensor integration
├── 📂 ml_backend/          ← 🧠 Python Edge-AI API Layer
│   ├── app.py              # Secure Flask API
│   ├── convert_to_onnx.py  # Model-to-ONNX pipeline
│   ├── models/             # PyTorch / Scikit-Learn Model sources
│   └── onnx_models/        # High-performance compiled ONNX graphs
└── 📂 src/                 ← ⚛️ Gamified Web Dashboard (React/Vite)
    ├── components/         # Reusable Tailwind UI components
    ├── pages/              # ML Insights, Leaderboard, Forecasts 
    └── data/               # Live websocket/serial simulation connectors
```

<br/>

## 🚀 Quick Start Guide

### 1. Running the Hardware Node
```bash
# Navigate to hardware code
cd harware_code/EnergyMonitor
# Flash the code to your ESP32 board using Arduino IDE or PlatformIO
```

### 2. Spinning up the Edge AI Backend (Flask)
```bash
cd ml_backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt

# Run the secure ML backend mapping predictions locally
python app.py
```
> Running at: `http://localhost:5000/api/`

### 3. Launching the React Dashboard
```bash
# On a new terminal, from the project root:
npm install
npm run dev
```
> View the live UI at: `http://localhost:5173`

<br/>

## 🔌 API Documentation (ML Engine)

| Endpoint | Purpose |
|:--|:--|
| `GET /api/health` | Service health & ONNX engine validation |
| `GET /api/anomalies` | Fast anomaly detection using Isolation Forest |
| `GET /api/forecast` | Ridge Regression predictions for the next 48 hours |
| `GET /api/patterns` | K-Means clustering of consumption behavior |
| `GET /api/recommendations`| AI-driven energy saving insights tailored to the cluster |

<br/>

## 🤝 Contribution & Links
This project was strictly developed for the **AMD Hackathon**. 
- **Repository:** [https://github.com/RITTISHg/AMD_Hackathon](https://github.com/RITTISHg/AMD_Hackathon)

<p align="center">
  <sub>Built for performance. Built for sustainability. Powered by AMD.</sub>
</p>
