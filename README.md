# Postpartum Depression Analysis

This project focuses on understanding and predicting **Postpartum Depression (PPD)** using real-world survey data. I have analyzed psychological, behavioral, and demographic factors and built machine learning models to identify significant indicators and predict PPD based on the presence of **anxiety**.

## Project Overview

### Research Questions

1. Do factors like **age**, **trouble sleeping at night**, and **overeating or loss of appetite** significantly influence Postpartum Depression?
2. Is **anxiety** a good predictor of Postpartum Depression?

### Hypotheses

- **Null Hypothesis**: Factors such as age, sleeping troubles, and appetite changes do not impact PPD.
- **Alternate Hypothesis**: These factors do significantly influence PPD.

## Dataset

- **Source**: [Kaggle - Postpartum Depression Dataset](https://www.kaggle.com/datasets/parvezalmuqtadir2348/postpartum-depression)
- **Format**: CSV
- **Size**: 1,503 rows × 11 columns
- **Target Variable**: `Feeling Anxious` (used as proxy for PPD)
- **All features are categorical**, covering aspects like mood, sleep, appetite, irritability, guilt, bonding with baby, and suicide attempts.

## Methodology

### Tools & Technologies

- Python
- MySQL
- pandas, matplotlib, seaborn
- Scikit-learn (SVM, Logistic Regression, KNN, Random Forest, Gradient Boosting)

### Key Steps

1. **Data Cleaning & Preprocessing**
   - Loaded into MySQL, handled null values using `bfill`.
   - Encoded categorical variables using Label Encoding.

2. **Exploratory Data Analysis (EDA)**
   - Univariate & bivariate analysis with frequency counts and visualizations (histograms, count plots).
   - Visualized patterns between features and anxiety.

3. **Correlation Analysis**
   - Heatmap identified key predictors: guilt, concentration issues, bonding problems.

4. **Model Building & Evaluation**
   - Trained 5 classifiers: **SVM, Logistic Regression, KNN, Random Forest, Gradient Boosting**
   - Used metrics like **accuracy, precision, recall, F1-score, AUC**
   - **SVM achieved best performance** with 96% accuracy and high precision.

5. **Feature Importance**
   - Identified `feeling of guilt`, `trouble concentrating`, and `bonding with baby` as most influential.

## Key Findings

- **Significant Predictors**: Age, sleep trouble, and appetite changes **do influence** PPD.
- **Anxiety is a strong predictor** of PPD, validated by high model performance.
- **SVM** was selected as the best model with **96% accuracy and precision**.
- `Feeling of guilt` was the most important feature influencing anxiety.

## Limitations

- Dataset is hospital-based and limited to a specific time and region.
- Data collected over just **two days**, limiting temporal insights.
- Potential bias due to the **COVID-19 pandemic** environment.
- Small sample size, and basic modeling due to learning constraints.

---

