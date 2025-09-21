# Instacart Customer Reorder Prediction

Predicting customer reorder behavior using machine learning to optimize inventory management and marketing strategies.

## Business Problem
Help Instacart predict which products customers are likely to reorder...

# Data Source

This project uses the Instacart Market Basket Analysis dataset from Kaggle:
https://www.kaggle.com/c/instacart-market-basket-analysis

## Dataset Description
- orders.csv: 3.4M+ customer orders
- products.csv: 49K+ products 
- order_products_train.csv: 1.4M+ training records with reorder labels
- order_products_prior.csv: Customer purchase history

## Setup Instructions
1. Download the dataset from Kaggle
2. Place CSV files in the data/ directory
3. Run the notebook

## Key Results
- **66.5% accuracy** in predicting customer reorder behavior
- **Historical reorder rate** is the strongest predictor (coefficient: 3.36)
- Model achieves 80% recall for identifying customers who will reorder
