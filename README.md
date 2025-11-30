STAT 311 Final Project – Modeling U.S. Health Insurance Charges
Authors: Feifei Li 
Course: STAT 311 – Regression Analysis, Fall 2025
Instructor: Dr.Iresha Premarathna
Date: December 2025
Project Overview

This project investigates how demographic and lifestyle factors influence annual U.S. health insurance charges. Using the Kaggle “Insurance Charges” dataset, we evaluate whether the effect of BMI differs between smokers and non-smokers and assess whether a log transformation improves model adequacy.

Three nested regression models were built:

Model 1 – Main Effects

Model 2 – BMI × Smoker Interaction

Model 3 – Log-Transformed Charges + Interaction (Final Model)

Model 3 was selected as the final model because it stabilized variance, improved residual normality, and achieved the best predictive accuracy (CV = 4.77%).

Abstract

Medical insurance charges in the United States are highly skewed and influenced by lifestyle and demographic factors. Using regression analysis, we found that smoking is the strongest predictor of medical costs, and BMI has a dramatically stronger effect for smokers than non-smokers. A natural log transformation of charges was recommended by Box–Cox and led to a valid, interpretable model with excellent predictive accuracy. This project demonstrates how appropriate modeling choices, diagnostics, and transformations can produce an effective and generalizable regression model for real-world cost data.

Contents of This Repository
1. STAT311_Final_Report.pdf

The complete regression analysis report, including:

Data description

Exploratory Data Analysis

Variable screening (stepwise + all possible models)

Model development (Models 1–3)

Diagnostics and validation

Final model selection

Conclusions and implications

2. STAT311_Presentation.pptx

Slides used for the final class presentation.
Covers research questions, methods, EDA visuals, JMP output, model results, conclusions, and limitations.

3. insurance.csv (Dataset)

Original dataset from Kaggle containing:

age, sex, BMI, children, smoker, region, charges

1,338 observations (1,335 used after cleaning)

If the dataset cannot be retrieved directly in GitHub, an alternate download link is provided below.

4. JMP_Files/ Folder

This folder contains:

insurance.jmp – cleaned dataset

analysis_report.jmpjournal – JMP output journal

model_1.jmp, model_2.jmp, model_3.jmp – model fit files

Residual plots, Q–Q plots, Box–Cox output

Influence & leverage diagnostics

These files are needed to reproduce all model fits and diagnostics.

How to Run the JMP Analysis

Download the JMP_Files folder.

Open insurance.jmp in JMP.

Open the .jmpjournal file to view all generated figures.

For model reproduction:

Go to Analyze → Fit Model

Set charges (or ln(charges)) as Y

Add predictors: age, BMI, children, smoker

Add interaction: BMI * smoker

To view VIF:

Fit Model → Red Triangle → Estimates → Show VIF

To run Box–Cox:

Fit Model → Red Triangle → Personality → Box–Cox

All model specifications match exactly what is documented in the final report.

 Dataset Source

Kaggle – Health Insurance Charges Dataset
https://www.kaggle.com/datasets/nalisha/health-insurance-charges-dataset

Dataset originally published by Nalisha; used under acceptable academic usage conditions.

Notes

This project satisfies all STAT 311 Final Project requirements, including written report, EDA, modeling, validation, JMP submission, dataset submission, and GitHub hosting.

For questions or access requests (if private), contact the repository owner.
