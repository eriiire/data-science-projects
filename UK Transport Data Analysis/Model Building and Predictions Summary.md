# UK Transport Dataset - Predictive Modeling Project

## Business Objective and Context

Our consultancy service focuses on analyzing past accident and casualty data to identify vehicular accident hotspots in a city. The goal is to:
- Pinpoint danger zones based on historical data
- Suggest preventative measures to reduce accidents and casualties in high-risk areas
- Aid city authorities in minimizing property damage and enhancing public safety

By analyzing patterns in accident data, we can inform decision-making for deploying resources and implementing policies in the most accident-prone areas.

# Data Loading and Cleaning

Four datasets were prepared as follows:

- **x_train, x_test**: Independent variables for training and testing
- **y_train, y_test**: Dependent variable, `accident_severity`

The data was cleaned to:

- Drop unnecessary columns
- Standardize numerical values
- Encode categorical variables using one-hot encoding

# Addressing Class Imbalance

Due to the class imbalance in `accident_severity`:

- **Oversampling** was done using SMOTE to increase minority class instances
- **Undersampling** was used to reduce the majority class for comparison

# Model Building and Evaluation

## Model Selection and Training

Various models were trained, including:

- Logistic Regression (Baseline)
- Decision Trees
- Random Forest
- Bagging
- Gradient Boosting
- AdaBoost
- XGBoost

Each model’s performance was evaluated using accuracy, recall, precision, and F1 score. Cross-validation helped mitigate overfitting, and confusion matrices highlighted misclassification areas, especially for rare fatal cases.

## Hyperparameter Tuning

Grid and randomized searches were employed to optimize hyperparameters, with significant improvement achieved through:

- **Random Forest and XGBoost** (best performers after tuning)

Fine-tuning reduced overfitting in XGBoost while retaining good test set performance.

# Final Model Performance

After evaluation, the final model was the XGBoost classifier with oversampled data, tuned through randomized grid search. The model achieved:

- **Test Accuracy**: 79.9%
- **Precision**: 75.3%
- **Recall**: 79.7%
- **F1 Score**: 76.6%

### Training and Validation Comparison:

| Model                        | Accuracy | Recall | Precision | F1 Score |
|------------------------------|----------|--------|-----------|----------|
| XGBoost Grid Search OverSampled | 0.924    | 0.924  | 0.928     | 0.920    |
| XGBoost Best Features        | 0.883    | 0.883  | 0.888     | 0.874    |
| XGBoost Randomized Grid Search | 0.877    | 0.877  | 0.881     | 0.866    |

# Insights and Recommendations

## Key Findings

The most significant features correlated with accident severity include:

- **Did Police Officer Attend Scene**: Correlates with accident severity
- **Number of Vehicles**: Indicates higher accident likelihood
- **Vehicle Manoeuvre and Light Conditions**: Contribute to accident risk

### Identifying Hazardous Zones

The 20 most accident-prone zones were identified by their latitude and longitude coordinates, which can guide resource allocation.

## Recommendations

For high-risk zones:

- Increase police presence to manage traffic and prevent risky maneuvers.
- Implement time-based driving regulations in high-risk areas.
- Penalize dangerous vehicle maneuvers heavily to discourage reckless driving.
- Reduce vehicle density through improved public transportation and road usage policies.

# Conclusion and Future Improvements

## Key Takeaways

- XGBoost emerged as the best model, performing well across training, validation, and test sets.
- Overfitting was observed but managed through feature selection and hyperparameter tuning.
- Model reliability is moderate, with reasonable accuracy and precision, though improvements are possible.

## Future Improvements

- **Increase Dataset Size**: More data can improve predictions, especially for fatal accidents.
- **Feature Engineering**: New features might improve model correlation with accident severity.
- **Try Additional Algorithms**: More algorithms may enhance model accuracy.
- **Advanced Hyperparameter Tuning**: Extend the grid search to cover a broader parameter space.

## Real-World Implementation Challenges

- **Integration with Existing Systems**: Emergency services may need support for real-time data flow.
- **Legal and Liability Issues**: Predictive models used in public safety raise legal considerations.
- **Data Quality**: The model’s accuracy depends on consistent, unbiased data collection.

