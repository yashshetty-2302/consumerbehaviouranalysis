  # E-commerce Customer Behavior Analysis

## Overview
This project analyzes customer behavior patterns in an e-commerce platform to understand factors influencing customer churn. The analysis includes customer interactions across desktop and mobile platforms, transaction patterns, and engagement metrics.

## Dataset Structure

### File: `data1.csv`
Contains customer behavioral data with 3,333 records and 20 features:

| Feature | Type | Description |
|---------|------|-------------|
| account length | Numeric | Duration of customer account |
| location code | Categorical | Customer location identifier (408, 415, 510) |
| user id | Numeric | Unique customer identifier |
| credit card info save | Boolean | If customer saved payment info (yes/no) |
| push status | Boolean | Push notification settings (yes/no) |
| add to wishlist | Numeric | Items in wishlist |
| desktop sessions | Numeric | Number of desktop website visits |
| app sessions | Numeric | Number of mobile app visits |
| desktop transactions | Numeric | Purchases made via desktop |
| total product detail views | Numeric | Product pages viewed |
| session duration | Numeric | Total time spent on platform |
| promotion clicks | Numeric | Interaction with promotions |
| avg order value | Numeric | Average purchase amount |
| sale product views | Numeric | Discounted items viewed |
| discount rate per visited products | Numeric | Average discount percentage |
| product detail view per app session | Numeric | Mobile app engagement metric |
| app transactions | Numeric | Purchases via mobile app |
| add to cart per session | Numeric | Cart additions per visit |
| customer service calls | Numeric | Support interactions |
| churn | Binary | Customer retention status (0=retained, 1=churned) |

## Analysis Notebooks

### `consumer_behaviour.ipynb`
Contains:
- Data preprocessing and cleaning
- Exploratory Data Analysis (EDA)
- Statistical analysis
- Visualization of customer behavior patterns

## Setup and Usage
## Prerequisites
Python 3.x
pandas
numpy
matplotlib
seaborn
Loading the Data
To load and prepare the dataset:
import pandas as pd

# Load the dataset
df = pd.read_csv('data1.csv', sep=';')

# Fix decimal formatting for numeric columns
numeric_columns = ['avg order value', 'discount rate per visited products', 
                  'add to cart per session', 'product detail view per app session']
for col in numeric_columns:
    df[col] = df[col].str.replace(',','.').astype(float)

## Data Characteristics
Delimiter: Semicolon (;)
Decimal Separator: Comma (,)
Missing Values: Represented as 0
Boolean Values: yes/no format
