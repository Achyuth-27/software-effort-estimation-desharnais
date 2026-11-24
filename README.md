Software Effort Estimation Using Machine Learning Overview

This project investigates software effort estimation using the Desharnais Software Project Dataset. The objective is to develop machine learning models that can accurately predict the effort required for software projects based on project characteristics.

The project follows a complete machine learning workflow, beginning with data understanding and exploratory analysis, followed by preprocessing, feature selection, model development, hyperparameter tuning, and model evaluation. Several regression models are compared to determine which approach provides the most reliable predictions.

This project was completed as part of my MSc in Business Analytics for Decision Makers at the National College of Ireland.

Dataset

The project uses the Desharnais Software Project Dataset, which contains information from 81 completed software projects.

The dataset includes variables describing project size, complexity, team experience, manager experience, programming language, and actual development effort.

The target variable is:

Effort – the actual software development effort required for each project.

Project Workflow

Data Understanding
The project begins with an exploration of the dataset to understand each variable and its relevance to software effort estimation.

During this stage:

Dataset structure is examined. Summary statistics are generated. Duplicate records are checked. Categorical and numerical variables are identified. Identifier variables such as id and Project are removed because they do not contribute to prediction. YearEnd is also removed since it represents projects completed between 1982 and 1988 and is unlikely to generalise well to future projects. 2. Exploratory Data Analysis

Several visualisations are used to better understand the dataset.

The analysis includes:

Distribution of categorical variables Distribution of numerical variables Detection of outliers Skewness analysis Scatter plots showing relationships with software effort Correlation analysis

Special attention is given to the Length variable because it may introduce data leakage. Since it is unclear whether project duration is known before or after project completion, models are evaluated both with and without this feature.

Data Preprocessing
The dataset is prepared for machine learning by performing several preprocessing steps, including:

Handling missing values Handling invalid values One-hot encoding of categorical variables Feature scaling Multicollinearity analysis Feature selection using SelectKBest

These steps help improve model performance and ensure the data is suitable for regression analysis.

Machine Learning Models

The following regression models are developed and compared:

Linear Regression Ridge Regression Lasso Regression Random Forest Regressor Gradient Boosting Regressor Artificial Neural Network (Multi-Layer Perceptron)

Each model is trained using the same preprocessing pipeline to ensure a fair comparison.

Model Evaluation

The models are evaluated using:

Root Mean Squared Error (RMSE) Mean Absolute Error (MAE) R² Score

Model performance is compared both with and without the Length feature to investigate its impact on prediction accuracy.

Feature Importance

For the best-performing models, feature importance is analysed to understand which project characteristics have the greatest influence on software development effort.

The analysis shows that project size, measured through function point-related variables, is one of the strongest predictors of software effort.

Hyperparameter Tuning

To further improve model performance, hyperparameter tuning is performed.

The project also includes:

Pipeline-based model evaluation Bootstrap evaluation Comparison of different tuning strategies Selection of the best-performing model based on evaluation metrics Technologies Used Python Jupyter Notebook Pandas NumPy Matplotlib Seaborn Scikit-learn

How to Run the Project Clone this repository. Install the required libraries listed in requirements.txt. Open the notebook in Jupyter Notebook. Run the notebook from top to bottom to reproduce the complete analysis and results. Key Findings Careful data preprocessing improved the quality of the dataset before modelling. Feature selection helped reduce unnecessary variables while retaining the most informative predictors. Comparing models with and without the Length feature showed that removing it had only a small impact on prediction performance, suggesting the models remained reliable without relying on a potentially leaked variable. Hyperparameter tuning further improved model performance. Among the evaluated models, Lasso Regression provided the best overall balance between prediction accuracy and model simplicity for this dataset. Future Work

Possible extensions of this project include:

Evaluating additional software effort estimation datasets. Comparing more advanced ensemble learning methods. Investigating explainable AI techniques such as SHAP for model interpretation. Exploring alternative feature selection methods and validation strategies. Author

Achyuth Manjunatha

MSc Business Analytics for Decision Makers

National College of Ireland
