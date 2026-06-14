
# Global Pollution Severity Classification Report

## Objective

The goal of this project is to classify countries into different pollution severity categories:

- Low
- Medium
- High

The classification is based on pollution levels, energy consumption, industrial waste, CO2 emissions, and other environmental indicators.

## Dataset

Input Dataset:

C:\Users\NXTWAVE\Downloads\Global Energy Recovery\Food_Delivery_Time_Prediction.csv

Total Records:

200

Total Features Used:

18

## Target Variable

The target variable `Pollution_Severity` was created using the `Overall_Pollution_Index`.

Thresholds used:

- Low Pollution Threshold: 0.0
- High Pollution Threshold: 0.0

## Models Used

Three classification algorithms were used:

1. Multinomial Naive Bayes
2. K-Nearest Neighbors
3. Decision Tree Classifier

## Model Performance

                  Model  Accuracy  Precision  Recall  F1_Score
Multinomial Naive Bayes       1.0        1.0     1.0       1.0
                    KNN       1.0        1.0     1.0       1.0
          Decision Tree       1.0        1.0     1.0       1.0

## Best Model

The best model based on weighted F1-score is:

Multinomial Naive Bayes

## Key Insights

### Pollution Classification

Countries or records with higher pollution index values were classified as High severity, while lower values were classified as Low severity.

### Energy Consumption Per Capita

Energy consumption per capita was engineered to understand how energy usage relates to pollution severity.

### Yearly Pollution Trend

Yearly pollution trend was created to observe whether pollution indicators are increasing or decreasing over time.

### Decision Tree Insights

The Decision Tree model provides feature importance, helping identify which environmental factors contribute most to pollution severity.

## Policy Recommendations

1. Countries with High pollution severity should focus on stricter emission control policies.
2. Industrial waste management systems should be improved.
3. Renewable energy adoption should be encouraged.
4. Energy recovery systems should be promoted to reduce waste and improve sustainability.
5. Countries with rising yearly pollution trends should be monitored continuously.
6. Public transportation and clean fuel policies can help reduce CO2 emissions.
7. Pollution monitoring dashboards should be implemented for real-time environmental tracking.

## Generated Files

- preprocessed_global_pollution_data.csv
- model_comparison_results.csv
- pollution_severity_predictions.csv
- decision_tree_feature_importance.csv
- model_performance_comparison.png
- decision_tree_feature_importance.png
- decision_tree_visualization.png
- Multinomial_Naive_Bayes_confusion_matrix.png
- KNN_confusion_matrix.png
- Decision_Tree_confusion_matrix.png
- multinomial_naive_bayes_model.pkl
- knn_model.pkl
- decision_tree_model.pkl
- standard_scaler.pkl
- minmax_scaler.pkl
- label_encoders.pkl
- target_encoder.pkl
- result_summary.json

## Final Recommendation

The recommended model is Multinomial Naive Bayes, as it achieved the best weighted F1-score.

If interpretability is important, the Decision Tree classifier is preferred because it shows which features are most responsible for pollution severity classification.
