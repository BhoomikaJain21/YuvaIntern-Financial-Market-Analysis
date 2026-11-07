# Financial Market Analysis

A Python-based financial market analysis project focused on collecting, cleaning, exploring, visualizing, and modeling historical stock market data for **Infosys, Reliance Industries, and Tata Consultancy Services (TCS)**.

This repository documents the weekly progress and deliverables of my **YuvaIntern Financial Market Analysis project**, from initial project planning and data preparation to exploratory data analysis and predictive modeling.

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)

## Table of Contents

- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Companies Covered](#companies-covered)
- [Tools and Technologies](#tools-and-technologies)
- [Project Workflow and Weekly Progress](#project-workflow-and-weekly-progress)
  - [Week 1 – Project Planning](#week-1--project-planning)
  - [Week 2 – Data Collection and Preprocessing](#week-2--data-collection-and-preprocessing)
  - [Week 3 – Exploratory Data Analysis](#week-3--exploratory-data-analysis)
  - [Week 4 – Predictive Modeling and Evaluation](#week-4--predictive-modeling-and-evaluation)
- [Week 4 Model Performance](#week-4-model-performance)
- [Repository Structure](#repository-structure)
- [Installation and Setup](#installation-and-setup)
- [Key Learnings](#key-learnings)
- [Limitations and Future Improvements](#limitations-and-future-improvements)
- [Conclusion](#conclusion)

## Project Overview

The project analyzes historical stock market data for three major Indian companies: Infosys, Reliance Industries, and TCS.

Using Python and its data analysis ecosystem, the project follows a structured workflow:

1. Planning the analysis and identifying relevant financial metrics.
2. Collecting historical stock market data.
3. Cleaning and preparing the datasets.
4. Performing exploratory data analysis (EDA).
5. Visualizing price movements, returns, volatility, and relationships between stocks.
6. Building and evaluating predictive models for next-trading-day adjusted closing prices.

The objective is to apply practical data analytics and machine learning techniques to real-world financial datasets while documenting the methodology, findings, and limitations.

## Objectives

- Collect historical stock market data for selected companies.
- Assess data quality and handle missing or inconsistent observations.
- Perform exploratory analysis to understand price trends, returns, and volatility.
- Identify patterns and relationships through statistical analysis and visualization.
- Engineer features suitable for time-dependent predictive modeling.
- Develop and evaluate a Linear Regression model.
- Compare model performance against a simple baseline.
- Communicate findings through notebooks, visualizations, and reports.

## Companies Covered

| Company | Yahoo Finance Ticker |
|---|---|
| Infosys | `INFY.NS` |
| Reliance Industries | `RELIANCE.NS` |
| Tata Consultancy Services | `TCS.NS` |

**Data period:** 1 November 2023 – 30 October 2026.

**Data source:** Yahoo Finance, accessed using the `yfinance` Python library.

## Tools and Technologies

| Tool / Library | Application |
|---|---|
| Python | Programming and analysis |
| Jupyter Notebook | Interactive analysis and documentation |
| Pandas | Data manipulation and preprocessing |
| NumPy | Numerical computations |
| yfinance | Historical market data collection |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Scikit-learn | Predictive modeling and evaluation |
| Git and GitHub | Version control and project hosting |

## Project Workflow and Weekly Progress

### Week 1 – Project Planning

Established the scope and objectives of the Financial Market Analysis project.

The planning stage included:

- Selecting Infosys, Reliance Industries, and TCS for analysis.
- Identifying Yahoo Finance as the historical data source.
- Defining the approximate three-year analysis period.
- Identifying relevant financial variables and analytical objectives.
- Outlining the data collection, preprocessing, visualization, and analysis workflow.

**Deliverable:** [Week 1 Project Plan](./Financial%20Market%20Analysis%20Week%201%20Project%20Plan.pdf)

### Week 2 – Data Collection and Preprocessing

Collected historical stock market data and performed data quality assessment and preprocessing.

Key activities:

- Downloaded historical data for all three companies using `yfinance`.
- Organized raw and cleaned datasets.
- Examined missing values, duplicate records, data consistency, and invalid observations.
- Investigated outliers and corporate-action-related price adjustments.
- Prepared individual cleaned datasets and a combined dataset.
- Generated visualizations of normalized stock prices and rolling volatility.

**Dataset summary:**

| Metric | Result |
|---|---:|
| Companies analyzed | 3 |
| Records collected | 2,220 |
| Records per company | 740 |
| Duplicate records | 0 |
| Missing essential values after cleaning | 0 |
| Unique outlier records identified | 184 |

**Deliverables:** Raw and cleaned datasets, quality assessment reports, visualizations, and the Week 2 report, all under [`week-2/Financial_Market_Analysis/`](./week-2/Financial_Market_Analysis/).

### Week 3 – Exploratory Data Analysis

Performed exploratory data analysis to understand the historical behavior of the selected stocks.

The analysis focused on:

- Daily stock returns and their distributions.
- Monthly average returns.
- Normalized stock price trends.
- Rolling volatility.
- Correlations between company returns.
- Relationships between stock returns using scatter plots.
- Comparative analysis of the three companies.

**Visualizations included** (in [`week-3/week_3_visualizations/`](./week-3/week_3_visualizations/)):

| Visualization | File |
|---|---|
| Daily return box plot | [`daily_return_boxplot.png`](./week-3/week_3_visualizations/daily_return_boxplot.png) |
| Daily return distribution | [`daily_return_distribution.png`](./week-3/week_3_visualizations/daily_return_distribution.png) |
| Monthly average returns | [`monthly_average_returns.png`](./week-3/week_3_visualizations/monthly_average_returns.png) |
| Normalized price trends | [`normalized_price_trends.png`](./week-3/week_3_visualizations/normalized_price_trends.png) |
| Return correlation heatmap | [`return_correlation.png`](./week-3/week_3_visualizations/return_correlation.png) |
| Return scatter plots | [`return_scatterplots.png`](./week-3/week_3_visualizations/return_scatterplots.png) |
| Rolling volatility | [`rolling_volatility.png`](./week-3/week_3_visualizations/rolling_volatility.png) |

**Deliverables:**

- [`week3_eda.ipynb`](./week-3/week3_eda.ipynb)
- [`Week3_EDA_Report.docx`](./week-3/Week3_EDA_Report.docx)
- [Week 3 visualization folder](./week-3/week_3_visualizations/)

### Week 4 – Predictive Modeling and Evaluation

Developed predictive models to forecast the next trading day's adjusted closing price for Infosys, Reliance Industries, and TCS.

**Target variable**

The target was defined as the next trading day's adjusted closing price (`adj_close`).

**Feature engineering**

Created lagged and current-day market features, including:

- Current closing price.
- Closing prices from previous trading days.
- Current and lagged trading volume.
- Current and lagged daily returns.
- Current and lagged rolling volatility.

**Model development**

- Used separate Linear Regression models for each company.
- Applied an 80:20 chronological train-test split without shuffling.
- Used `StandardScaler` for feature scaling.
- Implemented preprocessing and modeling through a Scikit-learn Pipeline.
- Fitted preprocessing steps using training data only.

**Baseline comparison**

Compared Linear Regression against a naive baseline that predicts the next trading day's adjusted closing price using the current day's adjusted closing price.

**Evaluation metrics**

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)

**Deliverables:**

- [`week-4.ipynb`](./week-4/week-4.ipynb) – Predictive modeling notebook.
- [`Week4_Predictive_Modeling_Report.docx`](./week-4/Week4_Predictive_Modeling_Report.docx) – Detailed methodology, results, visualizations, and interpretation.
- [`figures/`](./week-4/figures/) – Actual-versus-predicted and residual analysis plots.

## Week 4 Model Performance

The following table presents the test-set evaluation results.

| Company | Model | MAE | MSE | RMSE | R² |
|---|---|---:|---:|---:|---:|
| Infosys | Linear Regression | 19.099 | 594.661 | 24.386 | 0.888 |
| Infosys | Naive Baseline | 18.220 | 574.146 | 23.961 | 0.892 |
| Reliance | Linear Regression | 14.114 | 321.298 | 17.925 | 0.917 |
| Reliance | Naive Baseline | 14.024 | 321.026 | 17.917 | 0.917 |
| TCS | Linear Regression | 36.445 | 2391.187 | 48.900 | 0.892 |
| TCS | Naive Baseline | 34.983 | 2332.648 | 48.297 | 0.894 |

**Key observations:**

- The naive baseline marginally outperformed Linear Regression on MAE, MSE, and RMSE for all three companies.
- Reliance Industries showed the smallest difference between the two approaches.
- The results demonstrate the importance of comparing predictive models against simple benchmarks.
- High R² values alone do not establish that a model is better than a baseline, particularly when predicting persistent financial price series.

The results suggest that the tested Linear Regression approach did not provide an improvement over simply using the current adjusted closing price as the next-day prediction.

## Repository Structure

The repository is organized by project week.

```text
YuvaIntern-Financial-Market-Analysis/
│
├── Financial Market Analysis Week 1 Project Plan.pdf
│
├── week-2/
│   └── Financial_Market_Analysis/
│       ├── raw_data/
│       ├── cleaned_data/
│       ├── reports/
│       └── visualizations/
│
├── week-3/
│   ├── week3_eda.ipynb
│   ├── Week3_EDA_Report.docx
│   └── week_3_visualizations/
│       ├── daily_return_boxplot.png
│       ├── daily_return_distribution.png
│       ├── monthly_average_returns.png
│       ├── normalized_price_trends.png
│       ├── return_correlation.png
│       ├── return_scatterplots.png
│       └── rolling_volatility.png
│
├── week-4/
│   ├── week-4.ipynb
│   ├── Week4_Predictive_Modeling_Report.docx
│   └── figures/
│       ├── actual_vs_predicted_prices.png
│       └── residual_analysis.png
│
└── README.md
```

> **Note:** This structure summarizes the project organization. Refer to the repository for the complete list of files and datasets.

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/BhoomikaJain21/YuvaIntern-Financial-Market-Analysis.git
cd YuvaIntern-Financial-Market-Analysis
```

### 2. Install the required libraries

No `requirements.txt` is included. The following installs the libraries used in the notebooks:

```bash
pip install pandas numpy matplotlib seaborn yfinance scikit-learn jupyter
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open the required weekly notebook and execute its cells.

> **Note:** Ensure that the datasets are placed at the paths expected by the notebooks. In particular, the Week 4 notebook requires the combined cleaned dataset used during model development.

## Key Learnings

Through this project, I worked on:

- Collecting historical financial data using Python.
- Assessing data quality and preparing datasets for analysis.
- Performing exploratory data analysis on stock market data.
- Creating meaningful visualizations to communicate trends and patterns.
- Engineering lagged features for time-dependent prediction.
- Applying chronological train-test splitting to avoid future-data leakage.
- Building machine learning pipelines using Scikit-learn.
- Evaluating regression models using multiple performance metrics.
- Comparing machine learning models against baseline approaches.
- Interpreting model limitations and communicating findings objectively.

## Limitations and Future Improvements

The project provides a structured analysis of historical stock market data, but several improvements could be explored:

- Evaluate additional forecasting approaches.
- Explore more advanced time-series models.
- Incorporate additional market indicators and relevant external variables.
- Perform systematic hyperparameter tuning and time-series cross-validation.
- Investigate whether predicting returns rather than price levels provides more useful insights.
- Evaluate model performance across different market conditions.

These are potential future improvements and are not presented as completed work.

## Conclusion

This project demonstrates an end-to-end financial data analysis workflow, covering data collection, preprocessing, exploratory analysis, visualization, feature engineering, predictive modeling, and model evaluation.

An important finding from the predictive modeling stage was that a simple naive baseline performed marginally better than the tested Linear Regression models. This reinforces the importance of benchmarking machine learning models and interpreting evaluation metrics in the context of the problem.

The repository serves as a record of the practical analytical techniques, tools, and methods applied throughout the YuvaIntern project.

---

**Project:** YuvaIntern – Financial Market Analysis
**Repository:** [BhoomikaJain21/YuvaIntern-Financial-Market-Analysis](https://github.com/BhoomikaJain21/YuvaIntern-Financial-Market-Analysis)
