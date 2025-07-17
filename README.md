# Predictive Quality Control: Identifying High-Impact Manufacturing Events

## 🚀 Overview

This project builds a predictive model to identify **high-impact manufacturing defects** using historical data from 318 suppliers. These high-impact events result in costly production downtime. Our solution uses a custom machine learning pipeline and innovative feature engineering to provide an early warning system for quality control teams.

---

## 🔍 Problem Statement

Our company logs numerous material defects from suppliers. However, not all defects are equally disruptive. The challenge is distinguishing between routine issues and **critical events** that cause **severe downtime**. We need a **data-driven solution** to:

- Predict which new events will be **high impact**
- Prioritize triage efforts for urgent issues
- Identify risky suppliers and problematic material categories

---

## 📊 Classification Task

We frame this as a binary classification task:

- `1 = High Impact`: Event causes downtime in the top 25% of incidents.
- `0 = Not High Impact`: All other events.

---

## 🧠 Analytical Approach

Key highlights of our modeling pipeline:

- **Custom Feature Engineering: Vendor Priority Ranking**
  - We created a ranked encoding for suppliers:
    - Top 20 most frequent suppliers → Unique ranks (1–20)
    - Remaining 298 suppliers → Assigned a single rank: "Other" (21)

- **Modeling Techniques:**
  - Random Forest Regressor
  - AdaBoost Regressor
  - XGBoost Regressor

- **Evaluation Metrics:**
  - Precision, Recall, F1-score
  - Confusion Matrix
  - ROC-AUC

---

## 💡 Business Value

1. **Proactive Triage**
   - Escalate likely high-impact defects immediately to minimize downtime.

2. **Vendor Risk Management**
   - A separate vendor risk profile provides actionable insights for strategic sourcing and supplier negotiations.

3. **Focused Root Cause Analysis**
   - Feature importances highlight key drivers of severe downtime, aiding continuous process improvement.

---
