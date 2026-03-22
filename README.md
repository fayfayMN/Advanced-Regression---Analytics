# 🏥 Predictive Modeling: U.S. Health Insurance Cost Analysis
**STAT 311 | Advanced Regression & Analytics | Fall 2025**

## 📌 Executive Summary
Medical insurance charges in the U.S. are notoriously skewed and influenced by complex lifestyle interactions. This project bridges the gap between raw demographic data and accurate cost forecasting by developing a **Log-Transformed Interaction Model**. By stabilizing variance and addressing non-normality, I achieved a highly accurate predictive model with a **CV of 4.77%**.

## 🧠 The "Gap" Analysis: Why simple models failed
Standard linear models often fail on healthcare data because costs are not distributed normally. My analysis identified two critical "blind spots" in basic modeling:
1. **The Variance Gap:** Insurance charges are highly skewed; a Box-Cox transformation was required to normalize residuals.
2. **The BMI-Smoker Interaction:** I discovered that BMI does not affect everyone equally—it has a dramatically higher impact on costs for smokers than for non-smokers.

## 🛠️ Technical Methodology
I utilized **JMP Statistical Software** to build and validate three nested models:

* **Model 1 (Baseline):** Main effects only (Age, BMI, Smoking status).
* **Model 2 (Interaction):** Added $BMI \times Smoker$ interaction terms to capture non-linear cost spikes.
* **Model 3 (Selected Final):** Applied a **Natural Log Transformation** ($ln(charges)$) to address heteroscedasticity and stabilize variance.

### Model Performance Metrics
| Metric | Model 1 | Model 3 (Final) |
| :--- | :--- | :--- |
| **Model Type** | Linear Main Effects | Log-Transformed Interaction |
| **Predictive Accuracy** | Baseline | **CV = 4.77%** |
| **Variance Stability** | Poor (Heteroscedastic) | **Stable (Homoscedastic)** |
| **Key Insight** | Smoking is a predictor | **Smoking + BMI interaction drives 80%+ of cost** |

## 🗂️ Repository Structure
* **[STAT311_Final_Report.pdf](Link)**: Comprehensive 20+ page analysis including variable screening (Stepwise), diagnostics, and influence/leverage plots.
* **[JMP_Files/](Link)**: Complete reproducible environment including `.jmpjournal` files and model fit scripts.
* **[insurance.csv](Link)**: Cleaned dataset (1,335 observations).

## 🚀 How to Reproduce
1. Open `insurance.jmp` in JMP.
2. Run the saved scripts for **Model 3**.
3. **Model Specifications:** $Y = ln(charges)$; $X = Age, BMI, Children, Smoker, (BMI \times Smoker)$.
4. Diagnostics used: VIF for multicollinearity, Box-Cox for transformation, and Cook's D for influence.

---
**Course:** STAT 311 – Regression Analysis  
**Instructor:** Dr. Iresha Premarathna  
**Author:** Feifei Li (GPA: 3.9)
