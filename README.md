# Predicting Loan Rejection

A model is created to predict whether a loan will be *rejected or accepted*. The prediction is based on how likely repayment of the loan is, which itself is predicted by a number of features in the data set. The data set has been taken from [here](https://www.kaggle.com/datasets/architsharma01/loan-approval-prediction-dataset). A **Logistic Regression** model is choosen for this application as a starting point. In the future, additional models may be tested on the same data set.

# The Approach

We use a *one-hot encoding* approach to encode non-numerical variables. A simple *label encoder* is used to encode the target variable. Variables are *scaled* before training.

An *80/20 split* is used for the data set, with 80% of the data going to training, and 20% for testing.

# Results

The results of the model are discussed below.

An *accuracy* of 0.9227 is quite good, indicating that the model decides correctly most of the time. The model approves more loans which were originally rejected than it rejects those which were approved (40 vs 26), indicating a slight bias towards approving loans.

The *ROC curve* shows very low false-positive reporting. A standard deviation of 2.17% indicates very little variance. Dividing data into 5 buckets and analyzing their accuracy gives values ranging aproximately from 0.896 to 0.925, signalling minimal *over-fitting*.


# Future Improvements

Over-all, the model has performed quite well. However, future improvements may include:

- reducing the slight bias towards accepting loans
- experimenting other models (such as random forests) in search of better results
- engaging in further explatory data analysis (EDA) to reveal insights about data guiding model building
- implementing Explainable Artificial Intelligence (XAI) to help build trust on the model's decision

# Tools Used

The project is built in **Python 3** and **Jupyter Notebooks**. A **Logistic Regression** model is trained.

# How to Run

To run this project on your computer, ensure that you have Python 3 installed. Also, you will need Jupter Notebooks support. You can use VSCode with the Jupyter extensions or start your own Jupyter server and open the file in Jupyter Lab. Also ensure that you have the data set downloaded and that the file path points correctly to it.
