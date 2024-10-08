Employee Turnover Analytics 
Project Goal:

Develop machine learning models to predict employee turnover at Portobello Tech. By analyzing employee work details and satisfaction levels, we aim to identify patterns and factors that contribute to employee departures.

Data Description:

The dataset provides information about Portobello Tech employees, including their:

Satisfaction Level (satisfaction_level)
Last Evaluation Rating (last_evaluation)
Number of Projects (number_project)
Average Monthly Working Hours (average_montly_hours)
Time Spent in Company (time_spend_company)
Work Accident (Work_accident)
Left Status (left) - 0 (Stayed), 1 (Left)
Promotions in Last 5 Years (promotion_last_5years)
Department (Department)
Salary (salary)
Tasks:

Data Quality Checks:

Identify and handle missing values in the data.
Exploratory Data Analysis (EDA):

2.1. Correlation Matrix Heatmap:

Visualize the relationships between numerical features (satisfaction level, evaluation rating, etc.) using a heatmap. This helps identify potential correlations between factors and employee turnover.
2.2. Distribution Plots:

Create distribution plots for:
Employee satisfaction level
Employee evaluation rating
Employee average monthly hours
These plots will reveal data distribution patterns and potential outliers.
2.3. Bar Plot with Hue:

Plot the number of projects worked on for employees who stayed and those who left.
Analyze the distribution to see if project count correlates with employee turnover.
Clustering Analysis:

3.1. Target Columns:

Select "satisfaction_level," "last_evaluation," and "left" for clustering.
3.2. K-means Clustering:

Perform K-means clustering on employees who left (marked as "1" in the "left" column). Set the number of clusters to 3.
3.3. Cluster Interpretation:

Analyze the resulting clusters based on satisfaction and evaluation scores. Are there distinct patterns in employee subgroups who left?
Class Imbalance Handling:

4.1. Data Preprocessing:

Separate categorical features (Department) from numerical features.
Use get_dummies() to convert categorical features into numerical columns.
Combine preprocessed data back into a single dataset.
4.2. Stratified Split:

Divide the dataset into training (80%) and testing (20%) sets using a stratified split to ensure class balance within each set.
Set a random state (e.g., 123) for reproducibility.
4.3. SMOTE Upsampling:

Upsample the minority class (employees who left) in the training set using the SMOTE (Synthetic Minority Oversampling Technique) technique. This helps balance the data for better model performance.
Model Training and Evaluation:

5.1. Logistic Regression:

Train a logistic regression model to predict employee turnover.
Apply 5-fold cross-validation (CV) to evaluate the model'sgeneralizability.
Generate a classification report based on the CV results, showing precision, recall, F1-score, and accuracy for each class (stayed/left).
5.2. Random Forest Classifier:

Train a Random Forest Classifier model.
Perform 5-fold CV and generate a classification report.
5.3. Gradient Boosting Classifier:

Train a Gradient Boosting Classifier model.
Perform 5-fold CV and generate a classification report.
Model Selection and Evaluation Metrics:

6.1. ROC AUC:

Calculate the ROC-AUC (Receiver Operating Characteristic Area Under Curve) score for each model.
Plot the ROC curves for each model to visualize their performance in classifying employees who will likely leave.
6.2. Confusion Matrix:

Generate a confusion matrix for each model.
Analyze the confusion matrix to understand the models' performance in terms of true positives, false positives, true negatives, and false negatives.
6.3. Choosing the Best Model:

Compare model performance using metrics like accuracy, precision, recall, F1-score, and ROC-AUC.

Select the model that offers the best balance between predicting true positives (employees likely to leave) and avoiding false positives (employees incorrectly classified as leaving).

Recall vs. Precision:

In this context, recall is more important
