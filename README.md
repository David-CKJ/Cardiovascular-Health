# Cardiovascular-Health
## About
This is a SC1015 Mini-Project on Cardiovascular Health. In this project, we will analyse the dataset [Cardiovascular Disease](https://www.kaggle.com/datasets/colewelkins/cardiovascular-disease) to assess the reliability of Blood Pressure (BP) as an indicator for Cardiovascular Health. We will do so by finding the correlation between BP and various lifestyle variables, and comparing BP with other health indicators. For a detailed walkthrough, please view the source code in the following order:

1. Data Cleaning
2. Exploratory Data Analysis
3. Data Preprocessing
4. Machine Learning

## Contributors
- ashercw@gmail.com - Data Cleaning
- @David-CKJ - EDA
- Elbertgunawan1@gmail.com - Data Preprocessing and ML

## Problem Definition
- Are we able to predict BP based on various lifestyle variables (active, alcohol, cardio, and smoke) ?
- Will upsampling or downsampling the dataset improve the accuracy of prediction?
- Which model would be best to predict BP?

## Models Used
- Decision Tree
- Random Forest

## Conclusion
EDA
- Negative lifestyle variables (alcohol, cardio, and smoke) have a stronger correlation with BP.
- Positive lifestyle variables (active) do not have a strong correlation with BP.
- Correlation between lifestyle variables and BP is strongest for participants with Stage 2 Hypertension.
- External sources suggest that all lifestyle variables are related to BP, but there is a timeframe associated with their impact.
- Cholesterol and BMI have a stronger correlation with BP. Thus, they might be caused by similar health conditions.
- Relationship between health variables and BP are not linear, either plateauing (cholesterol) or (BMI).

ML
Upsampled vs Downsampled:
- The upsampled model consistently shows better goodness-of-fit and classification accuracy than downsampled one for training and test sets.
- Across the BP classes, Class 1 (Elevated BP) has the largest improvement from the downsampled model to upsampled one.
- For FPR, upsampled and downsampled datasets have similar results which means that upsampled would still be the better for predicting BP.

Decision Tree vs Random Forest:
- Random Forest has better goodness-of-fit and classification accuracy than Decision Tree.
- Random forest is a better as it generates multiples decision trees and this will result in a better goodness-of-fit.
- To further increase prediction accuracy, we implemented hypertuning, which can improve goodness-of-fit of the random forest model.
- Hypertuning focused on optimizing the performance of the random forest by finding the most optimal parameters.

Thus, the upsampled data using the Random Forest model after hyperparameter tuning is the better overall predictor. This is primarily due to better accuracy and more balanced performance across the classes, particularly in handling the minority classes without overly sacrificing performance in other areas.

## Lesson Learnt
Analysing data collection to detect any potential issues; the dataset only looks at cholesterol when there is good cholesterol, measured with the amount of high-density lipoprotein (HDL) and bad cholesterol, measured with the amount of low-density lipoprotein (LDL).

Handling imbalanced datasets by upsampling and downsampling the dataset and taking into cosideration their implications on the datset and prediction model accuracy.

## References
- https://www.kaggle.com/datasets/colewelkins/cardiovascular-disease

## External Sources
- https://pubmed.ncbi.nlm.nih.gov/8728301/
- https://pubmed.ncbi.nlm.nih.gov/20550499/
- https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6316192/
- https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10243231/
- https://my.clevelandclinic.org/health/articles/11918-cholesterol-high-cholesterol-diseases
- https://www.mayoclinic.org/diseases-conditions/high-blood-pressure/in-depth/high-blood-pressure/art-20045206#:~:text=An%20inactive%20%E2%80%94%20also%20called%20sedentary,or%20computer%20may%20be%20helpful
- https://www.mayoclinic.org/diseases-conditions/high-blood-pressure/expert-answers/blood-pressure/faq-20058254
