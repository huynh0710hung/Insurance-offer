AAI Data Scientist Challenge - BANCA Insurance Policy Prediction

1. Introduction

This report details the process of building a predictive model to identify customers likely to purchase BANCA's MANU healthcare insurance policy. The project involves data preprocessing, exploratory data analysis, model training, evaluation, and prediction on a test dataset.

2. Data Understanding and Preparation

Datasets:

train_data.txt: 5822 customer records with 85 features (columns 1-85) and a target variable (column 86).

test_data.txt: 4000 customer records with the same 85 features as the training set, but without the target variable.

attributes_description.pdf: Provides descriptions of each feature.

Data Cleaning: No missing values were found.

Feature Engineering: Categorical features (Customer Subtype, Average Age, Customer Main Type) were converted to numerical representations using Label Encoding.

Data Splitting: The training data was split into training (80%) and validation (20%) sets to evaluate model performance before applying it to the test set.

3. Exploratory Data Analysis (EDA)

EDA was performed to understand the data and identify potential patterns:

Univariate Analysis: Histograms and descriptive statistics were used to examine the distribution of individual features.

Bivariate Analysis: Correlations and visualizations were used to explore relationships between features and the target variable.

Key Findings: Certain customer subtypes, income levels, and product ownership patterns showed a stronger correlation with the likelihood of purchasing the MANU policy.

4. Model Selection and Training

Model: A Random Forest Classifier was chosen for its ability to handle various data types and capture complex relationships.

Training: The model was trained using the training dataset.

5. Model Evaluation

The model's performance was evaluated on the validation set using the following metrics:

Validation Accuracy: ~93-94% (Indicates the overall correctness of the model's predictions)

AUC Score: ~0.73-0.75 (Measures the model's ability to distinguish between the two classes)

Precision (Class 1): ~60-65% (Out of all customers predicted to buy, how many actually bought?)

Recall (Class 1): ~10-12% (Out of all customers who actually bought, how many did the model correctly identify?)

F1-score (Class 1): ~18-20% (Harmonic mean of precision and recall, a balanced measure)

6. Feature Importance

The Random Forest model provided feature importance scores, highlighting the most influential variables in the prediction.

Top Features: Customer Subtype, Average income, Purchasing Power Class, and some product ownership attributes were among the most important.

Visualization: A bar chart of the top 15 features is included in the notebook to visually represent their importance.

7. Prediction and Output

The trained model predicted the probability of each customer in the test_data.txt buying the policy.

Customers were ranked based on these probabilities.

The IDs of the top 800 customers (most likely to buy) were saved to predicted_top_800.csv.

8. Model Monitoring and Reliability

Cross-validation: Could be implemented during training for a more robust evaluation of model generalization.

Feature Importance Monitoring: Regularly checking feature importance helps detect changes in data patterns over time.

Calibration Curves: These can be used to assess how well the predicted probabilities align with actual probabilities.

A/B Testing: Deploying the model in a real-world setting and comparing predictions with actual outcomes is crucial for ongoing monitoring and improvement.

9. Explanation and Insights

Customer Segmentation: The model suggests that certain customer segments are more likely to purchase the MANU policy. Targeting these segments with tailored marketing campaigns could be beneficial.

Key Factors: Income, purchasing power, and specific customer subtypes are strong indicators of purchase likelihood.

10. Recommendations

Targeted Marketing: Focus sales efforts on high-probability customer segments.

Personalized Messaging: Tailor marketing communications based on customer characteristics.

Further Analysis: Explore interactions between features for deeper insights into customer behavior.

Model Refinement: Consider other models, feature engineering, and hyperparameter tuning to potentially improve prediction accuracy.

11. Conclusion

The Random Forest model demonstrates potential for predicting customer purchase behavior for the MANU policy. The insights gained from this analysis can be used to improve sales strategies and target marketing efforts. Continuous monitoring and refinement of the model are essential to maintain its effectiveness over time.
