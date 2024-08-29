# Cryptocurrency Clustering Project

## Overview
This project applies clustering techniques to cryptocurrency market data to group similar cryptocurrencies based on their price changes over various time periods. The goal is to explore the structure of the cryptocurrency market and identify clusters of similar cryptocurrencies using Principal Component Analysis (PCA) and K-Means clustering.

## Data
The dataset used in this project contains the following features for each cryptocurrency:

- `price_change_percentage_24h`: Percentage change in price over the last 24 hours
- `price_change_percentage_7d`: Percentage change in price over the last 7 days
- `price_change_percentage_14d`: Percentage change in price over the last 14 days
- `price_change_percentage_30d`: Percentage change in price over the last 30 days
- `price_change_percentage_60d`: Percentage change in price over the last 60 days
- `price_change_percentage_200d`: Percentage change in price over the last 200 days
- `price_change_percentage_1y`: Percentage change in price over the last year

## Methodology
1. **Data Preprocessing**: The data is normalized using `StandardScaler` to ensure that all features contribute equally to the analysis.

2. **Principal Component Analysis (PCA)**:
   - PCA is used to reduce the dimensionality of the data while retaining most of the variance.
   - The dataset is reduced to three principal components for easier visualization and clustering.

3. **K-Means Clustering**:
   - The optimal number of clusters is determined using the Elbow method, which plots the inertia (within-cluster sum of squares) for different values of \( k \).
   - K-Means is then applied to the PCA-transformed data to group the cryptocurrencies into clusters.

4. **Visualization**:
   - A scatter plot is created using the first two principal components to visualize the clusters.
   - The features contributing most to each principal component are identified by examining the PCA loadings.

## Usage
To run this analysis:

1. **Install Required Libraries**: Ensure that you have the necessary Python libraries installed. You can install the required packages using:
   ```bash
   pip install pandas scikit-learn matplotlib hvplot
