#  Crop Recommendation Dashboard (Power BI)

##  Overview

An **inspired decision support system** that recommends the most suitable crop based on **soil health (NPK, pH)** and **environmental conditions (temperature, humidity, rainfall)**.

The dashboard not only predicts the best crop but also explains **why it is suitable and what needs improvement**, making it practical for real-world agricultural decisions.

---
##  Dashboard Preview

<p align="center">
  <img src="Dashboard SS.png" width="900"/>
</p>


##  Key Features

*  **Smart Crop Recommendation** using dynamic user inputs
*  **Yield Score (0–10)** to estimate crop performance
*  **Limiting Factor Detection** (e.g., low nitrogen, excess humidity)
*  **Actionable Insights** (fertilizer and soil correction suggestions)
*  **Interactive Dashboard** with slicers for real-time analysis

---

##  How It Works

The model evaluates crop suitability using a **multi-factor approach**:

* Soil Nutrients (N, P, K)
* Soil pH (crop-specific requirements)
* Temperature, Humidity, Rainfall

 These are combined into a **weighted Yield Score**, and the system selects the **best-performing crop** under given conditions.

---

##  Sample Output

> **Best Crop:** Rice
> **Yield Score:** 8.75
> **Issue:** Low Nitrogen
> **Action:** Add Nitrogen fertilizer

---

## Key Insights

* Crop performance depends on **combined environmental + soil conditions**, not a single factor
* **pH imbalance can limit yield even when nutrients are sufficient**
* **NPK imbalance is a major constraint in crop productivity**
* Weather conditions (especially **rainfall & humidity**) strongly influence crop suitability

---

##  Technical Highlights

* Advanced **DAX modeling** (SWITCH, VAR, TOPN)
* **Crop-specific ideal condition mapping**
* Dynamic **KPI-based recommendation engine**
* Implementation of **limiting factor logic (minimum condition principle)**

---

##  Business Value

* Enables **data-driven crop selection**
* Helps optimize **fertilizer usage and soil health**
* Supports **better yield planning and resource management**

---

##  Tools Used

* Power BI
* DAX
* Data Modeling

---

##  Future Scope

* Integration with **real-time weather APIs**
* Machine Learning-based yield prediction
* Mobile-friendly and farmer-ready interface

---

