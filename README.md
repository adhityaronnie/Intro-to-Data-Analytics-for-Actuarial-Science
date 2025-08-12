# Intro-to-Data-Analytics-for-Actuarial-Science
# ===========================================
# Introduction to Data Analytics
# for Actuarial Science
# ===========================================

# Install if needed:
# pip install pandas numpy matplotlib seaborn

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# -------------------------------------------
# 1. Load Example Dataset
# -------------------------------------------
# For illustration: claims data
data = {
    'Policy_ID': range(1, 11),
    'Age': [25, 45, 39, 50, 29, 62, 35, 48, 55, 31],
    'Sum_Insured': [50000, 120000, 75000, 200000, 90000, 150000, 110000, 130000, 160000, 80000],
    'Claim_Amount': [0, 20000, 0, 50000, 0, 75000, 15000, 0, 25000, 0],
    'Claim_Flag': [0, 1, 0, 1, 0, 1, 1, 0, 1, 0]  # 1 = claim occurred
}
df = pd.DataFrame(data)

print("First 5 rows of the dataset:")
print(df.head())

# -------------------------------------------
# 2. Basic Summary Statistics
# -------------------------------------------
print("\nSummary Statistics:")
print(df.describe())

print("\nClaim Frequency:")
print(df['Claim_Flag'].mean())  # proportion of claims

print("\nAverage Claim Severity (conditional on having a claim):")
print(df.loc[df['Claim_Amount'] > 0, 'Claim_Amount'].mean())

# -------------------------------------------
# 3. Visualization
# -------------------------------------------
sns.set_style("whitegrid")

# Histogram of Age
plt.figure(figsize=(6, 4))
sns.histplot(df['Age'], bins=5, kde=True, color='skyblue')
plt.title("Distribution of Policyholder Age")
plt.xlabel("Age")
plt.ylabel("Count")
plt.show()

# Boxplot: Claim Amount by Age Group
df['Age_Group'] = pd.cut(df['Age'], bins=[20, 35, 50, 65], labels=['Young', 'Middle-aged', 'Senior'])

plt.figure(figsize=(6, 4))
sns.boxplot(x='Age_Group', y='Claim_Amount', data=df, palette='Set2')
plt.title("Claim Amount by Age Group")
plt.show()

# -------------------------------------------
# 4. Simple Risk Metric
# -------------------------------------------
# Pure Premium = Frequency × Severity
frequency = df['Claim_Flag'].mean()
severity = df.loc[df['Claim_Amount'] > 0, 'Claim_Amount'].mean()
pure_premium = frequency * severity

print(f"\nPure Premium Estimate: {pure_premium:,.2f}")
