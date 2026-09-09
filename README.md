<div align="center">

# 📊 Marketing Campaign Performance Analysis

### Turning Marketing Data into Customer Insights & Business Decisions

<br>

<img src="https://img.shields.io/badge/Python-Data%20Analysis-blue?style=for-the-badge&logo=python&logoColor=white">
<img src="https://img.shields.io/badge/SQL-Business%20Analysis-orange?style=for-the-badge&logo=sqlite&logoColor=white">
<img src="https://img.shields.io/badge/Power%20BI-Dashboard-yellow?style=for-the-badge&logo=powerbi&logoColor=black">
<img src="https://img.shields.io/badge/Google%20Data%20Analytics-Certificate-green?style=for-the-badge&logo=google&logoColor=white">

</div>

---

<div align="center">

> **Marketing Data → Cleaning → Analysis → Segmentation → Visualization → Insights → Decisions**

</div>

---

## 🎯 Project Overview

This project is an **end-to-end Marketing Campaign Performance Analysis** built as a portfolio project to demonstrate practical Data Analytics skills.

The analysis uses the public **Customer Personality Analysis** dataset to explore customer behavior, campaign response, purchasing patterns, customer segments, and marketing opportunities.

The project follows a complete analytical workflow:

**Business Problem → Data Preparation → Exploration → SQL Analysis → Customer Segmentation → Power BI → Business Recommendations**

> ⚠️ **Disclaimer:** This is a portfolio project based on a public dataset and a fictional business scenario. It does not represent analysis performed for the original dataset owner.

---

# 📌 Business Problem

A company wants to better understand its customers and improve the performance of its marketing campaigns.

The main question is:

### **How can a company understand its customers and campaign performance to make better marketing decisions?**

To answer this, the analysis investigates customer demographics, purchasing behavior, campaign responses, engagement patterns, and customer value.

---

# ❓ Business Questions

The analysis focuses on questions such as:

- What percentage of customers responded to the latest campaign?
- Which customer segments are more responsive?
- How does customer spending differ between responders and non-responders?
- Which purchasing channels are most associated with campaign response?
- Which product categories generate the highest spending?
- Does customer recency relate to campaign response?
- Does customer tenure relate to campaign response?
- How does campaign response vary across education levels and family size?
- Can customers be grouped into meaningful value-based segments?
- Which customers should receive greater marketing attention?

---

# 🛠️ Tech Stack

<div align="center">

| Tool | Purpose |
|---|---|
| 🐍 **Python** | Data cleaning, EDA, statistics & segmentation |
| 🐼 **Pandas** | Data manipulation & analysis |
| 🔢 **NumPy** | Numerical operations |
| 🗃️ **SQL / SQLite** | Business-oriented data analysis |
| 🤖 **Scikit-learn** | Customer segmentation using K-Means |
| 📊 **Power BI** | Interactive dashboard & visualization |
| 📓 **Jupyter / Google Colab** | Analytical workflow |
| 🐙 **GitHub** | Project documentation & versioning |

</div>

---

# 🔄 Project Workflow

```text
                MARKETING DATA
                      │
                      ▼
              DATA PREPARATION
                      │
                      ▼
               DATA CLEANING
                      │
                      ▼
             EXPLORATORY ANALYSIS
                      │
                      ▼
              SQL BUSINESS ANALYSIS
                      │
                      ▼
           CUSTOMER SEGMENTATION
                      │
                      ▼
              POWER BI DASHBOARD
                      │
                      ▼
                 KEY INSIGHTS
                      │

📂 Dataset
Dataset: Customer Personality Analysis
Records: 2,240 original customers
Final analytical dataset: 2,233 customers
The dataset contains information about:
Customer demographics
Income
Household composition
Product spending
Purchasing channels
Campaign acceptance
Customer recency
Customer enrollment date
🧹 Data Preparation & Cleaning
The dataset was inspected and prepared before analysis.
Data Quality Checks
Checked dataset dimensions
Checked missing values
Checked duplicate records
Checked data types
Checked unique customer IDs
Investigated suspicious birth years
Investigated income outliers
Converted customer dates into proper datetime format
Missing Values
Only the Income column contained missing values.
The missing income values were handled using median imputation.
Customer Status
Marital status categories were simplified into:
Partner
Alone
Rare inconsistent categories such as YOLO and Absurd were removed.
Age
Age was derived from the birth year.
Three implausible birth-year records were identified through the resulting age values and excluded by applying an age validity filter.
Additional Features
Several analytical features were created:
Children
Age
Total_Spending
Total_Purchases
Family_Size
Customer_Tenure_Days
Customer_Segment
📊 Exploratory Data Analysis
The exploratory analysis examined:
👥 Customer Characteristics
Age
Education
Marital status
Income
Children
Family size
💰 Customer Value
Total spending
Product-level spending
Total purchases
Purchasing channels
📣 Campaign Performance
Overall response
Previous campaign acceptance
Response by education
Response by number of children
Response by customer tenure
Response by recency
📈 Key Campaign Results
�

KPI
Result
👥 Customers
2,233
📣 Responders
332
📊 Response Rate
14.87%
💰 Average Income
52.21K
🛒 Average Purchases
12.54
💵 Average Spending
605.38
�

💡 Customer Response Analysis
One of the strongest patterns found in the analysis was the difference between customers who responded to the campaign and those who did not.
Average Total Spending
Customer Group
Average Spending
Responders
988.40
Non-Responders
538.49
Responders spent substantially more on average than non-responders.
Average Purchases
Customer Group
Average Purchases
Responders
15.36
Non-Responders
12.05
Responders also showed higher purchasing activity across channels.
🧩 Customer Segmentation
Customer segmentation was performed using K-Means clustering.
The segmentation model used behavioral and value-related features:
Income
Recency
Total_Spending
Total_Purchases
NumWebPurchases
NumCatalogPurchases
NumStorePurchases
Why K = 2?
Different values of K were evaluated using the Silhouette Score.
Clusters
Silhouette Score
2
0.436
3
0.311
4
0.247
5
0.247
6
0.247
7
0.251
8
0.248
The strongest result was obtained with K = 2.
�

0.436
Best Silhouette Score
�

👤 Customer Segments
The final segmentation produced two main customer groups.
Segment
Customers
Avg. Income
Avg. Spending
Avg. Purchases
Response Rate
🟢 Higher-Value Customers
1,058
69.03K
1,132.60
19.15
20.98%
🔵 Lower-Value Customers
1,174
36.53K
130.71
6.58
9.37%
Key Finding
The Higher-Value Customer segment represents approximately 47.4% of customers, but accounts for approximately 66.9% of campaign responders.
�

2.24×
Higher response rate among Higher-Value Customers
�

🔍 Important Analytical Decision
The Response and AcceptedCmp1–5 variables were not used as inputs for customer segmentation.
This was done intentionally to avoid target leakage and circular analysis.
Instead, campaign response was evaluated after segmentation to understand how the resulting customer groups differed in responsiveness.
⚠️ Outlier Handling
An income value of 666,666 was identified as a potential data-quality outlier.
Rather than deleting the customer from the entire dataset, the record was retained for the main analysis.
The value was excluded specifically from the clustering process because it could disproportionately influence distance-based segmentation.
This preserves the original analytical data while preventing one extreme value from dominating the clustering model.
⏱️ Customer Recency & Tenure
Recency
Customers who responded to the campaign had a lower average recency:
Group
Average Recency
Responders
35.41 days
Non-Responders
51.54 days
This suggests that more recently active customers were more responsive in this dataset.
Customer Tenure
Response was also associated with customer tenure.
Tenure Group
Response Rate
Less than 6 months
8.65%
6–12 months
9.38%
1–1.5 years
16.61%
More than 1.5 years
26.48%
Longer-tenure customers showed higher observed response rates.
🛍️ Product Insights
Responders had higher average spending across all major product categories.
The largest absolute spending differences were observed in:
🥇 Wines
🥈 Meat Products
This suggests potential opportunities for targeted offers and cross-selling around these categories.
These are observed associations in the dataset and should not be interpreted as proof that product preferences cause campaign response.

📣 Response by Education
Observed response rates:
Education
Response Rate
PhD
20.70%
Master
15.45%
Graduation
13.41%
2n Cycle
10.95%
Basic
3.70%
Education showed noticeable differences in campaign response, although it should be considered alongside behavioral and purchasing characteristics.
📊 Power BI Dashboard
The final Power BI dashboard brings together the main findings into a single analytical view.
Dashboard includes:
Total Customers
Responders
Average Income
Average Spending
Average Purchases
Response Rate
Response Rate by Customer Segment
Customer Distribution by Segment
Spending by Campaign Response
Product Spending by Response
Purchases by Channel
Response Rate by Customer Tenure
Response Rate by Education
Dashboard preview will be added here.
🎯 Business Recommendations
Based on the observed patterns:
Recommendation
Business Rationale
🎯 Prioritize Higher-Value Customers
Higher observed response rate and stronger purchasing behavior
⏱️ Use Recency for Targeting
More recently active customers showed higher response
🛒 Personalize by Purchasing Behavior
Responders were more active across purchasing channels
🍷 Focus on Strong Product Categories
Wines and Meat showed the largest spending differences
⭐ Build Loyalty Strategies
Longer-tenure customers showed higher response rates
🚀 Improve New-Customer Engagement
Newer customers showed lower observed response rates
These recommendations describe data-driven opportunities, not guaranteed causal effects.
🗃️ SQL Business Analysis
SQL was used to answer business questions directly from the analytical dataset.
The analysis included:
✓ Overall campaign response rate
✓ Response by education
✓ Response by number of children
✓ Spending by response
✓ Purchases by response
✓ Income by response
✓ Recency by response
✓ Purchasing channel comparison
✓ Previous campaign acceptance
✓ Product category spending
✓ Customer tenure analysis
🎓 Google Data Analytics Professional Certificate
This project was designed to apply the analytical thinking developed throughout the Google Data Analytics Professional Certificate.
Course Concept
Applied in This Project
Foundations
Data Analytics workflow
Ask Questions
Business problem & stakeholder questions
Prepare Data
Dataset understanding & preparation
Process Data
Data cleaning & quality checks
Analyze Data
EDA, statistics & SQL
Share Data
Power BI visualization
R Programming
Analytical concepts implemented using Python
End-to-End Analysis
Complete marketing analysis
Capstone Thinking
Business insights & recommendations
The analytical concepts from the R-focused material were implemented using Python, as Python is the primary language used in this project.
📚 What I Learned
This project strengthened my ability to:
Translate a business problem into analytical questions
Clean and validate real-world-style datasets
Work with missing and suspicious data
Perform exploratory data analysis
Use SQL for business analysis
Apply customer segmentation techniques
Avoid target leakage
Evaluate clustering using Silhouette Score
Build business-focused Power BI dashboards
Translate analytical findings into recommendations
Communicate insights without confusing correlation with causation
📁 Project Files
marketing-campaign-performance-analysis/
│
├── Marketing_Campaign_Performance_Analysis.ipynb
│
├── Marketing_Campaign_Performance_Analysis 1.pbix
│
└── README.md
📓 Jupyter Notebook
Contains the complete Python workflow:
Cleaning → EDA → SQL → Segmentation → Insights
📊 Power BI File
Contains the interactive dashboard and visual analysis.
📖 README
Documents the project, methodology, findings, and business recommendations.
🚀 Future Improvements
Possible future iterations could include:
Building a predictive campaign-response model
Testing additional segmentation techniques
Creating a dedicated SQL script
Adding automated data pipelines
Performing statistical significance testing
Building customer lifetime value analysis
Developing a campaign-response prediction dashboard
👨‍💻 Author
�

Omar Saleh
Computer Science Student | Data Analytics & Machine Learning
Building practical projects at the intersection of:
Data • Technology • Business • AI
�

�

⭐ If you found this project useful, feel free to explore the repository.
Marketing Data → Insights → Decisions
�
```
                      ▼
           BUSINESS RECOMMENDATIONS
