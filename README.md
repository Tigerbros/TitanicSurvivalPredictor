# Titanic Survival Prediction

## Overview
This project analyzes the Titanic dataset and builds predictive models to determine passenger survival rates based on various features. The main objective is to explore which factors contributed to survival and develop a model that can predict survival based on passenger information.

## System Requirements
To run this project, ensure you have the following libraries installed
```bash
pip install pandas seaborn matplotlib numpy
```
for any other library find them on the internet.

## Data
**Source**:[Kaggle](https://www.kaggle.com/datasets/yasserh/titanic-dataset)

## Project Stages

### Load Dataset
* **Action**: The Titanic dataset was loaded into the environment using **pandas**.
* **Description**: The dataset contains information on passengers, including demographics and survival-relevant details. Features include: 
    - **PassengerId**: Ticket class (1st, 2nd, 3rd)
    - **Pclass**: Ticket class (1st, 2nd, 3rd)
    - **Sex**: Gender of the passenger
    - **Age**: Age of the passenger
    - **SibSp**: Number of siblings or spouses aboard
    - **Parch**: Number of parents or children aboard
    - **Fare**: Ticket fare
    - **Embarked**: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)
---
### Exploratory Data Analysis (EDA)
* **Actions**: Used **.head()** to preview the initial rows of the dataset.
* Created count plots and histograms to visualize survival distributions across different categories like **Pclass (Passenger Class)**, **Sex**, and **Age**.
* Utilized box plots and additional visualizations to analyze relationships between passenger class, age, and survival and detect Outliers.
* **Key Findings**:Survival rates varied significantly across passenger classes and gender. Females and higher-class passengers exhibited higher survival rates.
* Higher fares were generally associated with a greater likelihood of survival, likely reflecting distinctions in passenger class.
---
### Data Preprocessing
* **Actions**:Handling Missing Values: Used the median age within each passenger class (1st, 2nd, or 3rd) from the IQR to fill missing values in the **Age** column, with a custom **fill_age** function.
* **Dropping Columns**: The **Cabin** column was removed due to its high number of missing values.
* **Encoding Categorical Variables**: Converted categorical features **Sex** and **Embarked** into numerical formats.
---
### Feature Extraction
* **Selection of Predictive Features**: Identified key features for predicting **'Passengerclass', 'Age', 'SiblingsSpouse', 'ParentChild','Fare', 'male', 'Q', 'S'**.
---
### Modelling
used only one machine learning model
- **Model**:
    - Logistic Regression: used as the baseline model
- **Evaluation Metrics**: precission, recall, f1-score,support,accuracy.

## Results
- **Final Results**: The model attained an Accuracy Score of **82.5%**

## Contributing
```markdown
1. Fork the repository
2. Create a new branch(`feature-branch`)
3. Add extra Data stages
4. Submit a pull request
```
## Acknowledgemtns
- **Inspiration**: This project was inspired by my Personal learning.