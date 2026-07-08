# 🧠 PenCap AI – Anomaly Detection in Pen Production
<img width="1012" height="842" alt="Screenshot 2026-07-08 084117" src="https://github.com/user-attachments/assets/fce4659b-ea0b-4edc-980e-53f7a374682c" />
<img width="1068" height="857" alt="Screenshot 2026-07-08 084151" src="https://github.com/user-attachments/assets/713bbce6-52ee-4abe-a342-c0618696e339" />
<img width="1062" height="857" alt="Screenshot 2026-07-08 084219" src="https://github.com/user-attachments/assets/378d1253-e854-4c2d-a951-aebed075c205" />

A real-time computer vision system that detects whether a pen is **capped or uncapped** using a live camera feed. Designed as a lightweight solution for automated quality inspection using just a smartphone.

---

## 🚀 Overview

PenCap AI combines **YOLOv8 object detection** with a **web-based interface** to enable real-time defect detection. The system uses a mobile camera stream (via IP Webcam) and processes frames through a FastAPI backend.

---

## 🛠️ Tech Stack

* **Backend:** Python, FastAPI, Uvicorn
* **Model:** YOLOv8 (Ultralytics), PyTorch
* **Frontend:** HTML, CSS, JavaScript
* **Libraries:** OpenCV, NumPy

---

## ✨ Key Features

* 📷 Live camera feed using mobile (IP Webcam)
* ⚡ Real-time detection via API
* 🎯 Detects **CAPPED vs UNCAPPED**
* 🔄 Manual correction for improving accuracy
* 📊 Live detection statistics
* 💾 Dataset generation for retraining

---

## ⚙️ Project Setup

### 1️⃣ Extract Project Files

```bash
unzip frontend.zip
unzip backend.zip
```

---

### 2️⃣ Setup Backend

```bash
cd backend
python -m venv venv
```

#### Activate Virtual Environment

```bash
# Windows
venv\Scripts\activate

# Mac/Linux
source venv/bin/activate
```

#### Install Dependencies

```bash
pip install -r requirements.txt
```

#### Run Server

```bash
uvicorn main:app --reload
```

Backend runs at:

```
http://127.0.0.1:8000
```

---

### 3️⃣ Setup Frontend

```bash
cd frontend
```

Run using simple server:

```bash
python -m http.server 5500
```

Open in browser:

```
http://localhost:5500
```

---

## 📱 Mobile Camera Integration (IP Webcam)

This project uses your phone as a live camera.

### Steps:

1. Install **IP Webcam** app on your phone
2. Connect phone and laptop to **same WiFi**
3. Open app → Start Server
4. You will get a URL like:

```
http://192.168.1.5:8080
```

---

### 🔗 Connect to Frontend

* Open your frontend in browser
* Enter the IP Webcam URL in the input field
* Example:

```
http://192.168.1.5:8080/video
```

Now your mobile camera stream will be used for detection 🎉

---

## 🔗 API Endpoints

* `GET /health` → Server status
* `POST /predict` → Run detection
* `POST /save` → Save corrected data
* `GET /stats` → View stats

---

## ⚙️ Workflow

1. Mobile camera streams video
2. Frontend captures frames
3. Frames sent to backend API
4. YOLO model processes image
5. Result displayed in UI
6. User verifies/corrects prediction

---

## 📈 Highlights

* Real-time detection using **mobile camera**
* No expensive hardware required
* API-driven scalable design
* Human-in-the-loop learning system

---

## 🔮 Future Improvements

* Cloud deployment (AWS)
* Automated model retraining
* Multi-object detection
* Production line integration

---

## 👩‍💻 Author

**Thanushree D N**
📧 [thanushreedn2003@gmail.com](mailto:thanushreedn2003@gmail.com)
🔗 https://www.linkedin.com/in/thanushree-d-n-74b979354/

---

⭐ *Turning real-world inspection into intelligent automation.*
