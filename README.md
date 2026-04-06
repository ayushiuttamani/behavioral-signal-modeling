# Behavioral Signal Modeling in Remote Work Systems

## Overview
This project analyzes behavioral and environmental factors influencing employee burnout, well-being, and productivity using a structured dataset of post-pandemic work patterns. The objective is to identify predictive signals, quantify their impact, and build models that explain variations in burnout risk and employee outcomes.

The analysis is framed as a **signal discovery and predictive modeling problem**, where latent behavioral variables (burnout, isolation, work-life balance) are derived and used to model outcomes across different work environments.

---

## Dataset

**Source:**  
https://www.kaggle.com/datasets/waqi786/remote-work-and-mental-health

The dataset contains ~3,000+ employee records with a mix of:
- **Numerical variables:** Age, Hours_Per_Week  
- **Categorical variables:** Gender, Region, Job Role, Work Arrangement  
- **Ordinal variables:** Burnout Level, Work-Life Balance, Social Isolation  

These variables capture behavioral, environmental, and demographic factors affecting employee well-being in remote, hybrid, and onsite settings.

---

## Problem Formulation

The project addresses multiple modeling and inference problems:

1. **Signal Identification:**  
   Which factors most strongly predict burnout levels?

2. **Classification / Risk Modeling:**  
   Which variables predict whether an employee is at risk of burnout?

3. **Behavioral Dynamics:**  
   How does work arrangement influence social isolation and work-life balance?

4. **Non-linear Effects:**  
   How does workload interact with burnout to affect job satisfaction?

5. **Outcome Modeling:**  
   What factors predict whether employees "thrive"?

---

## Methodology

### Data Preparation
- Type conversion and cleaning of numerical, categorical, and ordinal features  
- Feature engineering:
  - Burnout score (ordinal mapping)
  - Mental health indicator flags
  - Physical issue metrics
  - Composite "Thriving" variable  
- Encoding:
  - One-hot encoding (nominal variables)
  - Ordinal encoding (ranked variables)
- Standard scaling of numerical features  
- Train-test split (80/20)

---

### Signal Extraction & Feature Selection
- **LASSO Regression (L1 regularization):** sparse signal selection  
- **Mutual Information:** non-linear dependency detection  
- **Random Forest Feature Importance:** ensemble-based ranking  

---

### Statistical Analysis
- **Wilcoxon Rank-Sum Tests:** non-parametric comparison of numeric predictors  
- **Chi-Square Tests:** association between categorical variables and burnout risk  
- **Spearman Correlation:** ordinal relationships  

---

### Predictive Modeling
- **Ordinal Logistic Regression:** modeling ordered burnout levels  
- **Classification Models:** burnout risk prediction  
- **Regression Models:** workload vs satisfaction dynamics  
- **Interaction Models:** burnout-dependent effects of workload  

---

## Key Findings

- **Work arrangement is the strongest predictor of burnout.**
  - Remote employees show significantly higher burnout risk  
  - Onsite work shows a protective effect  

- **Behavioral and environmental signals dominate over raw workload metrics.**
  - Social isolation shows a meaningful relationship with burnout  
  - Many numeric workload variables are not statistically significant  

- **Burnout alters how workload is experienced.**
  - Low-burnout individuals tolerate longer hours  
  - High-burnout individuals show declining satisfaction with increased hours  

- **Predictive modeling shows strong separability of outcomes**
  - Behavioral features provide significantly higher predictive power than demographic variables  

---

## Repository Structure
