# Stroke Risk Prediction

A machine learning project for predicting stroke risk using exploratory feature analysis, risk engineering, and predictive modeling.

## Project Overview

This project analyzes patient health data to identify stroke risk factors and build predictive models. It focuses on:
- **Exploratory Feature Analysis**: Understanding the relationship between health metrics and stroke risk
- **Risk Engineering**: Creating new features like Age-Normalized Risk Index (ANRI) and Chronic Condition Score (CCS)
- **Predictive Modeling**: Building and evaluating models to predict stroke risk

## Key Features

### 1. Age-Normalized Risk Index (ANRI)
Identifies patients whose stroke risk is unusually high for their age. Calculated as:
```
ANRI = stroke_risk_pct / age
```

### 2. Chronic Condition Score (CCS)
Represents the number of chronic cardiovascular conditions a patient has:
```
CCS = high_bp + irregular_heartbeat
```

## Dataset

The project uses the following data files:
- `strokeX.csv` - Main training dataset
- `strokeX_test.csv` - Test dataset for evaluation
- `kaggle_submission.csv` - Submission file with predictions

## Dependencies

Core libraries used:
- **pandas**, **numpy** - Data manipulation and analysis
- **scikit-learn** - Machine learning models
- **matplotlib**, **seaborn**, **plotly** - Data visualization
- **imbalanced-learn** - Handling imbalanced datasets
- **pytest** - Testing

## Project Structure

```
├── notebook.ipynb           # Main analysis and modeling notebook
├── strokeX.csv              # Training dataset
├── strokeX_test.csv         # Test dataset
├── kaggle_submission.csv    # Model predictions for submission
├── requirements.txt         # Python dependencies
└── README.md                # This file
```

## Usage

Open and run the Jupyter notebook to:
1. Load and explore the stroke risk dataset
2. Compute risk engineering features (ANRI, CCS)
3. Perform exploratory data analysis
4. Train and evaluate predictive models
5. Generate predictions for submission

## Key Insights
Patients with the highest ANRI values show high stroke risk at lower ages, indicating acute vulnerability to stroke despite their age. The analysis reveals that symptoms like shortness of breath, chest discomfort, and dizziness are common among high-risk patients.

## Results

Accuracy: 98%
ROC-AUC: 99%
F1 score: 98%
Best model: Ensemble model with base model as LogisticRegression
