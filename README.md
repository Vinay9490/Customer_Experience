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

## 🔍 Analysis Highlights

### 1. Data Preparation
- Loaded and cleaned retail transaction data (8,890 observations, 21 variables)
- Handled data types and formats:
  ```r
  petfood$DATE <- as.Date(petfood$DATE, format = "%Y-%m-%d")
  petfood$ZIP_CODE <- as.character(petfood$ZIP_CODE)
