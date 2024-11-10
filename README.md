# Market-Trend-Analysis-and-Price-Prediction-on-Used-Cars

This project aims to analyze market trends in the used car market and develop a predictive model for estimating car prices based on various features. By understanding factors affecting prices, this analysis can assist car buyers, sellers, and dealers in making informed decisions.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Data Collection](#data-collection)
3. [Features](#features)
4. [Methodology](#methodology)
5. [Requirements](#requirements)
6. [Installation](#installation)
7. [Usage](#usage)
8. [Results](#results)
9. [Future Work](#future-work)
10. [Contributing](#contributing)
11. [License](#license)

## Project Overview

The used car market is complex and influenced by factors such as make, model, age, mileage, condition, and location. This project provides:
- **Market Trend Analysis**: Insight into price patterns across car makes, models, and locations.
- **Price Prediction**: A machine learning model to predict car prices based on selected features, providing a helpful tool for stakeholders.
## Data Collection

The data for this project was obtained through web scraping. Details of the data collection process are as follows:

### 1. Web Scraping
- **Source**: Data was scraped from the [Cars24 website](https://www.cars24.com/), which provides detailed listings of used cars available for sale across various cities.
- **Libraries Used**: The scraping was done using **BeautifulSoup** and **Selenium** to extract relevant details, including make, model, year, mileage, condition, location, and price.
- **Coverage**: Information on used cars was scraped from listings across **11 different cities**, providing a broad view of regional market trends and pricing.

This scraped dataset is the basis for analyzing market trends and building machine-learning models for price prediction.

## FEatures

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
  
