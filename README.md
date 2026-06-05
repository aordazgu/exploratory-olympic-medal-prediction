# DATA 301 Final Project: Predicting Olympic Medal Winners

**Team:** Arturo Ordaz-Gutiérrez, Lucas Summers, Jesus Avalos

## Overview

This project uses machine learning to predict whether an Olympic athlete will win a medal based on various features. We use the [120 Years of Olympic History](https://www.kaggle.com/datasets/heesoo37/120-years-of-olympic-history-athletes-and-results) dataset from Kaggle, which contains athlete event data from 1896 to 2016.

## Research Questions

1. **Primary:** Can we predict whether an athlete will medal using athlete characteristics and contextual factors? How do sport-specific models compare to a global model?
2. **Secondary:** Which feature set is more predictive of medal outcomes, athlete characteristics (Age, Height, Weight, Sex) or external factors (Country, Season, Sport, Year)?

## Methods

- **Models:** Logistic Regression and Decision Tree classifiers, tuned via GridSearchCV with 5-fold stratified cross-validation
- **Evaluation metric:** F1 score (to handle class imbalance between medalists and non-medalists)
- **Feature engineering:** Athletics events were categorized into sub-disciplines (Sprints, Distance, Jumps, Throws, etc.)

## Key Findings

- External factors (country, sport, season, year) are stronger predictors of medal outcomes than athlete physical characteristics alone.
- Decision Trees outperformed Logistic Regression across both feature sets.
- Sport-specific models improved performance for several sports (e.g., Rowing, Fencing) compared to the global model.

## Project Structure

| File | Description |
|------|-------------|
| `DATA_301_Project_Models_Updated.ipynb` | Primary analysis, data cleaning, model training, sport-specific vs. global model comparison |
| `DATA_301_Project_SecondaryQuestion.ipynb` | Secondary analysis, athlete features vs. external factors comparison |
| `DATA 301 Final Project Poster.pdf` | Project poster summarizing findings |
| `DATA 301 Olympics Data Context.pdf` | Dataset context and background information |

## Requirements

- Python 3.x
- pandas, numpy, scikit-learn, plotnine
- kagglehub (for dataset download)
