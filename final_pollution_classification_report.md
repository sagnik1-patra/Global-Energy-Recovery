
# Global Pollution Severity Classification Report

## Objective

The goal of this project is to classify countries into different pollution severity categories:

- Low
- Medium
- High

The classification is based on pollution levels, energy consumption, industrial waste, CO2 emissions, and other environmental indicators.

## Dataset

Input Dataset:

C:\Users\NXTWAVE\Downloads\Global Energy Recovery\Global_Pollution_Analysis.csv

Output Directory:

C:\Users\NXTWAVE\Downloads\Global Energy Recovery

Total Records After Cleaning:

200

Total Features Used:

16

## Data Preprocessing

The dataset was cleaned using the following steps:

- Duplicate records were removed.
- Missing numerical values were handled using median imputation.
- Missing categorical values were handled using most frequent value imputation.
- Outliers were handled using the IQR capping method.
- Categorical features such as country and year were encoded using LabelEncoder.
- Numerical features were scaled using StandardScaler.
- MinMaxScaler was used separately for Multinomial Naive Bayes because it requires non-negative input values.

## Feature Engineering

The following engineered features were created:

### Energy Consumption Per Capita

This feature was created to understand energy usage relative to population.

### Overall Pollution Index

This feature was created by combining pollution-related indicators such as:

['Air_Pollution_Index', 'Water_Pollution_Index', 'Soil_Pollution_Index', 'Industrial_Waste (in tons)', 'CO2_Emissions (in MT)', 'Plastic_Waste_Produced (in tons)']

### Yearly Pollution Trend

This feature was created to observe yearly changes in pollution levels.

## Target Variable

The target variable `Pollution_Severity` was created using the `Overall_Pollution_Index`.

Thresholds used:

- Low Pollution Threshold: 9808.5091
- High Pollution Threshold: 15559.571233333332

Classification rule:

- Low: pollution index less than or equal to low threshold
- Medium: pollution index between low and high threshold
- High: pollution index greater than high threshold

## Models Used

Three classification algorithms were trained and evaluated:

1. Multinomial Naive Bayes
2. K-Nearest Neighbors
3. Decision Tree Classifier

## Model Performance

                  Model  Accuracy  Precision  Recall  F1_Score
Multinomial Naive Bayes     0.725   0.712857   0.725  0.714380
                    KNN     0.675   0.711111   0.675  0.678312
          Decision Tree     0.950   0.951786   0.950  0.950000

## Best Model

The best model based on weighted F1-score is:

Decision Tree

## KNN Best Parameters

{'metric': 'manhattan', 'n_neighbors': 11, 'weights': 'uniform'}

## Decision Tree Best Parameters

{'criterion': 'gini', 'max_depth': 2, 'min_samples_leaf': 1, 'min_samples_split': 2}

## Key Insights

### Pollution Severity

Countries or records with higher pollution index values were classified as High severity, while lower values were classified as Low severity.

### Energy Consumption

Energy consumption per capita helps understand how energy use may be connected with pollution severity.

### Pollution Trend

Yearly pollution trend helps identify whether environmental conditions are improving or worsening over time.

### Decision Tree Interpretability

Decision Tree provides feature importance, making it useful for understanding which environmental factors contribute most to pollution severity.

## Policy Recommendations

1. High pollution severity countries should adopt stricter emission control policies.
2. Industrial waste treatment should be strengthened.
3. Renewable energy adoption should be encouraged.
4. Energy recovery systems should be implemented to convert waste into usable energy.
5. Countries with rising yearly pollution trends should be monitored closely.
6. Air, water, and soil pollution indices should be tracked regularly.
7. Public transport and clean fuel policies should be promoted.
8. Pollution dashboards should be used for real-time decision-making.

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

The recommended model is Decision Tree, as it achieved the best weighted F1-score.

If interpretability is the priority, the Decision Tree classifier is preferred because it explains which features are responsible for pollution severity classification.
