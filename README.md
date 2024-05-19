### Fraud Detection Model for Loan Applications

**Murali Kandan**

#### Executive summary:
The Fraud Detection Model for Loan Applications is designed to identify potentially fraudulent loan applications based on various applicant attributes and historical loan data. By leveraging machine learning algorithms and historical loan performance data, the model aims to improve the efficiency and accuracy of fraud detection in the lending process.

#### Rationale
The objective of this project is to develop a predictive model that can effectively identify fraudulent loan applications. With the increasing prevalence of fraudulent activities in the lending industry, it is crucial for financial institutions to implement robust fraud detection mechanisms to mitigate risk and protect their assets. By building a fraud detection model, we aim to address the growing concern of fraudulent activities in loan applications and enhance the overall security and integrity of the lending process.

#### Research Question
The primary question this project seeks to answer is: Can we develop a predictive model that accurately identifies potentially fraudulent loan applications based on applicant attributes and historical loan data? By analyzing applicant information, credit history, and loan characteristics, we aim to identify patterns and indicators of potential fraud and develop a model that can effectively flag suspicious loan applications for further review.

#### Data Sources
Referred data from kaggle
https://www.kaggle.com/datasets/nezukokamaado/auto-loan-dataset

#### Methodology
The development of a fraud detection model for loan applications is essential for mitigating financial risks and safeguarding lenders' assets. This project aims to construct a robust and accurate predictive model capable of identifying potentially fraudulent loan applications. The methodology encompasses several key components, including data collection, preprocessing, feature engineering, model development, evaluation, and interpretation.

1. **Data Collection**: Gather comprehensive auto application data, including applicant information, loan details, credit history, etc.
2. **Data Preprocessing**: Clean and preprocess the data, handling missing values, encoding categorical variables, and creating new features.
3. **Feature Engineering**: Critical step in order to transition from a unsupervised to a supervised model. Create a new feature representing the loan-to-income ratio (LTI), calculated as the ratio of the loan amount to the applicant's income. A high LTI ratio may indicate that the applicant is overleveraged and at a higher risk of default or fraud. Incorporate a feature indicating the prior loan charged-off status, which flags whether the applicant has a history of previous loan charge-offs. This information provides valuable insight into the applicant's creditworthiness and past financial behavior. <To include histogram of spread of charge-off accross years of work>
4. **Model Development**:  To establish a performance benchmark, a baseline model using a Dummy Classifier is first created. This simplistic model sets the minimum level of predictive accuracy necessary for more complex models to surpass. Subsequently, a simple logistic regression model is trained to provide insights into the relationship between applicant attributes and the likelihood of fraud.
5. **Model Comparison & Evaluation**: Following the baseline establishment, a variety of machine learning algorithms are explored and compared, including K-Nearest Neighbors (KNN), Decision Tree, and Support Vector Machine (SVM). Each model is evaluated based on its performance metrics, such as train accuracy, test accuracy, time taken and ROC curve with AUC comparison, to identify the most effective approach for fraud detection in auto loan applications.
6. **Results Interpretation**: The results interpretation phase involves analyzing the model outputs to gain insights into the driving factors behind fraud predictions and identify patterns associated with fraudulent behavior. Recommendations for further research and development are provided, including model refinement, feature importance analysis, data enhancement, real-time implementation, and monitoring and maintenance strategies.
7. **Next Steps**: Identify potential areas for model improvement and suggest recommendations for further research and development.

#### Results
The fraud detection model achieved promising results in identifying potentially fraudulent loan applications. Through rigorous data preprocessing, feature engineering, and model training, we were able to develop a model that effectively flags suspicious loan applications with high accuracy. The model's performance was evaluated using various evaluation metrics, demonstrating its effectiveness in detecting fraudulent activities in the lending process.
< Need to include outputs from baseline model, simple modelm comparison with/without tuning>
<Include feature importance correlation>

#### Next steps
1. **Data Enhancement**: Continuously collect and incorporate new data to enhance the model's predictive capabilities and adapt to evolving fraud patterns.
2. **Real-Time Implementation**: Integrate the model into the auto loan application process for real-time fraud detection and decision-making.
3. **Monitoring and Maintenance**: Implement robust monitoring systems to track model performance and update the model regularly based on new data and emerging fraud trends.

#### Outline of project

- [Link to notebook 1](https://github.com/muralikandan/fraud_detection/blob/main/fraud_detection_model.ipynb)


##### Contact and Further Information
[Murali Kandan](https://www.linkedin.com/in/muralikandan/)
