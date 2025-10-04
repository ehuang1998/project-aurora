Here’s your **complete, professional-grade README.md** — now including the **12-week implementation plan** with detailed milestones and features aligned to each sprint.
You can paste this directly into your GitHub repo. It’s written in Markdown for perfect GitHub rendering and readability.

---

# 🌿 AllerCheck

*A mobile app for detecting allergens and harmful ingredients in everyday products using the OpenFDA API.*

---

## 📖 Overview

**AllerCheck** helps users with **allergies and sensitivities** make safer product choices.
By scanning or searching for a product, the app identifies **potential allergens, irritants, and FDA recalls**, providing users instant, trustworthy health insights.

---

## 🎯 Motivation

Millions of consumers struggle to understand product ingredients or verify safety data. Manually checking labels or researching allergens is tedious and confusing.
**AllerCheck** bridges this gap by combining:

* The **OpenFDA API** for official product safety and recall data, and
* A **personal allergen profile** that flags risky ingredients.

This ensures every scan or search leads to safer, more informed choices.

---

## ⚙️ Core Features

### 🧭 Product Search

* Search for a product or ingredient using the OpenFDA API.
* Display product recalls, side effects, or safety notices.

### 🧾 Ingredient Analysis

* Paste or scan an ingredient list.
* Detect allergens or irritants from a predefined allergen dictionary.
* Highlight potential allergens with color-coded severity indicators.

### 🔔 Notifications

* Receive **push notifications** for:

  * FDA recalls on saved products.
  * Allergen matches based on user preferences.
* Uses **Expo Notifications API** for cross-platform alerts.

### 🧍 Personalized Allergen Profile

* Create a profile by selecting allergens (nuts, gluten, sulfites, parabens, fragrance, etc.).
* Profile is stored locally and used for every scan or search.

### 🕓 Product History

* View recently scanned or analyzed products.
* Mark items as “Safe” or “Avoid”.
* Stored locally using AsyncStorage.

### 📸 Label Scanning (Advanced)

* Upload or capture a photo of a product label.
* On-device OCR extracts ingredients and runs allergen matching.
* Counts as a **Device API Integration** for advanced course marks.

---

## 🧠 Technical Architecture

| Component            | Technology                          | Description                               |
| -------------------- | ----------------------------------- | ----------------------------------------- |
| **Frontend**         | React Native (Expo)                 | Cross-platform mobile app                 |
| **API Integration**  | OpenFDA REST API                    | Retrieves health & recall data            |
| **State Management** | React Context / Redux Toolkit       | User profile, allergens, history          |
| **Storage**          | AsyncStorage                        | Local data persistence                    |
| **Notifications**    | Expo Notifications                  | Push alerts for recalls and allergen hits |
| **OCR (Advanced)**   | ML Kit (Android) / Vision API (iOS) | Extracts text from product labels         |
| **Version Control**  | GitHub                              | Main/dev branches, PR workflow            |
| **CI/CD**            | GitHub Actions                      | Type checks, linting, build validation    |


