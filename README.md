# Titanic Survival Prediction – Machine Learning Modeling

## Project Overview

This project predicts whether a passenger survived the Titanic disaster using historical passenger data from the Kaggle Titanic dataset. The task is a binary classification problem where the target variable is `Survived`.

The project follows a complete machine learning workflow, including data exploration, data cleaning, feature engineering, model training, evaluation, and final prediction generation.

## Problem Statement

The objective of this project is to build a machine learning model that can predict passenger survival based on features such as passenger class, sex, age, family size, fare, embarkation point, and other engineered features.

## Dataset Overview

The dataset contains passenger information from the Titanic disaster.

### Files Used

- `train.csv` – training dataset with known survival outcomes
- `test.csv` – test dataset without survival outcomes
- `gender_submission.csv` – sample submission format

### Key Columns

- `PassengerId`
- `Survived`
- `Pclass`
- `Name`
- `Sex`
- `Age`
- `SibSp`
- `Parch`
- `Ticket`
- `Fare`
- `Cabin`
- `Embarked`

## Project Workflow

1. Problem Understanding
2. Data Loading
3. Exploratory Data Analysis
4. Missing Value Treatment
5. Feature Engineering
6. Encoding and Scaling
7. Model Training
8. Model Evaluation
9. Final Prediction
10. Submission File Creation

## Feature Engineering

The following new features were created to improve model performance:

- `FamilySize` – total number of family members travelling with the passenger
- `IsAlone` – identifies whether the passenger travelled alone
- `Title` – extracted from passenger names
- `AgeGroup` – groups passengers into age categories
- `FarePerPerson` – fare divided by number of people in the family group
- `HasCabin` – identifies whether cabin information is available

## Models Used

The following machine learning models were trained and compared:

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- Gradient Boosting Classifier

## Evaluation Metrics

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- Cross-validation score
- ROC-AUC score

## Results and Findings

The final model was selected based on validation performance and generalization ability. Key findings from the analysis showed that passenger sex, passenger class, age, fare, title, and family-related features had a strong relationship with survival.

## Tools and Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- GitHub

## Project Structure

```text
titanic-survival-prediction/
│
├── data/
│   ├── train.csv
│   ├── test.csv
│   └── gender_submission.csv
│
├── notebooks/
│   └── titanic_survival_prediction.ipynb
│
├── outputs/
│   └── titanic_submission.csv
│
├── presentation/
│   └── titanic_survival_prediction.pptx
│
├── README.md
├── requirements.txt
└── .gitignore