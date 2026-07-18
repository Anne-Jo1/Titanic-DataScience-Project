# BCS 404 Project: Titanic Exploratory Data Analysis, Statistical Analysis and Machine Learning

## Overview

This repository contains the complete project work for **BCS 404: Introduction to Data Science with Python**, Accra Technical University (2025/2026, Second Semester), under the supervision of Dr. Joseph Dadzie.

The project applies a full data science workflow — data acquisition, data cleaning, data visualisation, statistical analysis, and machine learning — to the [Titanic dataset](https://www.kaggle.com/competitions/titanic/data) from Kaggle.

## Repository Contents

- `BCS404_Titanic_Project.ipynb` — Jupyter Notebook containing all executed Python code, outputs, and charts for Tasks 1–5 (data acquisition, cleaning, visualisation, statistical analysis, and machine learning).
- `BCS404_Project_Report.pdf` — Full written report (cover page, table of contents, introduction, dataset description, methodology, results, discussion, conclusion, references, and code appendix).
- `README.md` — This file.

## Dataset

- **Source:** [Kaggle Titanic Competition](https://www.kaggle.com/competitions/titanic/data)
- **Rows / Columns:** 891 passengers, 12 variables
- **Target variable:** `Survived` (0 = did not survive, 1 = survived)

The notebook loads the data directly from a public mirror with identical structure and values to the Kaggle `train.csv`, so it runs end-to-end without any manual download. See the notebook for an alternate cell to load your own downloaded `train.csv` instead.

## Summary of Methodology

1. **Data Acquisition** — Imported the dataset and inspected its shape, columns, and data types.
2. **Data Cleaning** — Handled missing values in `Age` (median imputed by `Pclass`/`Sex` group), `Cabin` (converted to a `Has_Cabin` binary flag), and `Embarked` (mode imputed). Checked for and removed duplicate rows (none were found).
3. **Data Visualisation** — Produced a histogram of ages, a bar chart of passenger class, a boxplot of age by class, a scatter plot of age vs. fare, a correlation heatmap, and a pairplot of key numerical variables.
4. **Statistical Analysis** — Computed descriptive statistics, frequency distributions, and a full correlation matrix; identified the strongest positive correlation (`Parch` & `SibSp`, r = 0.415) and strongest negative correlation (`Fare` & `Pclass`, r = −0.549).
5. **Machine Learning** — Trained a Logistic Regression classifier (Scikit-Learn) on `Pclass`, `Sex`, `Age`, `Fare`, `SibSp`, `Parch`, and `Embarked`, using an 80/20 stratified train/test split. Achieved **81.56% accuracy** on the test set, evaluated with a confusion matrix and full classification report.

## How to Run

1. Clone this repository:
   ```bash
   git clone <this-repository-url>
   cd <repository-folder>
   ```
2. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn scipy jupyter
   ```
3. Launch the notebook:
   ```bash
   jupyter notebook BCS404_Titanic_Project.ipynb
   ```
4. Run all cells (Cell → Run All). The dataset is fetched automatically at runtime.

## Key Results

| Metric                         | Value                          |
| ------------------------------ | ------------------------------ |
| Dataset size                   | 891 rows × 12 columns          |
| Missing values handled         | `Age`, `Cabin`, `Embarked`     |
| Duplicate rows found           | 0                              |
| Strongest positive correlation | `Parch` & `SibSp` (r = 0.415)  |
| Strongest negative correlation | `Fare` & `Pclass` (r = −0.549) |
| Model                          | Logistic Regression            |
| Test accuracy                  | 81.56%                         |

## Author

Okoumba Mitchowanou Anne Jolie — Computer Science, Accra Technical University

## Academic Integrity

This work was produced individually in accordance with Accra Technical University's Examination Regulations on academic integrity.
