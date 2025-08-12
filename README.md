Week1: What this code teaches beginners in actuarial data analytics:
Data loading – using a simple in-memory dataset (can later be replaced by CSV/excel).
Descriptive statistics – describe(), claim frequency, severity.
Visualization – histograms, boxplots for exploratory data analysis (EDA).
Actuarial metric – calculation of Pure Premium as a first step in pricing.
ASSIGNMENT:
Background
You are an actuarial analyst at an insurance company. You have been given a small dataset of policyholders, containing demographic information, sum insured, and claims history. Your task is to perform exploratory data analysis (EDA), visualize the results, and calculate basic actuarial metrics.
Dataset
Use the provided dataset from the starter code: https://github.com/adhityaronnie/Intro-to-Data-Analytics-for-Actuarial-Science/blob/main/week1.py
You may copy it directly from the starter Python code or create your own small dataset with at least 10 policyholders.

Tasks
Data Preparation
-Load the dataset into a Pandas DataFrame.
-Check for missing values and handle them appropriately.
-Create an Age_Group variable with categories:
  Young (≤ 35)
  Middle-aged (36–50)
  Senior (> 50)

Descriptive Statistics
-Show summary statistics for Age, Sum_Insured, and Claim_Amount.
-Calculate Claim Frequency (proportion of policies with a claim).
-Calculate Average Claim Severity (average claim amount, conditional on a claim occurring).
Visualization
-Create a histogram showing the distribution of Age.
-Create a boxplot of Claim_Amount by Age_Group.
-Create a scatter plot of Sum_Insured vs Claim_Amount and comment on any trend.
Actuarial Metric
-Calculate the Pure Premium:
-Pure Premium = Frequency × Severity
-Pure Premium=Frequency×Severity
-Interpret the result: What does this mean for the insurer?
Extension Task (Bonus +5%)
Assume a loading factor of 20% to cover expenses and profit.
-Calculate the Gross Premium:
Gross Premium=Pure Premium×(1+0.20)
-Interpret how this would be used in pricing.
