## README: Employee Churn Prediction Project

This project focuses on building a predictive model to identify employees who are likely to leave the company (churn). The goal is to provide insights into factors influencing employee retention and to develop a classification model using Logistic Regression.

### Project Steps:

1.  **Data Loading and Initial EDA**: The dataset `people (2).csv` was loaded, and an initial Exploratory Data Analysis (EDA) was performed to understand its shape, data types, and basic statistics.

2.  **Preprocessing and Feature Engineering**: The categorical 'salary' column was mapped to numerical values (low: 1, medium: 2, high: 3) to prepare it for modeling.

3.  **Descriptive Analysis**: Various descriptive analyses were conducted to understand departmental trends in experience, salary, satisfactory levels, projects, last evaluations, and employee churn.

4.  **Relationship Analysis & Visualization**: Several visualizations were generated to explore relationships between key variables such as:
    *   Number of Projects vs. Salary
    *   Number of Projects vs. Employee Left Status
    *   Satisfactory Level vs. Number of Projects
    *   Promotion in Last 5 Years vs. Salary
    *   Department vs. Salary
    *   Average Monthly Hours vs. Satisfactory Level
    *   Satisfactory Level vs. Left Status
    *   Work Accident vs. Left Status

5.  **Encoding and Standardizing for Machine Learning**: The 'dept' column was one-hot encoded, and numerical features were standardized using `StandardScaler` to prepare the data for the machine learning model.

6.  **Split Data and Train Model**: The dataset was split into training (75%) and testing (25%) sets. A Logistic Regression model was then trained on the training data.

7.  **Model Evaluation**: The trained model was evaluated using the test set, and its performance was assessed through:
    *   A Confusion Matrix
    *   A Classification Report (showing precision, recall, f1-score)
    *   Accuracy Score

### Model Performance Summary:

*   **Accuracy**: The model achieved an accuracy of approximately **79.68%** on the test set.
*   **Precision and Recall for 'Left' (Churned) employees**: The model showed a precision of 65% and a recall of 36% for employees who left. This indicates that while the model is reasonably good at predicting who *will* leave when it does predict it, it misses a significant portion of the actual employees who leave (lower recall).
*   **Precision and Recall for 'Stayed' (Non-Churned) employees**: The model performed well in identifying employees who stayed, with a precision of 82% and a recall of 94%.

Further efforts could focus on improving the recall for the 'left' class, potentially through techniques like resampling, using different algorithms, or engineering more predictive features.
