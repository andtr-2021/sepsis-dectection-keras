
### Project Information:
* **Project Name**: Sepsis Detection
* **Libraries Used**: pandas, numpy, matplotlib, seaborn, sklearn, imblearn

### Project Summary and Model Evaluation

**Summary**: There are several major problems in the dataset. 

* **Small dataset**: the number of data points in the dataset is only a few hundred even though I used some oversampling technique, which can easily lead to overfitting so that I have to choose a simple algorithm with regularization because I can't do too much feature engineering or sample more data.

* **Imbalanced dataset**: the number of each class in the dataset is imbalanced so that I have to deal with it using SMOTE Oversampling technique. The reason I used this method is that it will not copy and repeat data point like the Random Oversampling technique but creating data points in a synthetic and systematical way. Which will vastly decrease the chance of overfitting. 

**Metrics**:
* Prevent overfitting.
* High recall score.
* Simple or ensemble algorithms.
* Regularization (L2)

Thus based on our evaluation metric, the scores of the models we tried are as below:

| Models      | Recall Score | F1-score| ROC AUC (%) | Precision |
|-------------|--------------------------|----------------------|-----|----|
| **1. Regularized Logistic Regression with Hyperparameter Tuning and SMOTE Oversampling** | 74, 78 | 77, 75 | 75.9 | 79, 72 |
| **2. Decision Tree with Hyperparameter Tuning and SMOTE Oversampling** | 73, 82 | 77, 77 | 77.4 | 82, 72 |
| **3. Bagging Decision Tree with Hyperparameter Tuning and SMOTE Oversampling** | 82, 89 | 86, 85 | 85.5 | 90, 81 |
| **4. Random Forest with Hyperparameter Tuning and SMOTE Oversampling** | 77, 89 | 83, 82 | 83.2 | 89, 77 |

Note: The first number is for class 0 and the second number (behind the comma) is for class 1. 

According to all the metrics and score, it can be seen that **Model 3** gives a better measures overall against others. 
