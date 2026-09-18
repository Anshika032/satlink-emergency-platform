# 🚀 SatLink — Edge-AI Emergency Response Platform

> **An Edge-AI powered emergency response system that detects hazards, identifies their location, and triggers SOS alerts through a centralized monitoring dashboard.**

## 🌍 Overview

**SatLink** combines Computer Vision, Edge AI, GPS, backend APIs, and emergency communication to provide rapid detection and reporting of hazardous events.

The system can detect events such as **fire and smoke**, attach their geographic location, generate an SOS, notify responders, and display the incident on a live emergency dashboard.

### Core Pipeline

```text
Camera / Edge Device
        ↓
   AI Detection
        ↓
 Event + Confidence
        ↓
      GPS
        ↓
   FastAPI Backend
        ↓
     SOS Engine
        ↓
 Communication Layer
        ↓
 Emergency Dashboard
```

---

## ✨ Key Features

* 🤖 **AI-based hazard detection** using YOLO + OpenCV
* 📍 **GPS-based event localization**
* 🚨 **Automatic SOS generation**
* 📡 **Satellite communication abstraction** for emergency messaging
* 📱 **Twilio SMS / voice alerts**
* 🗺️ **Interactive Leaflet emergency map**
* 📋 **Persistent SOS and incident logs**
* 🖼️ **AI event evidence/images**
* 🌦️ **Weather intelligence**
* 🆘 **Manual SOS triggering**
* 💻 **Multi-device/LAN event communication**

---

## 🏗️ Architecture

```text
             ┌──────────────┐
             │ Camera/Edge  │
             └──────┬───────┘
                    ↓
             ┌──────────────┐
             │   YOLO AI    │
             └──────┬───────┘
                    ↓
             ┌──────────────┐
             │ Event + GPS  │
             └──────┬───────┘
                    ↓
             ┌──────────────┐
             │   FastAPI    │
             │   Backend    │
             └──────┬───────┘
                    ↓
             ┌──────────────┐
             │  SOS Engine  │
             └──────┬───────┘
                    ↓
        ┌───────────┴───────────┐
        ↓                       ↓
   Communication            Dashboard
   (Twilio/Satellite)       (Map + Logs)
```

The AI detection layer can run on a separate device from the backend, allowing the system to distribute computation across multiple machines.

---

## 🛠️ Tech Stack

| Layer         | Technologies                |
| ------------- | --------------------------- |
| AI / Vision   | YOLO, OpenCV, Python        |
| Backend       | FastAPI, Uvicorn, Pydantic  |
| Frontend      | HTML, CSS, JavaScript       |
| Maps          | Leaflet.js, OpenStreetMap   |
| Communication | Twilio, Satellite Adapter   |
| Storage       | JSON-based SOS logs         |
| Deployment    | Local / LAN-based prototype |

---

## 📂 Project Structure

```text
satlink-emergency-platform/
│
├── backend/
│   ├── main.py
│   ├── config.py
│   ├── ai_event_receiver.py
│   ├── cleanup_logs.py
│   ├── satellite/
│   └── utils/
│
├── frontend/
│   ├── index.html
│   ├── sos.html
│   ├── sos.js
│   └── emergency_response.html
│
├── requirements.txt
├── package.json
└── README.md
```

---

## ⚙️ Installation

```bash
git clone https://github.com/Anshika032/satlink-emergency-platform.git
cd satlink-emergency-platform

python -m venv venv
venv\Scripts\activate

pip install -r requirements.txt
```

Run the backend:

```bash
cd backend
uvicorn main:app --reload
```

API documentation:

```text
http://127.0.0.1:8000/docs
```

Serve the frontend using any local web server and configure it to communicate with the FastAPI backend.

---

## 🚨 Example Workflow

```text
Fire detected by camera
        ↓
YOLO identifies fire
        ↓
Confidence threshold verified
        ↓
GPS coordinates attached
        ↓
AI alert sent to backend
        ↓
SOS generated
        ↓
Notification sent
        ↓
Event logged
        ↓
Location + evidence displayed
on emergency dashboard
```

---

## 🔮 Future Scope

* Raspberry Pi / dedicated edge deployment
* Real satellite modem integration
* LoRa/RF communication fallback
* Real-time WebSocket alerts
* PostgreSQL/database integration
* Authentication and role-based access
* Hardware-accelerated AI inference
* Offline-first emergency operation

> **Note:** The current satellite communication component is a prototype abstraction/simulation and is not direct communication with an operational satellite.

---

## 👩‍💻 Author

**Anshika Shukla**
Electronics & Communication Engineering, Banasthali University

**Interests:** Edge AI • Space Systems • Computer Vision • AI/ML • Emergency Communication

---

## 📄 License

MIT License

---

### ⭐ SatLink

**Detect early. Locate precisely. Communicate reliably.**
