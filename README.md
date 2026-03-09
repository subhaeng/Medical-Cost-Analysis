
🏥 Medical Cost Analysis








📌 Project Overview

The Medical Cost Analysis project explores healthcare insurance data to understand the key factors that influence medical insurance costs.

Using Python and data analysis techniques, this project performs data cleaning, exploratory data analysis (EDA), and visualization to uncover patterns between variables such as age, BMI, smoking habits, number of children, and region and their impact on medical expenses.

The goal is to gain data-driven insights that can help healthcare providers and insurance companies better understand cost drivers in medical insurance.

🎯 Business Problem

Healthcare costs vary widely depending on multiple factors. Understanding these drivers can help:

Insurance companies predict medical expenses

Customers understand cost risks

Healthcare organizations optimize insurance plans

This project answers questions such as:

How does age affect medical charges?

Do smokers pay higher insurance costs?

Does BMI influence medical expenses?

How do family size and region affect costs?

📂 Dataset Description

The dataset contains information about insurance beneficiaries and their medical charges.

Key Columns
Column	Description
age	Age of the insured person
sex	Gender of the individual
bmi	Body Mass Index
children	Number of dependents
smoker	Smoking status (Yes/No)
region	Residential region
charges	Medical insurance cost
🛠 Tools & Technologies Used
Tool	Purpose
Python	Data analysis
Pandas	Data manipulation
Matplotlib	Data visualization
Jupyter Notebook	Interactive analysis
📁 Project Structure
Medical-Cost-Analysis
│
├── Medical Cost Analysis.ipynb
├── insurance.csv
├── README.md
🔎 Data Analysis Workflow
1️⃣ Import Required Libraries
import pandas as pd
import matplotlib.pyplot as plt

These libraries are used for data analysis and visualization.

2️⃣ Load the Dataset
df = pd.read_csv("insurance.csv")

The dataset is loaded into a Pandas DataFrame for further analysis.

3️⃣ Data Exploration

Initial exploration helps understand the dataset.

df.head()
df.info()
df.describe()
df.shape

This step identifies:

Dataset structure

Data types

Statistical summaries

Number of records

4️⃣ Data Cleaning
Check Missing Values
df.isnull().sum()
Check Duplicate Records
df.duplicated().sum()

Ensuring the dataset is clean and consistent before performing analysis.

📊 Exploratory Data Analysis (EDA)
Age vs Medical Charges
plt.scatter(df["age"], df["charges"])
plt.title("Age vs Medical Charges")
plt.show()

This visualization shows how medical costs increase with age.

🚬 Smoking Impact on Medical Cost
df.groupby("smoker")["charges"].mean()

This analysis compares average medical charges for smokers and non-smokers.

⚖ BMI vs Medical Charges
plt.scatter(df["bmi"], df["charges"])
plt.title("BMI vs Medical Charges")
plt.show()

This helps analyze whether higher BMI leads to higher medical costs.

👨‍👩‍👧 Family Size Impact
df.groupby("children")["charges"].mean()

This analysis checks whether having more dependents affects medical costs.

🌍 Regional Medical Cost Comparison
df.groupby("region")["charges"].mean()

This shows how medical costs vary across different regions.

💡 Key Insights

✔ Smokers have significantly higher medical charges compared to non-smokers.

✔ Medical costs increase with age, indicating higher healthcare risks.

✔ Higher BMI is associated with increased medical expenses.

✔ Regional differences exist but are less significant compared to smoking status.

✔ Number of children has moderate impact on insurance costs.

📈 Business Implications

The insights from this analysis can help:

Insurance companies improve pricing models

Healthcare providers identify high-risk groups

Policymakers promote preventive health strategies

🚀 Future Improvements

This project can be extended by:

Building a machine learning model to predict medical charges

Creating interactive dashboards using Power BI or Tableau

Performing advanced statistical analysis

Deploying the analysis as a data analytics web app
