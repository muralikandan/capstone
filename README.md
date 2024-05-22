### Fraud Detection Model for Loan Applications

**Murali Kandan**

#### Abstract
The development of a fraud detection model for auto loan applications is essential for mitigating financial risks and safeguarding lenders' assets. This project aims to construct a robust and accurate predictive model capable of identifying potentially fraudulent auto loan applications. The methodology encompasses several key components, including data collection, preprocessing, feature engineering, model development, evaluation, and interpretation.

To establish a performance benchmark, a baseline model using a Dummy Classifier created. This simplistic model sets the minimum level of predictive accuracy necessary for more complex models to surpass. Subsequently, a simple logistic regression model is trained to provide insights into the relationship between applicant attributes and the likelihood of fraud.

Following the baseline establishment, a variety of machine learning algorithms are explored and compared, including K-Nearest Neighbors (KNN), Decision Tree, Support Vector Machine (SVM) and Random Forest. Each model is evaluated based on its performance metrics, such as accuracy, precision, recall, and F1-score, to identify the most effective approach for fraud detection in loan applications.

The results interpretation phase involves analyzing the model outputs to gain insights into the driving factors behind fraud predictions and identify patterns associated with fraudulent behavior. Recommendations for further research and development are provided, including model refinement, feature importance analysis, data enhancement, real-time implementation, and monitoring and maintenance strategies.

#### Executive summary:
The Fraud Detection Model for Loan Applications is designed to identify potentially fraudulent loan applications based on various applicant attributes and historical loan data. By leveraging machine learning algorithms and historical loan performance data, the model aims to improve the efficiency and accuracy of fraud detection in the lending process.

#### Rationale
The objective of this project is to develop a predictive model that can effectively identify fraudulent loan applications. With the increasing prevalence of fraudulent activities in the lending industry, it is crucial for financial institutions to implement robust fraud detection mechanisms to mitigate risk and protect their assets. By building a fraud detection model, we aim to address the growing concern of fraudulent activities in loan applications and enhance the overall security and integrity of the lending process.

#### Research Question
The primary question this project seeks to answer is: Can we develop a predictive model that accurately identifies potentially fraudulent loan applications based on applicant attributes and historical loan data? By analyzing applicant information, credit history, and loan characteristics, we aim to identify patterns and indicators of potential fraud and develop a model that can effectively flag suspicious loan applications for further review.

#### Data Sources
Referred [loan data](https://www.kaggle.com/datasets/nezukokamaado/auto-loan-dataset) from kaggle


#### Methodology
The development of a fraud detection model for loan applications is essential for mitigating financial risks and safeguarding lenders' assets. This project aims to construct a robust and accurate predictive model capable of identifying potentially fraudulent loan applications. The methodology encompasses several key components, including data collection, preprocessing, feature engineering, model development, evaluation, and interpretation.

1. **Data Collection**: Referred comprehensive loan application data from kaggle, including applicant information, loan details, prior loan details, dti, loan amount, income details ,etc.
2. **Data Preprocessing**: Data as such no missing values except categorical features, so encoding categorical variables, and creating new features.
3. **Feature Engineering**: Critical step in order to transition from a unsupervised to a supervised model by creating target feature called fraud flag which inturn to depend on new feature loan to income and prior loan called-off status. New feature, the loan-to-income ratio (LTI), calculated as the ratio of the loan amount to the applicant's income. A high LTI ratio may indicate that the applicant is overleveraged and at a higher risk of default or fraud. Incorporate a feature indicating the prior loan charged-off status, which flags whether the applicant has a history of previous loan charge-offs. This information provides valuable insight into the applicant's creditworthiness and past financial behavior. Followed below steps
   - New feature **loan-to-income** calculated as the ratio of the loan amount to the applicant's income. A high LTI ratio may indicate that the applicant is overleveraged and at a higher risk of default or fraud. Spread of new feature accross employment length depicted below which is clear indication that 84% of LTI within 0.3 which can be baseline ratio to start with.
   - ![image](https://github.com/muralikandan/fraud_detection/assets/5803282/956c2d2a-3585-4b42-affb-bbe643aa86e4)
   - Previous loan charge-off status accounted completely as that evenly (12 to 15%) spread across all years of employment length. 
   - ![image](https://github.com/muralikandan/fraud_detection/assets/5803282/b714c445-720f-4411-84e8-d178d57b6905)
   - Target feature **fraud_flag** derived based on above two features like application with LTI above 0.3 and charge-off, flagged as potential fraud which like 3% of application flagged as fraudualent application - imbalanced data based on threshold which influences model and metrics to account for.
5. **Model Development**:  To establish a performance benchmark, a baseline model using a Dummy Classifier is first created. This simplistic model sets the minimum level of predictive accuracy necessary for more complex models to surpass. Subsequently, a simple logistic regression model is trained to provide insights into the relationship between applicant attributes and the likelihood of fraud. Performance and metrics calculated as below for simple logistic regression model   

   - Simple LogisticRegression Model F1 Score: 0.41269841269841273 
   - Simple & Default Logistic test accuracy Score: 0.9712286158631416
   - Simple & Default Logistic train accuracy Score: 0.9701879455605963

- ![image](https://github.com/muralikandan/fraud_detection/assets/5803282/71312b04-7dbd-4ef6-b6fd-454bf4c96c14)

6. **Model Comparison & Evaluation**: Following the baseline establishment, a variety of machine learning algorithms are explored and compared, including K-Nearest Neighbors (KNN), Decision Tree, Support Vector Machine (SVM) and RandomForest classifier. Each model is evaluated based on its performance metrics, such as train accuracy, test accuracy, time taken and ROC curve with AUC comparison and F1 score, to identify the most effective approach for fraud detection in auto loan applications.
   - Metrics AUC & F1 score accounted as load application is a imbalanced data
   - ![default-model-comparison-outcome](https://github.com/muralikandan/fraud_detection/assets/5803282/c708d776-522c-49e0-b12d-897f2288bf74)
   - ![image](https://github.com/muralikandan/fraud_detection/assets/5803282/3fef1233-10e6-49a5-97cd-6c2737bfcaf5)

7. **Results Interpretation**: The results interpretation phase involves analyzing the model outputs to gain insights into the driving factors behind fraud predictions and identify patterns associated with fraudulent behavior. Recommendations for further research and development are provided, including model refinement, feature importance analysis, data enhancement, real-time implementation, and monitoring and maintenance strategies. 
      -Model improvement with adjusting model hyperparameter and metrics cross validation  
      - ![tuned-model-comparison-outcome](https://github.com/muralikandan/fraud_detection/assets/5803282/8b08683e-09ee-433e-b88c-81d3314e483b)
      - ![image](https://github.com/muralikandan/fraud_detection/assets/5803282/69b5917e-9c8d-4874-acd6-8671ed5526ec)
8. **Next Steps**: Identify potential areas for model improvement and suggest recommendations for further research and development.

#### Results
The fraud detection model achieved promising results in identifying potentially fraudulent loan applications. Through rigorous data preprocessing, feature engineering, and model training, we were able to develop a model that effectively flags suspicious loan applications with high accuracy. The model's performance was evaluated using various evaluation metrics, demonstrating its effectiveness in detecting fraudulent activities in the lending process.
      - Model Selection : Considering both AUC and F1-score, **Logistic Regression Model** works better for current data set. Though DecisionTree F1-score improved but still auc not as compared to logistic model. Similar for 'RandomForest' where F1-score not as good as Logistic model. For other models, though train and test accuracy score resonably increased but still not as much as logistic interms of both AUC & F1 score metrics. 
   - Feature selection through correlation and feature importance technique leveraged, results as below
   - ![image](https://github.com/muralikandan/fraud_detection/assets/5803282/5572c9de-bb1d-49a8-8d4b-304fc83d15c3)
   - ![feature-importance](https://github.com/muralikandan/fraud_detection/assets/5803282/2d8f4a6d-ebd6-414f-8f0c-e8a28270b671)
   - The 'installment' feature emerge as an important predictor in machine learning models for loan application fraud detection. Also exhibit better correlation with other features such as loan amount, total payment, interest rate and to extent to total income. This feature potential in-direct impact to fraud detection but understanding about high correlations with other features suggest interdependencies and potential multicollinerity, which can affect model performance and interpretation.
   - Keep monitoring loan-to-income threshold & other than charge-off loan status as well for further optimization
        
#### Next steps
1. **Data Enhancement**: Continuously collect and incorporate new data to enhance the model's predictive capabilities and adapt to evolving fraud patterns.
2. **Real-Time Implementation**: Integrate the model into the loan application process for real-time fraud detection and decision-making.
3. **Monitoring and Maintenance**: Implement robust monitoring systems to track model performance, metrics evaluation and update the model regularly based on new data and emerging fraud trends. Also try optimizing loan-to-income threshold based on as sample grows.

#### Outline of project

- [Link to notebook 1](https://nbviewer.org/github/muralikandan/fraud_detection/blob/main/fraud_detection_model.ipynb)
  Note : In order to view all visualizations rendered properly, please open in nbviewer.org (url provided for the same)

##### Contact and Further Information
[Murali Kandan](https://www.linkedin.com/in/muralikandan/)
