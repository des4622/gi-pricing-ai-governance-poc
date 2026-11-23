# GI Pricing Analytics & AI Governance Proof-of-Concept

## 🎯 Project Objective
To establish a transparent baseline pricing model for a General Insurance portfolio, identify profitability leakage in underperforming segments, and design a robust AI governance framework to guide the future integration of Machine Learning into the pricing engine.

*This project was developed as a technical proof-of-concept to demonstrate capabilities in actuarial data science, portfolio analytics, and AI model governance.*

## 🛠️ Methodology
1. **Baseline Modeling:** Developed a Poisson Generalized Linear Model (GLM) using a log-link function and exposure offset to accurately model claim frequency and calculate risk relativities.
2. **Portfolio Validation:** Conducted segment-level Actual vs. Expected (A/E) analysis and built a 2D Risk Heatmap to isolate concentration risks and rating inadequacies.
3. **Strategic Governance:** Formulated a 4-pillar AI Governance Framework to ensure regulatory compliance and ethical deployment of future ML challenger models.

## 📊 Key Findings & Insights

### 1. Portfolio Validation (Actual vs. Expected)
The baseline GLM is well-calibrated for the majority of the book (ages 26+). However, the linear assumption fails to capture the non-linear risk spike in the youngest demographic.
<img width="3000" height="1800" alt="day1_actual_vs_expected" src="https://github.com/user-attachments/assets/40f54c9d-b1d9-4bf4-907b-0e6a6d7da725" />


### 2. Underperforming Segment Identification
Deep-dive analysis revealed a critical leakage in the **18-25 'Med Risk' segment**, which is underperforming expectations by **63.7% (Lift = 1.63)**. 
<img width="3000" height="1800" alt="day2_portfolio_heatmap" src="https://github.com/user-attachments/assets/4ab65a3e-bc5c-4ec7-b551-a7054395671f" />

*Recommendation: Implement a +63.7% surcharge on base premium for this segment, or mandate telematics (UBI) for young drivers to improve risk selection.*

## 🛡️ AI Governance Framework
To support the transition from traditional GLMs to Machine Learning (e.g., XGBoost), I designed a 4-pillar governance framework to satisfy regulatory requirements (e.g., IA Hong Kong):
1. **Explainability:** SHAP values for all ML predictions.
2. **Baseline Reconciliation:** ML outputs bounded within ±15% of GLM baseline.
3. **Human-in-the-Loop:** Rate changes >5% require Actuarial sign-off.
4. **Drift Monitoring:** Automated alerts for >2% Actual vs. Expected deviation.
<img width="862" height="490" alt="day3_ai_governance_checklist" src="https://github.com/user-attachments/assets/79215258-14f5-4118-b454-7ee329911a05" />


## 📂 Repository Contents
- `day1_glm_pricing.py`: Python script for data ingestion, Poisson GLM fitting, and coefficient interpretation.
- `day2_portfolio_analysis.py`: Script for heatmap generation and Lift analysis.
- `steerco_briefing.html`: Interactive 3-slide SteerCo presentation summarizing the findings and strategic proposals.

---
**Prepared by:** Desmond Lai 
