# Bird Strike Analysis and Prediction using Machine Learning

## Project Overview
This project applies machine learning techniques to analyze historical bird strike data in aviation and develop predictive models to enhance flight safety and reduce operational costs.

## Problem Statement
Bird strikes pose significant safety and financial challenges to the aviation industry:
- Direct aircraft damage and maintenance costs
- Flight delays and cancellations
- Safety risks to passengers and crew

## Objectives
1. **Predictive Analysis**: Predict the likelihood of bird strike incidents
2. **Cost Analysis**: Analyze and predict financial impact of bird strikes
3. **Risk Mitigation**: Provide actionable insights for aviation stakeholders

## Dataset
- **Source**: FAA Bird Strikes Database
- **Records**: 25,429 bird strike incidents
- **Features**: 26 attributes (altitude, wildlife species, aircraft type, flight phase, cost, damage, etc.)

## Use Cases

### Use Case 1: Bird Strike Prediction
- **Target Variable**: Binary classification (Bird Strike occurred / No strike)
- **Models Used**: Logistic Regression, Decision Tree
- **Best Performance**: Decision Tree (93% Accuracy, 93% F1-Score)
- **Key Predictors**: Altitude, Flight Phase, Wildlife Size, Number Struck

### Use Case 2: Cost Analysis
- **Target Variable**: Regression (Financial cost in dollars)
- **Models Used**: AdaBoost, Random Forest
- **Best Performance**: AdaBoost (93.35% Accuracy, 96% F1-Score, 99% Recall)
- **Key Cost Drivers**: Wildlife Size, Altitude, Flight Phase, Effect Type

## Methodology

### Data Preprocessing
- Missing value imputation (median for numerical, "Unknown" for categorical)
- One-hot encoding and ordinal encoding for categorical features
- Log transformation for skewed features
- SMOTE for handling class imbalance

### Exploratory Data Analysis
- Distribution analysis of altitude, flight phases, wildlife species
- Correlation heatmaps to identify feature relationships
- Box plots and visualizations of high-cost incidents
- Time-series analysis by flight date

### Model Development
1. Train-test split (80-20 ratio, stratified sampling)
2. Multiple algorithm comparison
3. Hyperparameter tuning and cross-validation
4. ROC curves and confusion matrix analysis

## Key Findings

### Predictive Analysis Insights
- Approach and Landing phases are highest risk
- Medium altitude (100-700 ft) shows highest incident frequency
- Large wildlife and "Over 100" bird counts correlate with damage
- Engine shutdown is the most costly effect type

### Cost Analysis Insights
- High-cost incidents predominantly involve large wildlife
- Medium altitudes generate 2.5x higher costs than low altitudes
- Certain aircraft types (B-737, A-320) appear in more costly incidents
- AdaBoost identified 99% of high-cost incidents (excellent recall)

## Technologies Used
- **Languages**: Python 3
- **ML Libraries**: scikit-learn, pandas, numpy
- **Data Visualization**: matplotlib, seaborn
- **Environment**: Google Colab
- **Techniques**: Classification, Regression, Ensemble Methods, SMOTE

## Results Summary
| Metric | Logistic Regression (Prediction) | Decision Tree (Prediction) | AdaBoost (Cost) | Random Forest (Cost) |
|--------|----------------------------------|---------------------------|-----------------|---------------------|
| Accuracy | 93% | 93% | 93.35% | 92.67% |
| Precision | 92% | 93% | 94% | 94% |
| Recall | 93% | 93% | 99% | 98% |
| F1-Score | 91% | 92% | 96% | 96% |
| AUC-ROC | 0.82 | 0.84 | 0.95 | 0.94 |

## Impact & Applications
- **Airlines**: Optimize flight scheduling and maintenance planning
- **Airport Authorities**: Target wildlife management resources
- **Regulatory Bodies**: Support evidence-based safety policies
- **Insurance**: Better risk assessment and premium calculation

## Future Scope
- Integrate real-time weather data and flight trajectory
- Expand to international airports for global validation
- Develop deployment API for live risk scoring
- Detailed cost segmentation analysis (repairs, delays, fuel)
- Cross-validation across multiple regions and operators

## Course Information
- **Course**: CIS-508 (Machine Learning in Business)
- **Academic Year**: 2024-2025
- **Institution**: Arizona State University 
