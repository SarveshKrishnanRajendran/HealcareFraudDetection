# Healthcare Provider Fraud Detection

## Project Overview

This project focuses on detecting fraudulent activities committed by healthcare providers using machine learning techniques. Healthcare fraud, particularly by providers, poses a significant financial burden on healthcare systems, leading to increased insurance premiums and higher overall costs for patients. This project aims to identify potentially fraudulent providers by analyzing patterns in the claims they file.

## Table of Contents

1. [Project Goal](#project-goal)
2. [Introduction to the Dataset](#introduction-to-the-dataset)
3. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
4. [Feature Selection Methods](#feature-selection-methods)
5. [Implementing Supervised Models](#implementing-supervised-models)
6. [Hyperparameter Tuning](#hyperparameter-tuning)
7. [Conclusion](#conclusion)
8. [Requirements](#requirements)
9. [How to Run](#how-to-run)

## Project Goal

The primary goal of this project is to predict potentially fraudulent healthcare providers based on the claims data they submit. The project also seeks to identify key variables that are indicative of fraudulent behavior.

## Introduction to the Dataset

The project utilizes four main datasets:

1. **Inpatient Data**: Contains claims data for patients admitted to hospitals, including admission and discharge dates and diagnosis codes.
2. **Outpatient Data**: Includes claims data for patients who visited hospitals but were not admitted.
3. **Beneficiary Details Data**: Contains key KYC details of the beneficiaries, including health conditions and region.
4. **Provider Data**: Provides true labels indicating whether a provider is fraudulent or not.

Combined, these datasets form a comprehensive data frame with 558,211 rows and 55 columns.

## Exploratory Data Analysis (EDA)

The EDA process involved:

- Merging the different datasets into a single data frame.
- Inspecting the data to understand its structure, including non-null values and data types.
- Performing basic data wrangling tasks, such as encoding categorical variables and handling missing values.
- Visualizing the data using pair plots to identify patterns and relationships.

## Feature Selection Methods

Various methods were used to select the most relevant features for the model:

1. **Correlation Analysis**: Although no significant correlations were found initially, further analysis led to the selection of important features.
2. **Decision Tree Feature Importance**: Identified key features using a decision tree classifier.
3. **Random Forest Feature Importance**: Further validation was done using a random forest classifier, which provided more reliable importance values. The top 7 features were selected for modeling.

## Implementing Supervised Models

Multiple supervised learning models were implemented and evaluated for their accuracy:

- Logistic Regression: 63.00%
- K-Nearest Neighbors: 70.38%
- Linear Discriminant Analysis: 63.00%
- Quadratic Discriminant Analysis: 62.93%
- Naive Bayes: 62.59%
- Decision Tree: 69.82%
- Random Forest: 73.61% (Best performing model)
- Support Vector Machine: 63.03%

## Hyperparameter Tuning

Hyperparameter tuning was performed on the Random Forest classifier to optimize its performance further. However, due to some computational limitations, the final results of the tuning process were not fully obtained.

## Conclusion

The project successfully identified the best-performing model for predicting potentially fraudulent healthcare providers. The most important features were also determined, which include variables related to claim amounts, reimbursement, and deductible amounts.

## Requirements

- Python 3.x
- Jupyter Notebook
- Required Python libraries:
  - pandas
  - numpy
  - scikit-learn 
  - matplotlib
  - seaborn

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/SarveshKrishnanRajendran/HealcareFraudDetection.git
2. Install the Required Library:
   ```bash
   pip install -r requirements.txt
3. Open and run the Jupyter notebook:
   ```bash
   jupyter notebook healthcare_proj_final.ipynb
