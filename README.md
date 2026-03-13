# 🩺 Non-Contact Blood Pressure Analysis

![MATLAB](https://img.shields.io/badge/MATLAB-R2023a-orange?style=flat&logo=mathworks)
![Signal Processing](https://img.shields.io/badge/Signal-Processing-blue?style=flat)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-green?style=flat)
![IEEE Published](https://img.shields.io/badge/IEEE-Published-blue?style=flat&logo=ieee)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat)

> A non-contact blood pressure monitoring system that uses a webcam for facial video capture and advanced signal processing to estimate Systolic (SBP) and Diastolic (DBP) blood pressure — without any physical contact or wearable devices.

---

## 📄 Published Research

This project has been published at the **3rd IEEE International Conference on Knowledge Engineering and Communication Systems (ICKECS – 2025)**.

| Detail | Info |
|--------|------|
| **Title** | Non-Contact Blood Pressure Analysis |
| **Conference** | ICKECS 2025, April 28–29, 2025 |
| **Publisher** | IEEE |
| **DOI** | [10.1109/ICKECS65700.2025.11036062](https://doi.org/10.1109/ICKECS65700.2025.11036062) |
| **IEEE Xplore** | [View Paper](https://ieeexplore.ieee.org/document/11036062) |

---

## 📌 Overview

Traditional blood pressure measurement methods involve physical contact, causing discomfort and raising hygiene concerns. This project proposes a **completely non-contact solution** using facial video analysis to estimate blood pressure in real time.

The system:
- Captures facial video using a **standard webcam**
- Extracts **Photoplethysmographic (PPG) signals** from RGB channels
- Applies **Butterworth bandpass filtering** and **PCA** for signal refinement
- Uses **machine learning models** (GAMs and polynomial regression) to predict SBP and DBP
- Validates results against **BHS and AAMI clinical standards**

---

## 📂 Repository Structure

```
Non-Contact-Blood-Pressure-Analysis/
│
├── PPG_Simulation.m                      # Main MATLAB simulation script
├── bloodPressureLinearModel_DBP.mat      # Pre-trained DBP prediction model
├── bloodPressureLinearModel_DBP__1_.mat  # DBP model (alternate version)
├── blood_pressure_mean_std.csv           # Blood pressure mean & std data
├── untitled.mlx                          # MATLAB live script for simulation
└── README.md                             # Project documentation
```

---

## ⚙️ Methodology

### 1. Data Collection & Signal Extraction
- Facial video captured using a webcam at **30 fps**
- Forehead and hand regions used as **Regions of Interest (ROI)**
- **Green channel** analyzed for PPG signal extraction (most sensitive to blood volume changes)

### 2. Signal Preprocessing
- **Butterworth Bandpass Filter** (0.5 Hz – 5 Hz) applied to isolate physiological components and remove motion artifacts
- **Principal Component Analysis (PCA)** used to reduce noise and extract the most relevant signal components

### 3. Feature Extraction
- **Peak detection** to identify heartbeats and calculate pulse intervals
- Features extracted: mean, standard deviation, heart rate, heart rate variability (HRV), Pulse Transit Time (PTT)

### 4. Blood Pressure Estimation
- Heart rate and HRV fed into **pre-trained linear models**
- **Generalized Additive Models (GAMs)** and **polynomial regression** used for SBP and DBP prediction
- **Peak matching algorithm** to enhance accuracy and remove outliers

### 5. Clinical Validation
- Results validated against **BHS (British Hypertension Society)** and **AAMI (American Association for Medical Instrumentation)** protocols

---

## 🛠️ Tech Stack

| Category | Tools |
|----------|-------|
| Language | MATLAB |
| Signal Processing | Butterworth Filter, PCA |
| Machine Learning | GAMs, Polynomial Regression, Linear Models |
| Simulation | MATLAB Live Scripts |
| Validation | BHS & AAMI Clinical Protocols |

---

## 🚀 Getting Started

### Prerequisites
- MATLAB R2023a or later
- Signal Processing Toolbox
- Statistics and Machine Learning Toolbox

### Run the Simulation
1. Clone the repository:
```bash
git clone https://github.com/Bhargava102005/Non-Contact-Blood-Pressure-Analysis.git
```
2. Open MATLAB and navigate to the project folder
3. Run `PPG_Simulation.m`
4. Make sure `bloodPressureLinearModel_DBP.mat` is in the same folder

> **Note:** To use with your own video, update the video file path in `PPG_Simulation.m` at line 2.

---

## 👥 Authors

| Name | Institution |
|------|-------------|
| **Kanamarlapudi Bhargava Mani Rohith** | School of Artificial Intelligence, Amrita Vishwa Vidyapeetham, Coimbatore |
| **Mopuri Abhishiktha** | School of Artificial Intelligence, Amrita Vishwa Vidyapeetham, Coimbatore |
| **Sai Venkata Ganesh Vattikonda** | School of Artificial Intelligence, Amrita Vishwa Vidyapeetham, Coimbatore |
| **Thulasi Jyothi Reddy** | School of Artificial Intelligence, Amrita Vishwa Vidyapeetham, Coimbatore |
| **Akhil V.M** | School of Artificial Intelligence, Amrita Vishwa Vidyapeetham, Coimbatore |

---

## 💡 Key Highlights

- ✅ Completely **non-invasive and non-contact** — no wearable devices needed
- ✅ Uses only a **standard webcam** — cost-effective solution
- ✅ Validated against internationally recognized **clinical standards**
- ✅ Real-time BP monitoring with **automated alerts**
- ✅ Applicable for **remote healthcare and telemedicine**
- ✅ **Published and peer-reviewed** at IEEE ICKECS 2025

---

## 📜 Citation

If you use this work, please cite:

```
K. B. M. Rohith, M. Abhishiktha, S. V. G. Vattikonda, T. J. Reddy and A. V.M,
"Non-Contact Blood Pressure Analysis," 2025 3rd IEEE International Conference on
Knowledge Engineering and Communication Systems (ICKECS), 2025.
DOI: 10.1109/ICKECS65700.2025.11036062
```

---

## 📜 License

This project is for academic and research purposes.
© 2025 IEEE — Published under IEEE copyright.

---

<p align="center">Made with ❤️ for accessible, non-invasive healthcare monitoring 🏥</p>
