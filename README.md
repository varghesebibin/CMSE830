# CMSE 830 Midsemester Project

This repository contains the **House Price Prediction** project for the CMSE 830 Midsemester assessment, along with a secondary analysis focused on US macroeconomic indicators such as unemployment rate and industrial production. The project involves predicting house prices using Ridge and Lasso regression models, performing detailed model building and evaluation, as well as analyzing the US economy using key economic indicators.



## Table of Contents

- [Introduction](#introduction)
- [Project Structure](#project-structure)
- [Datasets](#datasets)
- [Features](#features)
- [Setup and Installation](#setup-and-installation)
- [How to Run the Project](#how-to-run-the-project)
- [Key Insights](#key-insights)
- [Technologies Used](#technologies-used)
- [Visualizations](#visualizations)
- [Notebook Sections](#notebook-sections)

## Introduction

The **House Price Prediction** project focuses on analyzing and predicting house prices using a dataset that includes several features, such as `OverallQual`, `GrLivArea`, `GarageCars`, `TotalBsmtSF`, and more. Additionally, a second analysis explores key US macroeconomic indicators, including the unemployment rate and industrial production.

This repository includes:

- **House Price Prediction**: Detailed Exploratory Data Analysis (EDA), data visualization, feature engineering, and regression modeling.
- **Macroeconomic Indicators Analysis**: Analysis of the US economy using macroeconomic data on unemployment rate and industrial production from a Kaggle dataset.

## Project Structure

The project contains the following key files and directories:

- `application.py`: Main Streamlit application file for running the project.
- `train.csv`: Dataset used for house price prediction.
- `requirements.txt`: List of Python libraries needed to run the project.
- `House Price Prediction Using Advanced Regression.ipynb`: Jupyter notebook containing the full analysis, including data exploration, visualization, feature engineering, model building, and evaluation.
- `README.md`: Documentation for the repository.

## Datasets

The project utilizes two distinct datasets:

1. **House Price Dataset** (`train.csv`):
   - This dataset contains house price data, including several numerical and categorical features. The dataset is used to predict house prices using Ridge and Lasso regression models.
   
2. **US Macroeconomic Indicators Dataset** (from Kaggle):
   - <a href="https://www.kaggle.com/datasets/calven22/usa-key-macroeconomic-indicators" target="_blank">Kaggle Dataset: US Key Macroeconomic Indicators</a>
   - This dataset contains macroeconomic data, including the unemployment rate and industrial production, which are analyzed for trends post-2000. The analysis provides insights into how these factors have influenced the US economy.

## Features

- **Data Exploration**: Interactive exploration of key features in the dataset using visualizations and statistical summaries.
- **Imputation of Missing Values**: Handling missing data with techniques such as filling with the median or using categorical replacements.
- **Feature Engineering**: Creation and transformation of new features to improve model performance.
- **Model Building and Evaluation**: Training and evaluating Ridge and Lasso regression models using various performance metrics like Mean Absolute Error (MAE) and R².
- **Macroeconomic Analysis**: Analyzing the unemployment rate and industrial production trends in the US economy post-2000.
- **Interactive Streamlit App**: A web app that allows users to explore different sections (EDA, Visualization, Imputation, etc.) and make predictions.

## Setup and Installation

To run this project locally, follow these steps:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/varghesebibin/CMSE830_Midsemester_Project.git
    cd CMSE830_Midsemester_Project
    ```

2. **Create a virtual environment** (optional but recommended):
    ```bash
    python -m venv streamlitenv
    source streamlitenv/bin/activate  # On Windows: streamlitenv\Scripts\activate
    ```

3. **Install the required dependencies**:
    Make sure you have `pip` installed, then install the required libraries:
    ```bash
    pip install -r requirements.txt
    ```

4. **Set up the dataset**:
    Ensure the `train.csv` file is present in the root directory. If it’s missing, upload your dataset or use your own version.

## How to Run the Project

To run the **Streamlit** app, follow these steps:

1. Open your terminal (ensure you are in the root directory of the project).
2. Run the Streamlit app:
    ```bash
    streamlit run application.py
    ```

3. **Access the app**: Open your web browser and go to the local URL provided (`https://cmse830midsemesterproject-gxbhpk4wstunehwvrgvjgk.streamlit.app/`).

## Key Insights

Here are some of the important findings from the project:

- **OverallQual** and **GrLivArea** have the strongest positive correlations with house prices.
- **Newer houses** tend to have higher sale prices, especially those built after the 2000s.
- **GarageCars** and **GarageArea** are highly correlated, indicating that one can be dropped to avoid multicollinearity in the model.
- **Feature Engineering** and **Imputation** were crucial steps to improving the model's predictive power.
- **US Macroeconomic Indicators**: Post-2000, there were clear trends in the **unemployment rate** and **industrial production**, affecting the overall economy, and these factors were analyzed in detail in the Jupyter Notebook.
- **Ridge** and **Lasso Regression** models were evaluated, and hyperparameter tuning was performed to select the best model.

## Technologies Used

- **Python 3.12.4**: Core programming language.
- **Pandas**: Data manipulation and analysis.
- **Matplotlib** and **Seaborn**: Data visualization.
- **Scikit-learn**: Machine learning, particularly for Ridge and Lasso regression.
- **Streamlit**: Interactive web app framework for displaying the project.
- **HiPlot**: Visualization tool for interactive exploration of feature relationships.
- **Altair**: Additional interactive visualizations.
- **Jupyter Notebook**: Used for data exploration, model building, and evaluation.

## Visualizations

The following visualizations are available within the project:

1. **Distribution of Sale Prices**: Displays the distribution of house prices in the dataset.
2. **Scatter Plot of GrLivArea vs SalePrice**: Shows how the ground living area affects sale prices.
3. **Scatter Plot of TotalBsmtSF vs SalePrice**: Analyzes how basement area impacts house prices.
4. **Boxplot of OverallQual vs SalePrice**: Compares overall quality with house prices.
5. **Heatmap of Correlations**: Displays correlations between key numerical features.
6. **HiPlot**: An interactive HiPlot for exploring relationships between key features and sale prices.
7. **US Macroeconomic Indicator Plots**: Visualization of trends in **unemployment rate** and **industrial production**

## Notebook Sections

The **Jupyter Notebook** file (`House Price Prediction Using Advanced Regression`) contains a comprehensive analysis of the data. The key sections are as follows:

### 1. **Data Exploration**
- Detailed exploration of the dataset's structure, including the distribution of key variables like `SalePrice`, `GrLivArea`, and `OverallQual` (house price).
- Analysis of the US economy post-2000 using key macroeconomic indicators such as the **unemployment rate** and **industrial production**.
- Insights on how these factors influenced the economy post-2000.
- Visualization of correlations and relationships between variables using scatter plots, histograms, and boxplots.

### 2. **Exploratory Data Analysis (EDA)**
- Visualizations to explore the impact of different features on house prices.
- Identifying outliers and multicollinearity between features.

### 3. **Visualization**
- Use of various plotting techniques to visualize feature relationships.
- Heatmaps, pair plots, and HiPlot were used to display multivariate relationships.

### 4. **Imputation of Missing Values**
- Handling missing values using various imputation techniques, including filling with medians and replacing categorical variables.

### 5. **Feature Engineering**
- Transformation of raw features into more useful variables for modeling.
- Creating interaction terms and handling categorical variables.

### 6. **Model Building and Evaluation**
- Training Ridge and Lasso regression models.
- Hyperparameter tuning using cross-validation to optimize the models.
- Model evaluation using performance metrics such as Mean Absolute Error (MAE) and R².


