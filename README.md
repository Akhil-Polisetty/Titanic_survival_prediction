Titanic Survival Prediction

This project aims to predict the survival chances of passengers aboard the Titanic using a logistic regression model. The focus is on thorough data preprocessing and model training to achieve reliable results.

Table of Contents

Introduction

Dataset Description

Data Preprocessing

Modeling

Results

Installation and Usage

Future Enhancements

Contributors

Introduction

The Titanic disaster is one of the most infamous shipwrecks in history. Using historical passenger data, this project predicts whether a passenger survived or not based on features like age, gender, class, etc. Logistic regression is used for its simplicity and efficiency in binary classification tasks.

Dataset Description

The dataset is obtained from the Kaggle Titanic competition: Titanic Dataset.

Key Features

Survived: Target variable (0 = No, 1 = Yes)

Pclass: Ticket class (1st, 2nd, 3rd)

Sex: Gender of the passenger

Age: Age of the passenger

SibSp: Number of siblings/spouses aboard

Parch: Number of parents/children aboard

Fare: Ticket fare

Embarked: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

Missing Values

Age: Contains missing values

Cabin: Contains a significant number of missing values (excluded from modeling)

Embarked: Contains a few missing values

Data Preprocessing

Data preprocessing is critical to improve the performance of the logistic regression model. Steps include:

Handling Missing Values

Age: Filled using median age grouped by Pclass and Sex.

Embarked: Filled with the mode of the Embarked column.

Cabin: Dropped due to a large number of missing values.

Feature Engineering

Binning Age: Age is binned into categories (child, young adult, adult, senior).

Creating FamilySize: Derived from SibSp + Parch + 1.

IsAlone: Created a binary feature to indicate if a passenger was alone.

Encoding Categorical Variables

Sex: Converted to binary (0 = male, 1 = female).

Embarked: One-hot encoded.

Scaling Numeric Features

Scaled features like Fare using Min-Max scaling for better convergence.

Modeling

Logistic Regression

Logistic regression is used due to its simplicity and interpretability. The model was trained using the following libraries:

Scikit-learn for building the pipeline and training the model.

NumPy and Pandas for data manipulation.

Matplotlib and Seaborn for data visualization.

Model Evaluation

Accuracy: Measured on the training and validation datasets.

Confusion Matrix: Evaluated true positives, true negatives, false positives, and false negatives.

ROC-AUC Score: Assessed the model's performance in classification.

Results

Achieved an accuracy of ~80% on the validation set.

The model identified significant predictors of survival, including Sex, Pclass, and Fare.
