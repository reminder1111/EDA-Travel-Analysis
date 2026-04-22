# EDA Travel Analysis

This project is an Exploratory Data Analysis (EDA) of a travel customer dataset focused on travel package purchase behavior.

## Dataset

The analysis uses the Travel.csv file included in this repository.

Based on the file name and the column structure, this dataset appears to match the Kaggle holiday package prediction dataset:
[Kaggle Holiday Package Prediction](https://www.kaggle.com/datasets/susant4learning/holiday-package-purchase-prediction)

The dataset includes customer and travel-related features such as:
- ProdTaken
- Age
- Gender
- CityTier
- TypeofContact
- Occupation
- ProductPitched
- DurationOfPitch
- NumberOfTrips
- Passport
- OwnCar
- MonthlyIncome
- MaritalStatus
- Designation

## What Happens In This EDA

In the notebook, the dataset is first loaded and explored using:
- shape and column checks
- data type inspection
- missing value checks
- general overview of the dataset

Then a few cleaning steps are done:
- the inconsistent gender value Fe Male is corrected to Female
- missing rows are removed using dropna()

After that, the notebook explores customer and package-related patterns through visualizations, including:
- countplots for categorical features
- histograms for numerical features
- age distribution
- type of contact distribution
- age vs duration of pitch by ProdTaken
- marital status vs package purchase using a stacked bar chart
- product pitched vs pitch satisfaction score
- age vs purchase behavior with OwnCar
- gender vs age with ProdTaken
- a 3D plot of age, monthly income, and duration of pitch
- correlation heatmap for numeric features

The notebook also starts a basic machine learning preparation step by separating features and target:
- X = df.drop('ProdTaken', axis=1)
- y = df['ProdTaken']

## Purpose

The main purpose of this EDA is to understand which customer characteristics are connected with travel package purchase decisions.

This project helps answer questions like:
- which customer groups are more common in the dataset
- how age and income relate to travel package behavior
- how contact type and product pitch may affect customer response
- which variables look more useful for predicting ProdTaken
- what patterns can help in future package targeting or customer segmentation

## Files

- 4. EDA Travel.ipynb : Jupyter notebook with the full EDA
- Travel.csv : dataset used in the analysis