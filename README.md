# Instacart Customer Reorder Prediction

Predicting customer reorder behavior using machine learning to optimize inventory management and marketing strategies.

## Business Problem

Help Instacart predict which products customers are likely to reorder based on their shopping history and behavior patterns. This enables data-driven decisions for inventory stocking, targeted marketing campaigns, and personalized customer experiences.

## Dataset

This project uses the Instacart Market Basket Analysis dataset from Kaggle:
https://www.kaggle.com/c/instacart-market-basket-analysis

### Data Structure
- **orders.csv**: 3.4M+ customer orders with timing and sequence data
- **products.csv**: 49K+ products with category information
- **order_products_train.csv**: 1.4M+ training records with reorder labels
- **order_products_prior.csv**: Customer purchase history for feature engineering

## Technical Approach

### Feature Engineering
Created customer behavior features from transactional data:
- `total_orders`: Customer loyalty indicator
- `unique_products`: Shopping diversity measure  
- `historical_reorder_rate`: Past reordering tendency
- `avg_days_between_orders`: Shopping frequency
- `avg_cart_position`: Item placement in cart
- `preferred_day` & `avg_order_hour`: Shopping timing patterns

### Models Implemented
1. **Logistic Regression**: Baseline model for interpretability
2. **Random Forest**: Advanced model for capturing non-linear patterns

### Evaluation Metrics
- Accuracy, Precision, Recall, F1-Score
- Feature importance analysis
- Business impact interpretation

## Key Results

### Model Performance
- **Logistic Regression**: 66.5% accuracy
- **Random Forest**: 66.9% accuracy  
- **Best F1-Score**: 0.75 (balanced precision/recall)
- **Recall**: 82% (catches most reorder opportunities)

### Feature Importance Insights
1. **Historical reorder rate** (56% importance): Strongest predictor - past behavior drives future reordering
2. **Total orders** (20% importance): Customer experience level matters significantly  
3. **Product diversity** (11% importance): Shopping variety affects loyalty patterns

### Key Business Finding
Modest algorithmic improvements suggest we've reached a **feature ceiling** rather than algorithm limitation - need richer data sources for further gains.

## Business Impact

This model enables Instacart to:

### Inventory Management
- **Stock optimization**: Increase inventory 20-30% for high-probability reorder products
- **Warehouse efficiency**: Prioritize high-reorder items in picker locations
- **Waste reduction**: Decrease stock levels for low-reorder probability items

### Customer Targeting  
- **Retention campaigns**: Target customers with declining reorder probability
- **Personalization**: Customize recommendations based on reorder likelihood
- **Subscription services**: Offer auto-delivery for high-reorder products

### Strategic Insights
- **Focus on first-time buyer conversion**: Once customers reorder once, they become loyal
- **Cart position optimization**: Items added later show higher reorder rates
- **Customer lifecycle management**: Different strategies for different experience levels

## Actionable Recommendations

1. **Immediate**: Implement reorder-based inventory stocking rules
2. **Short-term**: Design targeted campaigns for low-reorder probability customers  
3. **Long-term**: Collect product-level features (price, seasonality, substitution patterns)
4. **Validation**: A/B testing framework to measure model impact on business metrics

## Next Steps

- **Enhanced features**: Product characteristics, price sensitivity, seasonal patterns
- **Advanced models**: XGBoost, ensemble methods for marginal improvements
- **A/B testing**: Experimental framework for model deployment validation
- **Real-time deployment**: Production pipeline for live recommendations

## Setup Instructions

1. Download the Instacart dataset from Kaggle
2. Install requirements: `pip install -r requirements.txt`
3. Place CSV files in the `data/` directory
4. Run the Jupyter notebook: `notebooks/customer_reorder_prediction.ipynb`

## Technical Stack

- **Python 3.8+**
- **pandas**: Data manipulation and analysis
- **scikit-learn**: Machine learning models and evaluation
- **matplotlib/seaborn**: Data visualization
- **numpy**: Numerical computations

## Contact

[Your Name] - [Your LinkedIn] - [Your Email]

*This project demonstrates end-to-end data science workflow from business problem identification to actionable recommendations.*