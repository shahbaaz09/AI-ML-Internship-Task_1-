Task 1: Data Cleaning & Preprocessing - AI & ML Internship
This repository contains the solution for Task 1: Data Cleaning & Preprocessing as part of the AI & ML Internship by Elevate Labs.
🎯 Objective
The primary objective of this task was to learn how to clean and prepare raw data for machine learning models. This is a crucial step to ensure that the data is in a suitable format for effective model training.
🛠 Tools Used
 * Python: The core programming language used for data manipulation and analysis.
 * Pandas: A powerful library for data structures and data analysis, especially for tabular data.
 * NumPy: Used for numerical operations, often working in conjunction with Pandas.
 * Matplotlib & Seaborn: Libraries for data visualization, used to understand data distributions and identify outliers.
 * Scikit-learn: Utilized for preprocessing functionalities like StandardScaler and LabelEncoder.
📊 Dataset
The Titanic Dataset was used for this task. This dataset contains information about passengers on the Titanic, including demographics, travel class, and survival status.
📝 Steps Performed
The following steps were implemented to clean and preprocess the dataset, adhering to the mini-guide provided:
 * Data Loading and Initial Exploration:
   * The titanic.csv dataset was loaded into a Pandas DataFrame.
   * Basic information about the dataset, including its shape, data types, and initial count of null (missing) values for each column, was explored using df.info() and df.isnull().sum().
 * Handling Missing Values:
   * Age: Missing values in the 'Age' column were filled with the median age, a robust method to handle numerical missing data that is less affected by outliers.
   * Embarked: Missing values in the 'Embarked' column were filled with the mode (most frequent value), which is suitable for categorical data.
   * Cabin: The 'Cabin' column was dropped entirely due to a very high percentage of missing values, making imputation impractical and potentially misleading.
 * Dropping Irrelevant Columns:
   * Columns such as 'PassengerId', 'Name', and 'Ticket' were dropped as they were deemed irrelevant for direct use in the machine learning model without further complex feature engineering.
 * Converting Categorical Features into Numerical (Encoding):
   * Sex: The 'Sex' column (binary: male/female) was converted into numerical format using Label Encoding, where 'male' and 'female' were mapped to 0 and 1.
   * Embarked: The 'Embarked' column (multi-categorical: S, C, Q) was converted using One-Hot Encoding with drop_first=True to create new binary columns (Embarked_Q, Embarked_S), preventing multicollinearity.
 * Outlier Visualization and Removal:
   * Visualization: Boxplots were generated for numerical features like 'Fare' to visually identify outliers.
   * Removal: Outliers in the 'Fare' column were removed using the Interquartile Range (IQR) method. Rows where 'Fare' values fell outside the calculated upper and lower bounds (Q1 - 1.5*IQR and Q3 + 1.5*IQR) were filtered out.
 * Normalizing/Standardizing Numerical Features:
   * Numerical features, including 'Age', 'Fare', 'SibSp', and 'Parch', were standardized using StandardScaler. This transforms the data to have a mean of 0 and a standard deviation of 1, ensuring that features with larger ranges do not disproportionately influence the model.
🧠 What Was Learned
Through this task, a practical understanding of key data preprocessing techniques was gained, including:
 * Identifying and handling various types of missing data.
 * Transforming categorical variables into numerical formats suitable for machine learning models.
 * Scaling numerical features to ensure consistent ranges across the dataset.
 * Detecting and managing outliers to improve data quality and model performance.
 * Understanding the importance of preprocessing in the overall machine learning workflow.
📁 Repository Contents
 * titanic.csv: The original, raw dataset used for the task.
 * titanic_cleaned.csv: The cleaned and preprocessed dataset after applying all the steps.
 * [task_1].ipynb: The Jupyter Notebook containing all the Python code used for data cleaning and preprocessing.
