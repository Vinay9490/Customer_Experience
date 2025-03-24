# Pet Food Retail Analysis

![R](https://img.shields.io/badge/language-R-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## 📌 Overview

This repository contains a comprehensive analysis of pet food retail data to understand customer loyalty patterns, sales trends, and product preferences for Mars pet food products. The analysis is implemented in R Markdown and includes:

- Data cleaning and preparation
- Exploratory data analysis (EDA)
- Visualization of key insights
- Time series forecasting
- Customer loyalty segmentation

## 📂 Repository Structure
PetFood-Analysis/
├── data/ # Contains dataset (not included in repo)
├── scripts/
│ └── Petfood_analysis.Rmd # Main analysis file
├── output/ # Generated visualizations/results
├── README.md # This file
└── .gitignore # Specifies files to ignore

## 🔍 Analysis Highlights

### 1. Data Preparation
- Loaded and cleaned retail transaction data (8,890 observations, 21 variables)
- Handled data types and formats:
  ```r
  petfood$DATE <- as.Date(petfood$DATE, format = "%Y-%m-%d")
  petfood$ZIP_CODE <- as.character(petfood$ZIP_CODE)
  petfood$Sales <- petfood$UNITS * petfood$PRICE
petfood$DISCOUNT <- petfood$BASE_SALES - petfood$TOTAL_SALES
2. Key Insights
🐾 Product Preferences
Wet food (56%) more popular than dry food (44%)

Premium tier accounts for 45% of sales

Cat food outsells dog food (55% vs 45%)

💰 Sales Patterns
Strong positive correlation between price and base price (r = 0.92)

Negative correlation between units sold and base price (r = -0.31)

Highest sales month: July | Lowest sales month: March

🏆 Customer Loyalty
Identified 50 loyal customers (15+ visits)

Loyal customers generate 3x more revenue than others

Loyalty patterns consistent across time periods

🛠️ Installation & Usage
Prerequisites
R (version 4.0+ recommended)

RStudio (recommended)

Required packages:
install.packages(c("ggplot2", "dplyr", "forecast", "knitr"))
Running the Analysis
Clone the repository:
git clone https://github.com/yourusername/PetFood-Analysis.git
Place your dataset in the data/ folder

Open Petfood_analysis.Rmd in RStudio

Update the data path if needed

Click "Knit" to run the full analysis

📊 Sample Visualizations
Food Type Distribution
Fig 1: Wet food dominates purchases

Price by Lifestage
Fig 2: Puppy food commands premium pricing

📈 Forecasting
Implemented ARIMA model for sales prediction:
arima_model <- auto.arima(ts_data)
forecast_values <- forecast(arima_model, h = 24)
plot(forecast_values)
🤝 Contributing
Contributions are welcome! Please:

Fork the repository

Create your feature branch

Commit your changes

Push to the branch

Open a pull request
