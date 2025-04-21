# Titanic: Predicting Disaster Survivorship using Machine Learning

## Problem Statement

On April 15, 1912, during her maiden voyage, the widely considered "unsinkable" RMS Titanic sank after colliding with an iceberg. Unfortunately, there weren't enough lifeboats for everyone onboard, resulting in the death of 1502 out of 2224 passengers and crew.

While there was some element of luck involved in surviving, it seems some groups of people were more likely to survive than others.

This project aims to develop a machine learning model to capture the patterns and features affecting survivorship and accurately predict which type of individuals have a higher tendency to survive such disasters.

## Data Collection

The dataset used for this project can be accessed and downloaded at the following link: https://www.kaggle.com/competitions/titanic/data

There are two primary datasets:

- Training Set (`train.csv`): 891 rows, 12 columns
- Testing Set (`test.csv`): 418 rows, 11 columns (excluding target)

### Data Dictionary

| Column      | Data Type | Description                                                                                                       |
| ----------- | --------- | ----------------------------------------------------------------------------------------------------------------- |
| PassengerId | Integer   | Unique ID of passenger                                                                                            |
| Survived    | Integer   | Prediction target, whether the passenger survived or not (0 = No, 1 = Yes)                                        |
| Pclass      | Integer   | Ticket class (1 = 1st/Upper class, 2 = 2nd/Middle class, 3 = 3rd/Lower class)                                     |
| Name        | String    | Name of passenger                                                                                                 |
| Sex         | String    | Sex of passenger ("female", "male")                                                                               |
| Age         | Float     | Age in years (Fractional if estimated)                                                                            |
| SibSp       | Integer   | Number of siblings or spouses aboard ship                                                                         |
| Parch       | Integer   | Number of parents or children aboard ship                                                                         |
| Ticket      | String    | Ticket number (Note: There are multiple formats, and duplicates - due to some passengers sharing the same ticket) |
| Fare        | Float     | Ticket price                                                                                                      |
| Cabin       | String    | Cabin number (Example format: "C85"). Some passengers have multiple cabins listed in the same cell                |
| Embarked    | String    | Port of embarkation ("C" = Cherbourg, "Q" = Queenstown, "S" = Southampton)                                        |

## Data Exploration

### Duplicates

- There are no duplicated records

### Irrelevant Data

- `PassengerId`, `Name`, and `Ticket` are not needed for prediction (_Note:_ Might create feature for ticket if useful patterns found)

### Missing Values

- `Age`: 177 missing
- `Cabin`: 687 missing
- `Embarked`: 2 missing
- No more missing data in the rest of the features

### Inconsistent Formatting

- Column names are in PascalCase, should be reformatted to snake_case

### Data Type Issues

- Age is a float, due to uncertain ages being formatted as decimals

### Incorrect Values

- None as of the moment

### Outliers

- Will check up on this later
