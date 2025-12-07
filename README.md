# 📊 Hypertension Risk Prediction Using NHANES 2017–2018

A biostatistics project using logistic regression modeling, exploratory analysis, and NHANES survey data.

This repository contains a structured analysis pipeline built using NHANES 2017–2018 data to explore factors associated with hypertension in U.S. adults.
Using demographic, anthropometric, and dietary data, three logistic regression models (A, B, and C) are developed and evaluated.

Note: NHANES is a complex survey dataset; this project illustrates statistical modeling concepts using merged XPT files but does not incorporate survey weights.

## 🔍 Project Overview

The workflow includes:

1. Data Integration

Importing multiple NHANES XPT files (demographics, blood pressure, body measurements, dietary intake)

Merging datasets on participant ID (SEQN)

Cleaning and selecting relevant variables

Constructing a binary hypertension indicator:

SBP ≥ 130 or DBP ≥ 80

2. Exploratory Data Analysis

Using seaborn + matplotlib to explore distributions and subgroup patterns:

Age distribution by hypertension status

BMI distribution & boxplots

Hypertension differences across:

gender

race/ethnicity

Visual checks for variable behavior prior to modeling

These plots help assess trends, potential confounders, and effect directions.

3. Logistic Regression Models

Three models are built using statsmodels.Logit for full statistical transparency:

🟦 Model A — Age + BMI

Basic biophysical model:

RIDAGEYR (age)

BMXBMI (BMI)

Outputs:

regression coefficients

odds ratios (via exponentiated coefficients)

accuracy & ROC-AUC

🟩 Model B — Age + BMI + Gender + Race

Adds categorical demographic variables with one-hot encoding:

improves model complexity and interpretability

helps capture health disparities across subgroups

Outputs identical metrics with updated predictors.

🟧 Model C — Age + BMI + Gender + Race + Dietary Calories

Introduces dietary intake (DR1TKCAL) to evaluate whether energy consumption improves prediction.

This represents a realistic biostatistics workflow: incrementally adding covariates to compare model fit and predictive performance.

## 📈 Evaluation Metrics

For each model, the script computes:

🔹 Accuracy

🔹 ROC-AUC

🔹 Odds ratios (exp(coefficients))

These provide both interpretability and predictive insight.

## Repository Structure
Biostatistics/
│── hypertension-prediction-nhanes.py   # Full analysis pipeline
└── README.md

## Skills Demonstrated

🔹 Biostatistics & Epidemiology

🔹 Binary outcome modeling (logistic regression)

🔹 Interpreting odds ratios

🔹 Working with population health datasets

🔹 Identifying meaningful covariates

🔹 Data Engineering

🔹 Reading NHANES XPT files

🔹 Merging multi-table datasets

🔹 Handling categorical recoding

🔹 Cleaning and validating inputs

🔹 Exploratory Analysis

🔹 Distribution analysis

🔹 Group comparisons

🔹 Visual storytelling with seaborn/matplotlib

🔹 Modeling & Evaluation

🔹 Building staged predictive models

🔹 Assessing feature importance

🔹 Evaluating ROC-AUC and accuracy

🔹 Understanding effect of covariates on hypertension risk

### Tools Used

🔹 Python

pandas, numpy

🔹 statsmodels

seaborn, matplotlib

sklearn (metrics only)

## 🎯 Purpose of This Project

This project was created to:

🔹 strengthen applied biostatistics skills

🔹 understand how demographic, anthropometric, and dietary factors relate to hypertension

🔹 practice structured modeling pipelines

🔹 develop reproducible, transparent analysis workflows

It is a learning-focused exploration rather than a clinical decision tool.

### 🤝 Author

Khushi Tyagi
Bioinformatics | Biostatistics | Computational Genomics
