

# 🌿 AllerCheck

*A mobile app for detecting allergens and harmful ingredients in everyday products using the OpenFDA API.*

---

## 📖 Overview

**AllerCheck** helps users with **allergies and sensitivities** make safer product choices.
By scanning or searching for a product, the app identifies **potential allergens, irritants, and FDA recalls**, providing users instant, trustworthy health insights.

---

## 1️⃣ Motivation

### Problem & Need

Millions of consumers with **food allergies, chemical sensitivities, or skin conditions** struggle to identify safe products. Ingredient lists are often complex, inconsistent, and printed in small fonts that make it hard to verify safety information. Additionally, **official recall or warning data** from agencies like the FDA are rarely checked by everyday users.

Manually researching ingredients and recalls across multiple sources is **tedious, error-prone, and time-consuming**.
**AllerCheck** bridges this gap by combining:

* The **OpenFDA API** for official product safety and recall data, and
* A **personal allergen profile** that flags risky ingredients.

This ensures every scan or search leads to safer, more informed choices.

---

### Why It’s Worth Pursuing

AllerCheck empowers users to make safer, more informed choices about what they buy and use. By combining **personal allergen profiles**, **official FDA data**, and **smart scanning**, the app becomes a practical companion for people with health sensitivities or dietary restrictions.

---

### Target Users

* Individuals with **food allergies** (e.g., nuts, dairy, gluten)
* People with **skin sensitivities or asthma**, avoiding irritants such as parabens or fragrances
* **Parents or caregivers** shopping for children with allergies
* **Health-conscious consumers** seeking recall or ingredient transparency

---

## 2️⃣ Objective and Key Features

### Project Objective

To develop a **cross-platform mobile app** using **React Native and Expo** that allows users to:
1. Search or scan products for allergen and safety information.
2. Maintain a **personal allergen profile** stored locally.
3. Receive **notifications** for product recalls or allergen alerts.
4. Use **OCR scanning** to extract and analyze product labels.

---

### Core Features

#### Product Search
* Search for products or ingredients using the **OpenFDA REST API**.
* Display product recalls, warnings, and safety notices.

#### Ingredient Analysis
* Paste or scan an ingredient list.
* Detect allergens or irritants from a predefined allergen dictionary.
* Highlight risky ingredients and potential allergens with color-coded severity indicators.

#### Notifications
* Receive **push notifications** for:
  * FDA recalls on saved products.
  * Matches between new product data and user allergens.
* Uses **Expo Notifications API** for cross-platform alerts.

#### Personalized Allergen Profile
* Create and edit a local profile selecting allergens such as nuts, gluten, sulfites, parabens and fragrances.  
* Profile is stored with **AsyncStorage**, ensuring privacy and offline availability.

#### Product History
* View recently scanned or analyzed products.
* Mark items as “Safe” or “Avoid”.
* Stored locally for persistence across sessions.

#### Label Scanning *(Advanced Feature #1)*
* Upload or capture a photo of a product label.  
* **OCR** extracts text and detects allergens automatically.

#### Real-time Recall Alerts *(Advanced Feature #2)*
* Background polling of the OpenFDA recall database.  
* Notify users when a saved product appears in a recall notice.

---

### Navigation Structure

The app will use **Expo Router** for intuitive, type-safe navigation:

| Route | Screen Purpose |
|-------|----------------|
| #TODO | Home screen - search bar and product scan button |
| #TODO | Allergen profile setup and editing |
| #TODO | History of scanned or analyzed items |
| #TODO | Product details, recall info, and allergen matches |
| #TODO | #TODO |

---

### State Management and Persistence

* **React Context API** (or Redux Toolkit if scaling needed) for global state: allergen profile, recall data, and recent history.  
* **AsyncStorage** for persistent local storage between sessions.

This ensures data consistency across the app without external backend dependencies.

---

### Backend Integration

* Uses **OpenFDA REST API**, accessing endpoints for food, drug, and cosmetic safety.  
* Fetches official recall and ingredient information with filtering and caching.  
* Implemented via `fetch()` with proper error handling and TypeScript typing for API responses.

---

### Notification Setup

* Implemented using **Expo Notifications**.  
* Local notifications will alert users when:
  * A saved product has been recalled.
  * An ingredient in a newly scanned product matches their allergen profile.
* Optional remote notification setup (if time allows) through Expo’s push notification service.

---

### Deployment Plan

* Final builds generated via **Expo EAS Build** for both Android (.apk/.aab) and iOS (.ipa).  
* Test builds will be distributed to team members for internal testing before the final presentation.  
* Deployment scripts will include automated linting and type checking via **GitHub Actions** CI workflow.

---

### Technical Architecture

| Component / Requirement | Technology | Description |
|--------------------------|-------------|--------------|
| **Frontend** | React Native (Expo) | Cross-platform mobile app implementing course frameworks |
| **Navigation** | Expo Router | File-based navigation and layout structure with TypeScript typing |
| **State Management** | React Context / Redux Toolkit | Handles user profile, allergens, and scan history globally |
| **Local Persistence** | AsyncStorage | Stores allergen preferences and product history locally |
| **Notifications** | Expo Notifications API | Push alerts for recalls and allergen matches |
| **Backend Integration** | OpenFDA REST API | Retrieves verified FDA data on recalls and ingredients |
| **Advanced Features** | ML Kit (Android) / Vision API (iOS) | OCR-based label scanning for ingredient extraction |
| **Deployment** | Expo EAS Build | Cloud builds for Android and iOS test deployment |
| **Version Control** | GitHub | Main/dev branches, pull request workflow |
| **CI/CD** | GitHub Actions | Automated type checks, linting, and build validation |


---

### Scope and Feasibility

* **Feasible scope**: Core app (search, profile, analysis, local storage) achievable within 3-4 weeks.  
* **Stretch goals** (OCR, notifications) are realistic for remaining weeks and add innovation.  
* Uses public data and standard Expo APIs, avoiding backend setup overhead.  
* Each component can be independently developed and integrated incrementally.  

---

### Privacy & Ethics

* All allergen data and product history are stored **locally only**.  
* No user medical or identifying data are transmitted externally.  
* App provides **informational support only**, not medical advice.  

---

## 3️⃣ Tentative Plan

### Team Members and Responsibilities

| Member | Responsibilities |
|--------|------------------|
| **Eric Huang** | #TODO |
| **Devanshu Singhvi** | #TODO |
| **Hamza Choudhary** | #TODO |
| **Kinkini Monaragala** | #TODO |

---

### Development Approach

1. **Setup & UI**  
  Initialize Expo project, navigation routes, and core UI screens (Home, Profile, History).  

2. **Backend & Data Integration**  
  Connect to OpenFDA API and render real data with basic allergen detection.  

3. **Profile & Persistence**  
  Add allergen profile setup, local storage, and recall tracking functionality.  

4. **Advanced Features**  
  Integrate OCR and notifications; finalize data flow and user testing.  

5. **Polish & Deployment**  
  Conduct final testing, bug fixes, and prepare EAS builds for presentation.  

This staged plan ensures steady progress and clear task ownership across the team, making project completion  realistic.

---

## Future Enhancements

- Barcode scanning for automatic product lookup.  
- Integration with **USDA FoodData Central** for nutritional information.  
- Cloud backup of allergen profiles for multi-device syncing.  
- Community-shared allergen safety reports or feedback features.

---
