# Manual-Testing-of-Farming-Assistant-project
# 🌱 Farming Assistant – IoT-Based AI-Integrated Device for Farmers

**Conference Paper:** *Published in IEEE 6th International Conference on Electrical Engineering and Information & Communication Technology (ICEEICT) 2024*
📄 **IEEE Link:** [https://ieeexplore.ieee.org/document/10534549](https://ieeexplore.ieee.org/document/10534549)
📑 **Manual Testing Documentation:** [View on SharePoint](https://mistedu-my.sharepoint.com/:x:/g/personal/202014018_student_mist_ac_bd/EeuJPuPwVUZIlJdr93ynqtsBf2ar84R8YP-HTWf4TqUmNw?e=1b5LEt)

---

## 📖 Project Overview

Farming Assistant is an **IoT-based AI system for smart agriculture**. This phase focuses on **manual testing** across critical modules – authentication, crop recommendation, fertilizer recommendation, and disease detection – with test cases documented in Excel to validate **functional behavior, UI, and security aspects**.

### 🔧 Tech Stack

* **Frontend:** Flutter (Dart) – Bengali-language Android app for easy farmer adoption
* **Backend:** Firebase Realtime Database – Real-time data sync
* **ML Models:**

  * Crop Recommendation → Gaussian Naive Bayes (GNB)
  * Fertilizer Recommendation → Decision Tree
  * Disease Detection → Convolutional Neural Network (CNN)
* **API Layer:** Flask – For ML model integration
* **Hardware:** Arduino + NPK Sensor – Sends real-time soil data to Firebase

### 📱 App Features

* Farmer-friendly Bengali-language interface
* Real-time crop & fertilizer recommendations
* Disease detection via image classification
* Historical soil data tracking

---

## 🏆 Success Story

This project was **published in IEEE ICEEICT 2024**, under the title:

> *"IoT-Based AI-Integrated Device for Farmers: A Recommendation System for Crop Cultivation"*

This recognition validates the project’s **innovation and real-world impact**, showcasing its potential to contribute toward **smart agriculture**.

---

## 🧪 Manual Testing – Authentication Module

Performed **end-to-end manual testing** for the **Authentication Module** covering:

| **Test Area**          | **Coverage**                                                   |
| ---------------------- | -------------------------------------------------------------- |
| Functional Testing     | Valid & invalid login with email & password                    |
| Regression Testing     | Verified login after adding "Login with Phone Number" feature  |
| UI Testing             | Verified layout, alignment, and responsiveness of login screen |
| Boundary Value Testing | Tested min/max input lengths for email & password              |
| Integration Testing    | Verified login UI → backend API → Firebase/Auth DB flow        |
| Security Testing       | Password masking & SQL injection-like input handling           |

### ✅ Sample Test Cases

| **Test Case ID** | **Scenario**                                  | **Type**       | **Steps**                                   | **Expected Result**                  |
| ---------------- | --------------------------------------------- | -------------- | ------------------------------------------- | ------------------------------------ |
| TC-001           | Valid login with email/password               | Functional     | Enter valid email & password → Tap Login    | Redirect to Dashboard                |
| TC-004           | Verify login after adding phone number button | Regression     | Enter valid credentials → Tap Login         | Existing login still works           |
| TC-005           | Min/Max input length validation               | Boundary Value | Enter min & max email/password combinations | Reject too-short, accept max allowed |
