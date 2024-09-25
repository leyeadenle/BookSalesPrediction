# Model Card: Book Sales Prediction Model

## Model Description

- **Model Name**: Book Sales Prediction Model  
- **Version**: 1.0  
- **Date**: September 22, 2024  

### **Input**  
The model takes the following features as inputs:
- **Numerical features**: Publishing year, author rating, average book rating, book ratings count, gross sales, publisher revenue, sale price, sales rank.
- **Categorical features**: Book name, author name, language code, genre.

### **Output**  
The model predicts the number of units sold for each book (the target variable). This is an integer representing the number of copies sold.

### **Model Architecture**  
This is a regression model designed to predict book sales using several algorithms:
- **Algorithms Used**: 
  - Linear Regression
  - Random Forest Regressor
  - XGBoost Regressor
  - Support Vector Regressor (SVR)
  
  The Random Forest model was identified as the best-performing architecture, after comparing it with the other algorithms based on performance metrics like RMSE and \(R^2\).

### **Model Training**
The model was trained using an 80/20 train-test split on a dataset containing book sales data. Bayesian Optimization was used to tune hyperparameters for the Random Forest, XGBoost, and SVR models.

## Performance

The models were evaluated on the test set using **Root Mean Squared Error (RMSE)** and **\(R^2\) score**. Here are the key results:

- **Linear Regression**: RMSE = [Linear Regression RMSE], \(R^2\) = [Linear Regression R²]
- **Random Forest**: RMSE = **1011.02**, \(R^2\) = **0.9958**
- **XGBoost**: RMSE = [XGBoost RMSE], \(R^2\) = [XGBoost R²]
- **Support Vector Regressor**: RMSE = [SVM RMSE], \(R^2\) = [SVM R²]

The **Random Forest Regressor** model achieved the best performance with the lowest RMSE and the highest \(R^2\) score, indicating high predictive accuracy on the test set.

### Summary Metrics
- **RMSE**: Root Mean Squared Error
- **\(R^2\)**: Coefficient of Determination

## Limitations

- **Data Representation**: The model assumes that the dataset is representative of the book sales market, which may not generalise well to other markets or regions.
- **Feature Simplification**: Categorical features like "Book Name" and "Author" are simplified using one-hot encoding, which may not capture deeper relationships.
- **Imputation Impact**: Missing data was imputed with the median for numeric features and 'Unknown' for categorical features, which could affect prediction accuracy in cases where imputed values are not representative of the actual data.

## Trade-offs

- **Bias**: The model may reflect biases present in the data, favouring established authors or popular genres. This could result in under-predicting sales for newer or niche authors.
- **Transparency**: Some of the algorithms used (e.g., Random Forest, XGBoost) are complex and may not offer interpretability without additional tools like SHAP or LIME.
- **Fairness**: The model may perform differently based on genre, publisher, or author due to underlying data biases, potentially reinforcing existing inequalities in the publishing industry.
