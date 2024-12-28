# Market-Trend-Analysis-and-Price-Prediction-on-Used-Cars

This project aims to analyze market trends in the used car market and develop a predictive model for estimating car prices based on various features. By understanding factors affecting prices, this analysis can assist car buyers, sellers, and dealers make informed decisions.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Data Collection](#data-collection)
3. [Features](#features)
4. [Methodology](#methodology)
5. [Requirements](#requirements)
6. [Installation](#installation)
7. [Usage](#usage)
8. [Results](#results)
9. [Contributions](#contributions)
10. [License](#license)

------------------------

## Project Overview

The used car market is complex and influenced by make, model, age, mileage, condition, and location. This project provides:
- **Market Trend Analysis**: Insight into price patterns across car makes, models, and locations.
- **Price Prediction**: A machine learning model to predict car prices based on selected features, providing a helpful tool for stakeholders.

-----------------------
## Data Collection

The data for this project was obtained through web scraping. Details of the data collection process are as follows:

### 1. Web Scraping
- **Source**: Data was scraped from the [Cars24 website](https://www.cars24.com/), which provides detailed listings of used cars available for sale across various cities.
- **Libraries Used**: The scraping was done using **BeautifulSoup** and **Selenium** to extract relevant details, including make, model, year, mileage, condition, location, and price.
- **Coverage**: Information on used cars was scraped from listings across **11 different cities**, providing a broad view of regional market trends and pricing.

This scraped dataset is the basis for analyzing market trends and building machine-learning models for price prediction.

-------------------------

## Features

1. **Name**: Contains information about the car's year, make, and model.
2. **Trim**: Specifies different pre-packaged groups of features available for a particular car.
3. **Transmission**: Indicates the transmission type, either Automatic or Manual.
4. **kms_driven**: The total number of kilometres driven by the car.
5. **ownership_status**: The number of previous vehicle owners.
6. **fuel_type**: The type of fuel the car uses (e.g., petrol, diesel, CNG).
7. **emi_per_month**: The estimated EMI (Equated Monthly Installment) payment to be made monthly.
8. **original_price**: The original price of the car when first sold.
9. **reduced_price**: The reduced price of the car reflects its current valuation.
10. **City**: The city where the car is listed for sale.

These attributes form the basis for market trend analysis and price prediction in this project.

------------------------

## Methodology

The project follows these main steps:

1. **Web Scraping**:
   - Data was collected by scraping car listing information from [Cars24](https://www.cars24.com/) using BeautifulSoup and Selenium.

2. **Data Preprocessing**:
   - Cleaning the data and handling missing values.
   - Preparing the dataset for analysis by scaling numerical features and selecting relevant features.

3. **Feature Engineering**:
   - Created new features from existing ones to enhance model performance.

4. **Exploratory Data Analysis (EDA)**:
   - Analyzed the distribution of car prices to understand price patterns.
   - Identified key features that significantly impact car prices.
   - Visualized trends across different car models, brands, and locations.

5. **Data Transformation**:
   - Transformed data as needed, including encoding and scaling, to improve model performance.

6. **Outlier Detection**:
   - Identified outliers using the Interquartile Range (IQR) and box plot methods.

7. **Outlier Treatment**:
   - Applied log transformation to handle outliers and normalize the data distribution.

8. **Correlation Analysis**:
   - Analyzed feature correlations by plotting a heatmap to understand relationships between variables.

9. **Model Building**:
   - Trained and evaluated several machine learning models:
     - **Decision Trees**
     - **Random Forests** (with and without hyperparameter tuning)
     - **XGBoost** (with and without hyperparameter tuning)
   - Used cross-validation to assess and compare model performance.

10. **Model Evaluation**:
    - Evaluated models using metrics like Mean Squared Error (MSE) and R-squared to assess accuracy.
    - Selected the best-performing model based on test set performance after evaluating both tuned and untuned versions of each model.

This methodology ensures a thorough analysis and comparison of models, providing insights into market trends and accurate predictions for used car prices.

------------------------
## Requirements

- Python 3.x
Install all dependencies using:

```bash
pip install -r requirements.txt
```
--------------------

## Installation 

To set up the project on your local machine, follow these steps:

**Clone the Repository**:

```bash
git clone https://github.com/tasneem-badar/Market-Trend-Analysis-and-Price-Prediction-on-Used-Cars.git
cd Market-Trend-Analysis-and-Price-Prediction-on-Used-Cars
```
---------------------

## Usage

Open and execute the Jupyter Notebook `Market Trend analysis & price prediction on used cars.ipynb` to visualize trends in car prices across different features. This notebook provides insights into price distribution, feature correlations, and market trends for used cars.

------------------------
## Results 

### Model Performance
After training and evaluating multiple machine learning models, the following results were obtained:

- **Decision Tree**: Provided a baseline for understanding how a simple model performs with minimal tuning. However, it had lower accuracy compared to ensemble methods.
- **Random Forest**: Achieved better accuracy and generalization than the Decision Tree. The model with hyperparameter tuning had an R-squared score of 0.86 and a Mean Squared Error (MSE) of 0.03 on the test set.
- **XGBoost**: Outperformed other models with its ability to capture complex relationships. The best-tuned XGBoost model achieved an R-squared score of 0.91 and an MSE of 0.01, making it the most accurate model in this project.

### Comparison of Models

| Model                     | R-squared (Train) | R-squared (Test) | Mean Squared Error (Test) |
|---------------------------|-------------------|-------------------|---------------------------|
| Decision Tree (Tuned)     | 0.89              | 0.74              | 0.05                      |
| Random Forest (No Tuning) | 0.94              | 0.88              | 0.02                      |
| Random Forest (Tuned)     | 0.92              | 0.86              | 0.03                      |
| XGBoost (No Tuning)       | 0.96              | 0.90              | 0.02                      |
| XGBoost (Tuned)           | 0.98              | 0.91              | 0.01                      |


### Insights from Model Evaluation

- **Best Model**: The XGBoost model with hyperparameter tuning was the best-performing model, providing the most accurate predictions on test data.
- **Feature Importance**: The most crucial car price features were make, model, year, mileage, and location, as identified through feature importance analysis.

### Summary
This project successfully demonstrated the potential of machine learning models in predicting used car prices based on various features. The insights gained from trend analysis and the accurate predictions from the model can help stakeholders make informed decisions in the used car market.

---------------------
## Contributions
Contributions are welcome! Please feel free to open issues or submit pull requests for improvements.

----------------------
## License 
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
  
