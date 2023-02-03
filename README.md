# Heart Failure Prediction Data Analysis
## Analyzing a patients chance of developing a heart disease based on a variety of attributes

**Christina Reeder**: 

## Data Source:
https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction

For this dataset, there are 918 rows and 12 columns.

## Data Dictionary
![Attribut Information.png](https://github.com/dcreeder89/Heart-Failure-Prediction-Data-Analysis/blob/main/Attribute%20Information.png)


## Explanatory Data Analysis

### Exploring Chance of Heart Disease Based on Age and Gender
   
![age v heart disease by gender.png](https://github.com/dcreeder89/Heart-Failure-Prediction-Data-Analysis/blob/main/age%20v%20heart%20disease%20by%20gender.png)

There is a significantly higher percent chance for male patients to develop a heart disease than female patients. The percent chance to develop heart disease increases as the age of the male patients increases. However, the chance of heart disease is highest in females in the age range of 60-69 and lowest in females in the age range of 40-49. 

### Explore How Maximum Heart Rate Effects Percent Chance of Heart Disease and Changes with Age

![hr and age v heart disease.png](https://github.com/dcreeder89/Heart-Failure-Prediction-Data-Analysis/blob/main/hr%20and%20age%20v%20heart%20disease.png)

The top plot shows that the chance a patient will develop a heart disease decreases as the maximum heart rate achieved by that patient increases, meaning that the faster the heart is able to beat correlates to how healthy that heart is. The bottom plot shows that the maximum heart rate achieved by a patient decreases with the age of the patient. This leads me to the conclusion that older patients are at a higher risk for heart disease than younger patients on average. 


## Classification Machine Learning

### Machine Learning using the following models:
  - Logistic Regression Classifier
  - K Nearest Neighbor Classifier
  - Random Forest Classifier

We also trained the above models utilizing PCA and Feature Engineering to determine if this would lead to a better performing model. 


### Optimized Models Evaluated and Test Results: 
  - Logistic Regression Classifier: C = 0.1 with L2 Tuning
      - Accuracy: 87.4%
      - Recall: 86.4%

  - K Nearest Neighbor Classifier: n_neighbors = 9
      - Accuracy: 87.0%
      - Recall: 87.1%
      
   - Random Forest Classifier: max_depth = 7 & n_estimators = 69
      - Accuracy: 89.6%
      - Recall: 90.2%


## Final Model Choice
The final model chosen was a Random Forest Classifier Model with max_depth of 7, n_estimators tuned to 69, and utilizing PCA
    - Accuracy: 89.1%
    - Recall: 90.9%


### Data Scientist Observations
Since I prioritize minimizing type 2 errors, the random forest model trained with PCA is better performing than that without PCA. The type 2 errors are the errors in which a patient with heart disease is predicted to not have a heart disease. A patient being given a false negative prognosis will preclude them from receiving treatment they may otherwise need to save their life. 

The random forest model trained without PCA did have one less error overall than the model utilizing PCA. However, it had one more of the type 2 errors, or false negative, errors. 


## Recommendations
It is my recommendation that more datapoints be collected on these patients health history to better train the model for predicting the risk of a patient developing a heart disease. As it is, I do not believe this model is sufficient be utilized to predict anything relating to a patients health or treatment. The number of false positive and false negative predictions made by the model are far to high when someone's life is on the line. I would require an accuracy in a model around 98-99% to even begin considering commercial use. 


### For further information
For any additional questions, please contact dcbailo89@gmail.com
