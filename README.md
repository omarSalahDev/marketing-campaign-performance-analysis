Marketing Campaign Performance Analysis

An end-to-end data analytics project focused on understanding customer behavior, marketing campaign response, and customer segments to support better marketing decisions.

The project follows a complete analytics workflow:

Business Problem → Data Preparation → Cleaning → Exploration → SQL Analysis → Customer Segmentation → Power BI Dashboard → Insights → Recommendations

---

Project Overview

Marketing teams collect large amounts of customer and campaign data, but the real challenge is turning that data into useful decisions.

In this project, I worked with the Customer Personality Analysis dataset to answer a practical business question:

«How can a company understand its customers and marketing campaign performance to make better marketing decisions?»

Rather than focusing only on creating charts, I treated the dataset as a real analytics problem — starting with data quality and business questions, then moving through analysis and segmentation before building the final dashboard.

The project was also used as a practical way to apply the concepts covered throughout the Google Data Analytics Professional Certificate, using Python instead of R for the programming and analysis work.

---

Business Questions

The analysis focused on questions such as:

- What percentage of customers responded to the latest campaign?
- Which customer groups are more likely to respond?
- How does customer value relate to campaign response?
- Do recent customers respond differently from less-recent customers?
- Which product categories generate the highest spending?
- Which purchasing channels are used most by responders?
- Does customer tenure appear to be associated with campaign response?
- Can customers be segmented based on their behavior and value?
- Which segments should marketing teams prioritize?

---

Dataset

The project uses the Customer Personality Analysis dataset containing customer demographics, purchasing behavior, campaign responses, and channel activity.

The original dataset contains:

- 2,240 customers
- 29 variables

Main areas of the dataset include:

- Customer demographics
- Income and household information
- Product spending
- Web, catalog, and store purchases
- Previous campaign acceptance
- Current campaign response
- Customer enrollment date

The dataset was used as a portfolio analysis scenario rather than representing a specific real company.

---

Tools & Technologies

Area| Tools
Data Cleaning & Analysis| Python, Pandas, NumPy
Statistical / Exploratory Analysis| Pandas, Matplotlib
Business Analysis| SQL, SQLite
Customer Segmentation| Scikit-learn, K-Means, StandardScaler
Dashboard & Visualization| Microsoft Power BI
Development Environment| Google Colab, Jupyter Notebook
Version Control| GitHub

---

Project Workflow

1. Business Understanding

I started by defining the business problem and identifying the questions that the analysis should answer.

The goal was not simply to describe the dataset, but to understand which customer characteristics and behaviors are associated with campaign response.

---

2. Data Preparation & Quality Checks

Before analyzing the data, I inspected its structure and quality.

The initial dataset contained:

- 2,240 rows
- 29 columns
- 24 missing values in "Income"
- No duplicate records

I also checked categorical values, data types, unique customer IDs, and suspicious values.

---

3. Data Cleaning

Several data-quality decisions were made during the preparation stage.

Missing Income

Only "Income" contained missing values.

The missing values were handled using median imputation because income contains high-value observations and the median is less sensitive to extreme values than the mean.

Marital Status

The original marital-status categories were consolidated into two broader groups:

- "Partner"
- "Alone"

Rare invalid categories such as "YOLO" and "Absurd" were removed.

Age

The dataset contained suspicious birth years, including values from the 1800s.

Instead of manually changing those records, I calculated age using the dataset's 2014 reference year and removed observations with an age of 100 or above.

After cleaning:

2,233 customers remained.

Additional Features

I created several analytical features:

- "Age"
- "Children"
- "Family_Size"
- "Total_Spending"
- "Total_Purchases"
- "Customer_Tenure_Days"

Constant columns that provided no analytical value were also removed from the final analytical dataset.

---

Exploratory Analysis

The exploratory analysis was used to understand customer behavior before moving into predictive or segmentation techniques.

Some important findings included:

Campaign Response

Out of 2,233 cleaned customers:

- 332 responded
- 1,901 did not respond
- Overall response rate: 14.87%

Spending & Response

Customers who responded to the campaign had considerably higher average spending:

Group| Avg. Spending
Responders| 988.40
Non-responders| 538.49

This indicates a strong association between customer spending and campaign response.

Recency

Responders had an average recency of approximately:

35.41 days

compared with:

51.54 days

for non-responders.

This suggests that customers with more recent purchasing activity were more responsive.

Product Categories

Responders spent more across every analyzed product category.

The largest absolute differences were observed in:

- Wines
- Meat Products

These categories therefore became important candidates for targeted marketing analysis.

---

SQL Business Analysis

SQL was used to answer business questions directly from the cleaned analytical dataset.

Examples included:

- Overall campaign response rate
- Response rate by education
- Response rate by number of children
- Spending comparison between responders and non-responders
- Purchase behavior by response
- Income comparison
- Recency comparison
- Purchasing-channel analysis
- Previous campaign acceptance
- Product-category performance
- Response rate by customer tenure

Customer Tenure Analysis

One particularly useful finding was the relationship between customer tenure and campaign response.

Tenure Group| Response Rate
Less than 6 months| 8.65%
6–12 months| 9.38%
1–1.5 years| 16.61%
More than 1.5 years| 26.48%

Longer-tenure customers showed substantially higher response rates in this dataset.

---

Customer Segmentation

To move beyond simple descriptive analysis, I created behavioral customer segments using K-Means clustering.

The segmentation used:

- Income
- Recency
- Total Spending
- Total Purchases
- Web Purchases
- Catalog Purchases
- Store Purchases

Importantly, campaign response variables were not used as clustering inputs.

This avoided target leakage and allowed the segments to be evaluated against campaign response afterward.

Choosing the Number of Clusters

I compared multiple K-Means configurations using silhouette scores.

The best result was obtained with:

K = 2

with a silhouette score of approximately 0.436.

---

Customer Segments

The resulting segments were interpreted based on their behavioral profiles.

Higher-Value Customers

1,058 customers — 47.4% of the dataset

Average profile:

- Income: 69,033.82
- Spending: 1,132.60
- Purchases: 19.15
- Campaign response rate: 20.98%

Lower-Value Customers

1,174 customers — 52.6% of the dataset

Average profile:

- Income: 36,530.38
- Spending: 130.71
- Purchases: 6.58
- Campaign response rate: 9.37%

Segment-Level Campaign Response

The higher-value segment represented approximately 47.4% of customers but 66.9% of all campaign responders.

Its response rate was also approximately 2.24× higher than the lower-value segment.

This makes customer value an important factor for campaign prioritization in this dataset.

---

Key Insights

1. Higher-value customers are more responsive

The higher-value segment showed a 20.98% response rate compared with 9.37% for the lower-value segment.

This suggests that campaign targeting could benefit from prioritizing customers who already demonstrate stronger purchasing behavior.

2. Recent activity is associated with higher response

Responders had significantly lower recency values than non-responders.

This suggests that recent customer activity can be useful when building campaign targeting rules.

3. Responders are more active across purchasing channels

Responders generally had higher purchasing activity across:

- Web
- Catalog
- Store

The largest absolute difference was observed in catalog purchases.

4. Wines and meat products stand out

Responders spent more across all product categories, with wines and meat products showing the largest absolute spending differences.

These categories could be considered when designing targeted offers or cross-selling strategies.

5. Customer tenure matters

Customers with longer relationships with the company showed higher campaign response rates.

Customers with more than 1.5 years of tenure had a response rate of 26.48%, compared with 8.65% among customers with less than 6 months of tenure.

---

Business Recommendations

Based on the analysis, I would recommend:

Prioritize higher-value customers

Use behavioral segmentation to identify customers with stronger purchasing activity and prioritize them for targeted campaigns.

Use recency as a targeting signal

Customers with more recent activity may be more receptive to marketing campaigns, making recency a useful targeting feature.

Personalize campaigns by behavior

Different customers interact with the company through different channels. Campaign strategies should therefore consider observed purchasing behavior rather than treating all customers the same.

Consider product preferences

Wines and meat products showed particularly large spending differences between responders and non-responders, making them potential categories for targeted offers.

Build different strategies for new and established customers

Longer-tenure customers showed stronger campaign response, while newer customers may benefit from onboarding and engagement strategies.

«These findings represent associations observed in the dataset and should not be interpreted as proof of causation.»

---

Power BI Dashboard

The final analysis was transformed into an interactive Power BI dashboard combining customer overview, campaign response, segmentation, purchasing behavior, product performance, education, and customer tenure.

The dashboard includes:

- Total Customers
- Responders
- Average Income
- Average Spending
- Average Purchases
- Overall Response Rate
- Response Rate by Customer Segment
- Customer Distribution by Segment
- Spending by Campaign Response
- Product Spending by Response
- Purchases by Channel and Response
- Response Rate by Tenure
- Response Rate by Education

The dashboard was designed to move from high-level KPIs → customer segmentation → behavioral analysis → actionable insights.

---

Google Data Analytics Certificate Application

This project was also my practical application of the concepts covered throughout the Google Data Analytics Professional Certificate.

Course| Applied Concept
Foundations: Data, Data, Everywhere| Analytics workflow and data mindset
Ask Questions to Make Data-Driven Decisions| Business questions and stakeholder thinking
Prepare Data for Exploration| Dataset understanding and preparation
Process Data from Dirty to Clean| Data cleaning and quality checks
Analyze Data to Answer Questions| EDA, statistics, and relationships
Share Data Through the Art of Visualization| Power BI dashboard and storytelling
Data Analysis with R Programming| Analytical programming concepts implemented with Python
Introduction to Data Analysis| End-to-end analytical workflow
Google Data Analytics Capstone| Complete project from problem to recommendations

The goal was not to force every technique from the certificate into one project, but to apply the relevant analytical concepts in a realistic workflow.

---

Project Files

marketing-campaign-performance-analysis/
│
├── Marketing_Campaign_Performance_Analysis.ipynb
├── Marketing_Campaign_Performance_Analysis.pbix
└── README.md

Additional SQL and documentation files may be added as the project is further organized.

---

Important Note

This is a portfolio project based on a publicly available customer marketing dataset.

The business scenario, questions, recommendations, and dashboard interpretation are part of the analytical exercise and do not represent analysis performed for the original dataset owner.

---

What I Learned

The biggest lesson from this project was that data analysis is not mainly about knowing more tools.

The tools helped me execute the work, but the real challenge was deciding:

What question should I ask?

What should I trust in the data?

What should I clean or investigate?

What does the result actually mean for a business?

And what decision could be made from it?

That shift — from simply working with data to thinking with data — was the most valuable part of this project.
