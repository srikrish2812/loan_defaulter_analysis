
# German Bank Loan Defaulter Analysis - Project Overview

This is the final project for the course INFO-521 Introduction to Machine Learning. The main aim of the project is to build a machine learning model that can be used by the German bank to predict whether the customer will default on their loan or not. The dataset used in this project contains historical data about the customers of a German bank who have taken loans. The dataset has 17 columns and 1000 rows where each row represents the historical data of a customer. The target or the response that needs to be predicted is 'default' and the remaining 16 columns are used as predictors. 


## Project Folder

The project folder consists of a dataset file, python notebook, python notebook exported as a HTML file, report document(.docx), report pdf(.pdf) and a README.txt file.

1. Dataset file: The dataset file **credit.csv** contains historical data of the customers that took loan from the German bank.

2. Python notebook: **IML_final_project_week6_Abhay.ipynb** contains the detailed analysis of the dataset along with various ML models that are trained on the dataset.

3. HTML file: It is the python notebook exported as a html file.

4. Report document: This is the project report in .docx format

5. Report PDF: This is the project report in .pdf format

6. README.txt: This file has brief introduction about the project and its organization.

In addition to the above file my project directory has a pics folder and a catboost_info folder. The folder pics contains pictures regarding the project and the folder catboost_info contains information regrading the catboost model training and tuning.

## Structure of My Project folder




## Python notebook structure

In this notebook, firstly the main context and problem statement are explained briefly along with dataset details. The problem introduction is followed by the code part. The code is divided into 6 main sections with sub-sections within them as follows:

1. Import required packages and Load the dataset: In this section, all the required functions, modules and metrics are imported and the **credit.csv** file is loaded.

2. Exploratory Data Analysis or Visualizing Data: In this section missing, duplicate and null values are handled and various plots of categorical and numerical vairables are drawn. These plots include different types of frequency plots. In addition to this a correlation matrix is constructed on the numerical variables to assess the correlation among any variables.

3. Pre-processing data for model training: In this section, the dataset is split into training and test sets in a 70:30 ratio and pre-processing steps such as one-hot encoding, ordinal encoding and normalization are applied on the dataset to transform it into the required format.

4. Training and Testing different models: In this section models like Bagging, Random Forest, GBM, AdaBoost, XGBoost are tuned to get the optimal parameters and once again these models are trained on the training dataset using the optimal parameters obtained above. The parameters are tuned using grid-search cross-validation approach. Finally, the above trained models are evaluated on the test dataset and results are plotted. Additionally, CatBoost and LightGBM models are also trained but not with optimal parameter setting.

5. Comparing models: In this section all the model results are consolidated and put into a dataframe for effective comparison.

6. Observations: This section contains all the observations done on the results obtained in the previous sections. AdaBoost was found to be the best model for this task as it has high recall, good accuracy and decent precision values. Finally, the top three important features of the dataset in the AdaBoost model are found to be amount, months_loan_duration and credit_history.



## Installation
Please follow these steps to reproduce the results.

- Create a python environment, activate it and install all the required packages present in the requirements.txt file in the environment.

```bash
pip install -r requirements.txt
```

- After successfully installing the above packages in the environment, download the all the project files in a single folder. Navigate to the project folder in the command line and open the jupyter notebook using the following command.

```
jypter notebook
```
- Run the notebook to reproduce the results.

