# Manual-Testing-of-Farming-Assistant-project
# 🌱 Farming Assistant – IoT-Based AI-Integrated Device for Farmers

Farming Assistant is an **IoT-based AI system for smart agriculture**.  
This phase focuses on **manual testing** across modules like authentication, crop & fertilizer recommendation, and disease detection — all documented in Excel, covering **functional, UI, regression, integration, and security validations**.

---

## 📄 Documentation

- **Conference Paper:** *Published in IEEE 6th International Conference on Electrical Engineering and Information & Communication Technology (ICEEICT) 2024*  
  📑 **IEEE Link:** [https://ieeexplore.ieee.org/document/10534549](https://ieeexplore.ieee.org/document/10534549)

- **Manual Testing File:** [📊 Download Excel from SharePoint](https://mistedu-my.sharepoint.com/:x:/g/personal/202014018_student_mist_ac_bd/Ebe9J-7ViJFOqve8b7uC1-cBa35wHKtmSGJkzRceBOJavA?e=T5fo9s)

---

## 📖 Project Overview

Farming Assistant is an **Integrated Software & Hardware (IDP)** project designed to help farmers make **data-driven agricultural decisions**.

### 🔧 Tech Stack

- **Frontend:** Flutter (Dart) – Bengali-language Android app for easy farmer adoption  
- **Backend:** Firebase Realtime Database – Real-time data sync  
- **ML Models:**  
  - Crop Recommendation → Gaussian Naive Bayes (GNB)  
  - Fertilizer Recommendation → Decision Tree  
  - Disease Detection → Convolutional Neural Network (CNN)  
- **API Layer:** Flask – For ML model integration  
- **Hardware:** Arduino + NPK Sensor – Sends real-time soil data to Firebase  

### 📱 App Features

- Farmer-friendly Bengali-language interface  
- Real-time crop & fertilizer recommendations  
- Disease detection via image classification  
- Historical soil data tracking  

---

## 🏆 Success Story

This project was **published in IEEE ICEEICT 2024**, under the title:  

> *"IoT-Based AI-Integrated Device for Farmers: A Recommendation System for Crop Cultivation"*  

This recognition validates the project’s **innovation and real-world impact**, showcasing its potential to contribute toward **smart agriculture**.

---

## 🧪 Manual Testing Summary

Performed **end-to-end manual testing** for all modules covering:

| **Module**                  | **Test Areas Covered**                                                                 |
|----------------------------|---------------------------------------------------------------------------------------|
| Authentication             | Functional (valid/invalid login), Regression (login with phone), UI, Boundary Value, Integration (UI → API → Firebase), Security (password masking, SQL injection) |
| Crop & Fertilizer Recommendation | Unit testing (ML model predictions), Integration (Hardware → Firebase → App, App → API → ML), System testing (end-to-end flow), Performance (under 2s), GUI, Usability |
| Disease Detection          | Functional (clear/blurry/healthy images), Negative (non-crop input), UI, Integration (Flask API), Security (malicious file handling), Performance, Model accuracy |

---

### ✅ Sample Authentication Test Cases

| **Test Case ID** | **Scenario**                                  | **Type**       | **Steps**                                   | **Expected Result**                  |
|------------------|-----------------------------------------------|---------------|---------------------------------------------|-------------------------------------|
| TC-LOGIN-001     | Valid login with email/password               | Functional    | Enter valid email & password → Tap Login    | Redirect to Dashboard               |
| TC-LOGIN-004     | Verify login after adding phone number button | Regression    | Enter valid credentials → Tap Login         | Existing login still works          |
| TC-LOGIN-009     | Min/Max input length validation               | Boundary Value| Enter min & max email/password combinations | Reject too-short, accept max allowed |
| TC-LOGIN-010     | Verify login UI → Firebase → Auth DB          | Integration   | Enter valid credentials → Tap Login         | API returns success → Navigate Dashboard |
| TC-LOGIN-012     | SQL injection-like input handling             | Security      | Enter `admin' OR '1'='1` as email → Submit | Show "Invalid Credentials" safely   |


