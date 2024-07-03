# product-recommender

```markdown
# Multi-Label Product Recommendation System

This project implements a multi-label classification model to predict which banking products a customer is likely to use based on their demographic and account information.

## Overview

The system uses a Random Forest Classifier to predict multiple products for each customer. It includes data preprocessing, feature selection, and model training steps to create a robust prediction system.

## Requirements

- Python 3.7+
- pandas
- numpy
- scikit-learn

You can install the required packages using:
```

```shell
pip install pandas numpy scikit-learn
```

```
 Dataset

The model expects a CSV file named 'test.csv' with the following columns:

- Customer features: age, seniority, income, sex, segment, cust_type, residence_index, foreigner_index
- Product columns: Saving Account, Guarantees, Current Accounts, etc. (24 product columns in total)

Usage

1.'test.csv' file is in the same directory as the script.

```

```
3. The script will output:
   - Model performance metrics (F1 scores and Hamming Loss)
   - Recommended products for a sample customer
   - Selected features used by the model

## Customization

- To predict products for a new customer, use the `predict_products` function:


```

```python
new_customer = [age, seniority, income, sex, segment, cust_type, residence_index, foreigner_index]
recommended = predict_products(new_customer)
print("Recommended products:", recommended)
```

- Model  can be adjusted  `features` and `products` lists in the script to match the specific dataset.

## Model Details

- The model uses a Random Forest Classifier as the base estimator.
- Feature selection is performed using VarianceThreshold to remove low-variance features.
- Missing values are imputed using mean strategy.
- The model is trained on 80% of the data and tested on 20%.

## Future Improvements

- Implement cross-validation for more robust performance estimation.
- Explore other multi-label classification techniques like classifier chains or label powerset methods.
- Perform more advanced feature engineering to improve predictive power.
- Experiment with different classification algorithms or ensemble methods.

## 