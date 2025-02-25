# Data Science Project

This template is designed to jumpstart data science projects by providing a basic setup for database connections, data processing, and the development of machine learning models. It includes a structured folder organization for your datasets and a predefined set of Python packages required for most data science tasks.

## Structure

The project is organized as follows:

- `app.py` - The main Python script that you run for your project.
- `explore.py` - A notebook for your exploratory analysis; ideally, the code from this notebook is migrated to app.py for production.
- `utils.py` - This file contains utility code for operations such as database connections.
- `requirements.txt` - This file contains the list of necessary Python packages.
- `models/` - This directory should contain your SQLAlchemy model classes.
- `data/` - This directory contains the following subdirectories:
  - `interim/` - For intermediate data that has been transformed.
  - `processed/` - For the final data to be used for modeling.
  - `raw/` - For raw, unprocessed data.

## Setup

**Prerequisites**

Make sure you have Python 3.11+ installed on your machine. You will also need pip to install Python packages.

**Installation**

Clone the project repository to your local machine.

Navigate to the project directory and install the required Python packages:

```bash
pip install -r requirements.txt

# Business Understanding

## Project Description

This project aims to help the Portuguese bank identify existing customers with a higher probability of subscribing to a long-term deposit. Long-term deposits allow banks to hold funds for a specified period, enabling them to use these funds to improve their investments. Marketing campaigns for this product are based on telephone calls; if a user is unavailable at a given moment, they will be contacted again later.

## Problem Description

The Portuguese bank is experiencing a decline in its revenues, so they want to identify existing customers who have a higher probability of subscribing to a long-term deposit. This will allow them to focus their marketing efforts on those customers and avoid wasting time and resources on those who are unlikely to subscribe.

To address this problem, a classification algorithm will be developed to predict whether a customer will subscribe to a long-term deposit or not.

## Data

The dataset is contained in the file `bank-marketing-campaign-data.csv` and can be loaded directly from the following link:  
https://raw.githubusercontent.com/4GeeksAcademy/logistic-regression-project-tutorial/main/bank-marketing-campaign-data.csv

The dataset contains the following variables:

- **age:** Customer's age (numeric)
- **job:** Type of job (categorical)
- **marital:** Marital status (categorical)
- **education:** Level of education (categorical)
- **default:** Has credit in default? (categorical)
- **housing:** Has a housing loan? (categorical)
- **loan:** Has a personal loan? (categorical)
- **contact:** Contact communication type (categorical)
- **month:** Last month contacted (categorical)
- **day_of_week:** Last day contacted (categorical)
- **duration:** Duration of the previous contact in seconds (numeric)
- **campaign:** Number of contacts made during this campaign (numeric)
- **pdays:** Number of days since the last campaign until contact (numeric)
- **previous:** Number of contacts made during the previous campaign (numeric)
- **poutcome:** Outcome of the previous marketing campaign (categorical)
- **emp.var.rate:** Employment variation rate (numeric, quarterly indicator)
- **cons.price.idx:** Consumer price index (numeric, monthly indicator)
- **cons.conf.idx:** Consumer confidence index (numeric, monthly indicator)
- **euribor3m:** 3-month EURIBOR rate (numeric, daily indicator)
- **nr.employed:** Number of employees (numeric, quarterly indicator)
- **y (TARGET):** Whether the customer subscribes to a long-term deposit (categorical)

## Project Steps

### Step 1: Data Loading

Load the dataset from the provided link or download it manually and include it in your repository.

### Step 2: Exploratory Data Analysis (EDA)

Perform a comprehensive exploratory data analysis to:

- Identify and select the relevant variables.
- Remove variables that do not provide significant information.
- Split the dataset into training and testing sets, following best practices.

Use the provided example Notebook and adapt it to this use case.

### Step 3: Build the Logistic Regression Model

Create a logistic regression model to predict the probability that a customer will subscribe to a long-term deposit. Start with the default parameters and evaluate the model's performance.

### Step 4: Model Optimization

If the initial results are not satisfactory, apply optimization techniques (such as hyperparameter tuning or feature selection) to improve the model's performance.

## Requirements

- **Python 3.x**
- **Libraries:** `pandas`, `numpy`, `scikit-learn`, `matplotlib`/`seaborn` (or other visualization libraries)
