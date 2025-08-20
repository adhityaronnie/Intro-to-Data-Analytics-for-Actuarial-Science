Assignment 1 – Data Cleaning & Preparation
Dataset: health_insurance_claims.csv (provided in Week 2–3 lab)
Due Date: 1 (one) week after announced.
Weight: 7.5% of final grade (part of Assignments total 30%)
Learning Objectives
By completing this assignment, students will:
Identify and handle missing data.
Detect and treat duplicate records.
Explore and handle outliers.
Apply transformations to prepare data for analysis.
Document and justify their cleaning decisions.

Tasks
Part A: Initial Inspection (10 points)
Load the dataset and display the first 10 rows.
Report the number of rows and columns.
Generate summary statistics for all numeric variables.
Identify categorical vs. numerical variables.

Part B: Missing Values (20 points)
Report the total number of missing values per variable.
Decide and apply appropriate strategies:
For age: fill with median.
For claim_amount: fill with mean or median (justify your choice).
For diagnosis_code: fill with most frequent category.
Provide before-and-after comparison of missing values.

Part C: Duplicates & Data Integrity (15 points)
Check for duplicate claim_id entries.
Remove duplicates, if any, and report how many rows were removed.
Verify that all remaining claim IDs are unique.

Part D: Outlier Detection (25 points)
Create a boxplot of claim_amount.
Identify potential outliers using the IQR method.
Decide whether to remove, cap, or transform them (justify your approach).
Show before-and-after distribution plots.

Part E: Data Transformation (20 points)
Encode categorical variables (gender, policy_type, payment_status) into numerical form (label encoding or one-hot encoding).
Normalize or standardize the claim_amount variable.
Explain why normalization may be useful for downstream modeling.

Part F: Reporting & Documentation (10 points)
Summarize the cleaning steps performed.
Justify major decisions (e.g., imputation choice, outlier treatment).
Save the final cleaned dataset as health_insurance_claims_clean.csv.

Submission Format
Jupyter Notebook (.ipynb) with:
Clear code and output cells
Comments explaining steps
CSV file of cleaned dataset
Short report (1–2 pages, PDF) summarizing steps and justifications
