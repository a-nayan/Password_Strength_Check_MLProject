# Password Strength prediction using Logistic Regression Algorithm(Multiclass Classification)

Project Overview:

This project aims to leverage my Data Science capabilities to build a ML model that predicts the strength of a password (o as week, 1 as normal, 2 as strong) and depicts password user the intensity of how hackable a password is on the basis of its length and characters, thus helping a user choose strong password.


The project consists of below parts.

1) Data ingestion - The data is stored in a sqlite database "Users" table. The table has two field "password" and "strength" and consists of 100000 records.
 
2) Data cleaning 
	- Checks for missing values
	- Drop irrelevant features
	- Drop irrelevant rows
	- Conversion of feature data type to appropriate data type
	- Creation of additional features from existing features
	- Ensure data integrity
3) Exploratory data analysis
	- check how many passwords are only numeric
        - check how many passwords have only upper case characters
        - check how many passwords are alphanumeric
        - check how many passwords have title case characters
        - check how many passwords have some special charecters
4) Feature Engineering
	
	- Creating below new features that will help to determine the strength of a password. In order to normalize the data and avoid outlier divide each length frequency by total length
	      1. Length of password
       	      2. Lower Case letter frequency
              3. Upper Case letter frequency
              4. Digit frequency
              5. Special Character frequency
	- Convert the password feature into TF-IDF matrix feature using TfidVectorizer before training model
 	- Outlier Detection and handling- Perform descriptive statistics and plot graphs on above created features to detect outlier if any
	- Calculate mutual information score between feature strength and other remaining independent features and plot graphs to determine which features are worth to consider for ML algorithm

5) Model Building
	- Build model for the problem which is multiclass classification.  
	- Train and Test
	- Calculate accuracy_score, confusion_matrix and classification_report to check how model is performing.


Tools Used: Jupyter Notebook, Python
Skills Used: 
	Statistics,
	Python Library -  os, pandas, numpy, sqlite3, matplotlib.pyplot, 
			seaborn, 
			mutual_info_regression from sklearn.feature_selection, 
			TfidfVectorizer from sklearn.feature_extraction, 
			LogisticRegression from sklearn.linear_model
			classification_report, accuracy_score, confusion_matrix  from sklearn.metrics 