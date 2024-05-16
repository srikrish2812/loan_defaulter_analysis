
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

- Create a python environment, activate it and install all the required packages given below in the environment.

```text
aiohttp==3.9.3
aiosignal==1.3.1
anyio==4.3.0
appnope==0.1.4
argon2-cffi==23.1.0
argon2-cffi-bindings==21.2.0
arrow==1.3.0
asttokens==2.4.1
async-lru==2.0.4
attrs==23.2.0
autograd==1.6.2
autograd-gamma==0.5.0
Babel==2.14.0
beautifulsoup4==4.12.3
bleach==6.1.0
catboost==1.2.5
certifi==2024.2.2
cffi==1.16.0
charset-normalizer==3.3.2
click==8.1.7
click-plugins==1.1.1
cligj==0.7.2
cmake==3.29.2
comm==0.2.2
contourpy==1.2.0
cycler==0.12.1
debugpy==1.8.1
decorator==5.1.1
defusedxml==0.7.1
executing==2.0.1
fastjsonschema==2.19.1
filelock==3.13.4
fiona==1.9.6
fonttools==4.50.0
formulaic==1.0.1
fqdn==1.5.1
frozenlist==1.4.1
fsspec==2024.3.1
future==1.0.0
geopandas==0.14.3
graphviz==0.20.3
h11==0.14.0
httpcore==1.0.4
httpx==0.27.0
idna==3.6
imbalanced-learn==0.12.2
interface-meta==1.3.0
ipykernel==6.29.3
ipython==8.22.2
ISLP==0.3.22
isoduration==20.11.0
jedi==0.19.1
Jinja2==3.1.3
joblib==1.3.2
json5==0.9.22
jsonpointer==2.4
jsonschema==4.21.1
jsonschema-specifications==2023.12.1
jupyter-events==0.9.1
jupyter-lsp==2.2.4
jupyter_client==8.6.1
jupyter_core==5.7.2
jupyter_server==2.13.0
jupyter_server_terminals==0.5.3
jupyterlab==4.1.5
jupyterlab_pygments==0.3.0
jupyterlab_server==2.25.4
kiwisolver==1.4.5
lifelines==0.28.0
lightgbm==4.3.0
lightning-utilities==0.11.2
lxml==5.2.1
MarkupSafe==2.1.5
matplotlib==3.8.3
matplotlib-inline==0.1.6
mistune==3.0.2
mpmath==1.3.0
multidict==6.0.5
nbclient==0.10.0
nbconvert==7.16.2
nbformat==5.10.3
nest-asyncio==1.6.0
networkx==3.3
notebook==7.1.2
notebook_shim==0.2.4
numpy==1.24.4
overrides==7.7.0
packaging==24.0
pandas==1.5.3
pandocfilters==1.5.1
parso==0.8.3
patsy==0.5.6
pexpect==4.9.0
pillow==10.2.0
platformdirs==4.2.0
plotly==5.21.0
progressbar2==4.4.2
prometheus_client==0.20.0
prompt-toolkit==3.0.43
psutil==5.9.8
ptyprocess==0.7.0
pure-eval==0.2.2
pycparser==2.21
pydataset==0.2.0
pygam==0.9.0
Pygments==2.17.2
pyparsing==3.1.2
pyproj==3.6.1
python-dateutil==2.9.0.post0
python-json-logger==2.0.7
python-utils==3.8.2
pytorch-lightning==2.2.1
pytz==2024.1
PyYAML==6.0.1
pyzmq==25.1.2
referencing==0.33.0
requests==2.31.0
rfc3339-validator==0.1.4
rfc3986-validator==0.1.1
rpds-py==0.18.0
scikit-learn==1.4.1.post1
scipy==1.11.4
seaborn==0.13.2
Send2Trash==1.8.2
shapely==2.0.3
six==1.16.0
sniffio==1.3.1
soupsieve==2.5
stack-data==0.6.3
statsmodels==0.14.1
sympy==1.12
tenacity==8.2.3
terminado==0.18.1
threadpoolctl==3.4.0
tinycss2==1.2.1
torch==2.2.2
torchmetrics==1.3.2
tornado==6.4
tqdm==4.66.2
traitlets==5.14.2
types-python-dateutil==2.9.0.20240315
typing_extensions==4.11.0
tzdata==2024.1
uri-template==1.3.0
urllib3==2.2.1
wcwidth==0.2.13
webcolors==1.13
webencodings==0.5.1
websocket-client==1.7.0
wrapt==1.16.0
xgboost==2.0.3
yarl==1.9.4
```

- After successfully installing the above packages in the environment, download the all the project files in a single folder. Navigate to the project folder in the command line and open the jupyter notebook using the following command.

```
jypter notebook
```
- Run the notebook to reproduce the results.

