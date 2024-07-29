### Predicting Breast Cancer Recurrence using Machine Learning

**Aaron Leung**

#### Executive summary
#### Rationale
Breast cancer is one of the most common cancers among women, making it essential to understand the factors that contribute to its recurrence to improve patient prognosis and survival rate. By integrating predictive models into clinical practice, healthcare providers can provide effective, targeted intervention for high-risk patients.

#### Research Question
This analysis seeks to accomplish two main goals. First, it explores how predictive models can be used to accurately predict the recurrence of breast cancer based on attributes such as patient demographics and clinical features. Second, it seeks is to identify which factors are most important for predicting recurrence.

#### Data Sources
The dataset used in this analysis is sourced from UCI Machine Learning Repository and originally comes from University Medical Centre, Institute of Oncology, Ljubljana, Yugoslavia. Please see the following link for more information: https://archive.ics.uci.edu/dataset/14/breast+cancer. It includes the target variable ('Class') indicating recurrence/ no recurrence, along with nine attributes related to patient demographics, clinical features and treatment. To provide a clearer understanding of these features, we will briefly describe each one below:

1. Class: Indicates whether the patient experienced recurrence events of breast cancer
2. Age: Indicates the age of the patient
3. Menopause: Indiates the menopausal stage of the patient (premenopausal vs postmenopausal)
4. Tumor size: Indicates the size of the tumor in millimeters
5. Inv-nodes: Refers to the number of positive lymph nodes that contain cancer
6. Node-caps: Refer to the presence of extracapsular extension which means that cancer cells have spread beyond the capusle of the lymph node into surrounding tissue
7. Degree-malig: Indicates how aggressive the cancerous tumor is
8. Breast: Refers to the side (left or right) where cancer has occurred
9. Breast-quad: Identifys the specific quadrant of the breast where tumor is located
10. Irradiat: Indicates whether patient has received radiation therapy

#### Methodology
Methods used comprise of the following:

_Data Exploration_
1. Overview of the Dataset
2. Check for Missing Values
3. Univariate analysis: Visualize and analyze distribution of each feature

_Data Preprocessing_
1. Data Cleaning
2. Data Transformation and Encoding followed by Bivariate Analysis (examining relationship between each feature and the target variable)
3. Feature Scaling

_Exploration of Different Classifcation Models_
1. Logistic Regression
2. Decision Tree
3. K-Nearest Neighbors
4. Support Vector Machines

_Model Evaluation and Hyperparameter Tuning_
1. Access performance of models using metrics such as accuracy, precision, recall, f1-score
2. Perform hyperparameter tuning with GridSearchCV

#### Results
1. _Small Dataset Size_: The dataset contains only 286 samples which can significantly impact each model's ability to generalize well to unseen data. This limited size often leads to overfiting which we observed in the four models that were trained.

2. _Lack of significant improvement when using GridSearchCV_: Hyperparameter tuning with GridSearchCV did not yield substantial improvements in our model's performance. This is likely due to the model's inability to effectively learn from the small dataset. Among the models, KNeighbors and Support Vector Machines showed the most improvement in terms of recall on the test set.

3. _Feature importance_: Despite the models' suboptimal performance, we were still able to gain insights into which features are important for predicting recurrence. In Logistic Regression model, receiving irradiation, high lymph node involvement and a higher degree of malignancy were strong positive predictors. In the Decision Tree model, key predictors included degree of malignancy and tumor location. Similar to logistic regression, other important predicts iclude receiving irradiation and high lymph node involvement. Patients with above-mentioned high risk features should be more closely monitored to detect recurrence early.

#### Next steps
One of the biggest issues we encountered was that the models were unable to effectively learn from the small dataset. Therefore, I consider this a pilot study, as multiple improvements can be made. The following list are future considersations to take into account.
1. Find a larger dataset to enable models to learn more effectively and generalize well to unseen data.
  
2. Revisit hyperparameter tuning and data preprocessing steps to enhance cross-validation score and performance metrics.
  
3. Incorporate genetic factors, such as genetic mutations and family history, as these can significantly increase risk of breast cancer.

#### Link to notebook

- [Final Report Notebook](https://github.com/ahleung2/Prediction-of-Breast-Cancer-Recurrence/blob/main/Leung_Aaron%20Prediction%20of%20Breast%20Cancer%20Recurrence.ipynb)



##### Contact and Further Information
