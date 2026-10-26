# Fitness Data Classification: Model Comparison

## Overview

This project explores physical fitness data and compares two machine learning classification models: Logistic Regression and Random Forest. It covers data cleaning, exploratory data analysis (EDA), preprocessing, model training, and evaluation.

The objective is to compare model performance and identify which algorithm performs better on the dataset's original classification target.

## Dataset

This project uses the [Body Performance Data dataset from Kaggle](https://www.kaggle.com/datasets/kukuroo3/body-performance-data).

The dataset includes physical measurements and fitness indicators such as:

- Age and gender
- Height and weight
- Body fat percentage
- Systolic and diastolic blood pressure
- Grip strength
- Flexibility
- Sit-up counts
- Broad-jump distance

**Target variable:** `class` — the dataset's original A/B/C/D labels.

The project currently predicts the original `class` variable, not BMI-based categories such as Underweight, Normal, Overweight, or Obese.

The dataset file is not included in this repository. Download it from the original Kaggle source before running the notebook.

## Project Workflow

1. Data loading and inspection
2. Data cleaning and duplicate checking
3. Exploratory data analysis and visualization
4. Categorical encoding and feature scaling, where appropriate
5. Train-test splitting
6. Model training using Logistic Regression and Random Forest
7. Model evaluation using accuracy, precision, recall, F1 score, and confusion matrices
8. Feature importance analysis using Random Forest

## Machine Learning Models

### Logistic Regression
Used as a baseline classification model.

### Random Forest Classifier
An ensemble learning algorithm used to classify observations based on multiple decision trees.

Both models are evaluated on the test dataset to compare their classification performance.

## Evaluation Metrics

The models are evaluated using:

- Accuracy
- Macro-averaged Precision
- Macro-averaged Recall
- Macro-averaged F1 Score
- Confusion Matrix

Random Forest feature importance is also examined to understand which features contribute most to the model's predictions. These importance scores do not establish causation.

## Repository Structure

```text
fitness-data-classification/
├── fitness_data_classification_model_comparison.ipynb
├── README.md
└── requirements.txt
```

## Installation and Usage

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd fitness-data-classification
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Download the dataset

Download the CSV file from the Kaggle dataset linked above and place it at the file path specified in the notebook. Update the path if necessary.

### 4. Run the notebook

Open `fitness_data_classification_model_comparison.ipynb` in Jupyter Notebook or VS Code and run the cells sequentially.

## Limitations

- The model predicts the dataset's original A/B/C/D labels; it does not predict BMI categories or diagnose health conditions.
- Results depend on the dataset, preprocessing choices, and train-test split.
- Feature importance indicates predictive contribution within the fitted model, not a causal relationship.

## Future Improvements

- Apply cross-validation for more robust evaluation.
- Perform hyperparameter tuning.
- Investigate class imbalance and per-class performance.
- Compare additional classification algorithms.
- Explore BMI-category classification as a separate extension, with appropriate feature selection to avoid target leakage.

## Acknowledgements

Dataset: [Body Performance Data — Kaggle](https://www.kaggle.com/datasets/kukuroo3/body-performance-data)
