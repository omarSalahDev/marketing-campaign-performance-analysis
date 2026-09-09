📊 Marketing Campaign Performance Analysis

End-to-End Data Analytics Project | Python • SQL • Customer Segmentation • Power BI

«Turning customer and marketing data into actionable business insights.»

---

🚀 Project Overview

This project presents an end-to-end marketing analytics workflow designed to understand customer behavior, evaluate campaign response, identify valuable customer segments, and translate analytical findings into actionable business recommendations.

The project follows the core Data Analytics lifecycle:

Ask → Prepare → Process → Analyze → Share → Act

Using Python, SQL, Machine Learning-based Customer Segmentation, and Power BI, the analysis transforms raw customer data into insights that can support better marketing decisions.

«📌 Project Type: Portfolio / Case Study
📂 Dataset: Customer Personality Analysis — Kaggle
🏢 Business Scenario: Fictional marketing case based on public data»

---

🎯 Business Problem

A company has customer-level data covering:

- Customer demographics
- Product spending
- Purchase channels
- Previous campaign responses
- Website activity
- Customer tenure
- Household characteristics

The business wants to understand:

«Which customers are more likely to respond to marketing campaigns, what behavioral patterns are associated with response, and how can these insights improve marketing decisions?»

---

❓ Business Questions

The analysis focuses on the following questions:

1. What is the overall campaign response rate?
2. Which customer characteristics are associated with higher response?
3. How does customer spending differ between responders and non-responders?
4. Which purchasing channels show the strongest engagement?
5. Which product categories generate the highest spending?
6. Does customer recency relate to campaign response?
7. Does customer tenure relate to campaign response?
8. Can customers be segmented based on their value and purchasing behavior?
9. Which customer segment represents the strongest marketing opportunity?
10. How can these findings be translated into actionable recommendations?

---

🛠️ Tech Stack

Area| Tools
Programming| Python
Data Manipulation| Pandas, NumPy
Statistical Analysis| Python / Descriptive Statistics
Business Analysis| SQL / SQLite
Customer Segmentation| Scikit-learn / K-Means
Visualization| Matplotlib, Seaborn
Dashboard| Microsoft Power BI
Development| Google Colab / Jupyter Notebook
Documentation| GitHub Markdown

---

🔄 Project Workflow

Business Problem
       ↓
Data Preparation
       ↓
Data Cleaning
       ↓
Exploratory Data Analysis
       ↓
SQL Business Analysis
       ↓
Customer Segmentation
       ↓
Insight Generation
       ↓
Power BI Dashboard
       ↓
Business Recommendations

---

📂 Dataset

The project uses the Customer Personality Analysis dataset from Kaggle.

Dataset Size

Metric| Value
Original Customers| 2,240
Original Columns| 29
Customers After Cleaning| 2,233
Analytical Columns| 33+

The dataset contains information about:

- Customer demographics
- Income
- Family structure
- Product spending
- Purchase behavior
- Marketing campaign responses
- Website activity
- Customer registration date

---

🧹 Data Preparation & Cleaning

The dataset was systematically inspected and prepared before analysis.

Data Quality Checks

The following checks were performed:

- Dataset dimensions
- Missing values
- Duplicate records
- Data types
- Unique customer IDs
- Categorical values
- Suspicious age values
- Extreme income values
- Constant columns

Key Cleaning Steps

1. Missing Income Values

Only 24 Income values were missing.

Instead of removing these customers, missing income values were replaced using the median income to minimize the effect of extreme values.

2. Marital Status Standardization

Marital status categories were consolidated into two analytical groups:

- Partner
- Alone

Invalid / extremely rare categories were removed.

3. Age Validation

Suspicious birth-year records were identified.

An "Age" feature was created and customers with implausible ages were excluded from the final analytical dataset.

4. Feature Engineering

Several analytical features were created:

Children
Age
Total_Spending
Total_Purchases
Family_Size
Customer_Tenure_Days
Customer_Segment

5. Constant Columns

Columns containing no analytical variation, such as "Z_CostContact" and "Z_Revenue", were excluded from the analytical copy of the dataset.

---

📊 Exploratory Data Analysis

The exploratory analysis examined customer demographics, spending behavior, purchasing activity, campaign response, and engagement patterns.

---

📈 Overall Campaign Performance

After cleaning:

KPI| Result
Total Customers| 2,233
Responders| 332
Response Rate| 14.87%
Average Income| 52.21K
Average Spending| 605.38
Average Purchases| 12.54

The campaign response rate was approximately 14.87% across the analyzed customer base.

---

💰 Spending & Campaign Response

One of the strongest patterns observed was the difference in spending behavior between responders and non-responders.

Customer Group| Avg. Spending
Responders| 988.40
Non-Responders| 538.49

Responders spent substantially more on average than non-responders.

This pattern suggests that higher-value customers were also more responsive to the campaign within this dataset.

«⚠️ This is an observed association, not evidence that higher spending causes campaign response.»

---

🛒 Purchasing Behavior

Responders also showed higher purchasing activity:

Customer Group| Avg. Purchases
Responders| 15.36
Non-Responders| 12.05

Responders were more active across:

- Web purchases
- Catalog purchases
- Store purchases

The largest absolute difference was observed in catalog purchasing activity.

---

🍷 Product Spending Analysis

Responders spent more across all six product categories.

The largest absolute differences were observed in:

Product Category| Non-Responders| Responders
Wines| 269.11| 503.34
Meat Products| 144.41| 295.60
Gold Products| 40.84| 60.95
Fish Products| 34.90| 51.71
Sweet Products| 25.06| 38.67
Fruits| 24.16| 38.12

Wines and Meat Products therefore represent particularly important categories for understanding customer value and potential cross-selling opportunities.

---

🎓 Response by Education

Campaign response varied across education groups.

Education| Response Rate
PhD| 20.70%
Master| 15.45%
Graduation| 13.41%
2n Cycle| 10.95%
Basic| 3.70%

The highest observed response rate was among customers with a PhD, while the lowest was among the Basic education group.

---

👨‍👩‍👧 Response by Number of Children

Children| Response Rate
0| 26.46%
1| 10.23%
2| 11.16%
3| 3.77%

Customers with no children showed the highest observed response rate in this dataset.

---

⏱️ Customer Recency

Recency showed one of the clearest behavioral differences.

Customer Group| Avg. Recency
Responders| 35.41 days
Non-Responders| 51.54 days

Responders had purchased more recently on average.

Key Observation

«More recent customer activity was associated with higher campaign response.»

This makes recency a potentially useful variable for customer targeting and re-engagement strategies.

---

🗓️ Customer Tenure

Customer tenure was calculated from the customer registration date.

Customer Group| Avg. Tenure
Responders| 446.62 days
Non-Responders| 337.29 days

Response rate also increased across tenure groups:

Tenure Group| Response Rate
Less than 6 months| 8.65%
6–12 months| 9.38%
1–1.5 years| 16.61%
More than 1.5 years| 26.48%

Longer-tenure customers showed a higher observed response rate.

---

🧮 SQL Business Analysis

SQL was used to answer business questions directly from the analytical dataset.

The SQL analysis covered:

- Overall campaign response
- Response by education
- Response by number of children
- Spending comparison
- Purchase behavior
- Income comparison
- Customer recency
- Purchase channels
- Previous campaign acceptance
- Product category spending
- Customer tenure

This demonstrated how SQL can be used not only for data retrieval, but also for business-oriented analytical questions.

---

👥 Customer Segmentation

To move beyond descriptive analysis, customers were segmented according to their behavioral and financial characteristics.

Segmentation Features

The clustering model used:

Income
Recency
Total_Spending
Total_Purchases
NumWebPurchases
NumCatalogPurchases
NumStorePurchases

Method

K-Means Clustering was evaluated using different values of K.

K| Silhouette Score
2| 0.436
3| 0.311
4| 0.247
5| 0.247
6| 0.247
7| 0.251
8| 0.248

Based on the results, K = 2 provided the strongest clustering quality.

---

💎 Customer Segments

The final segmentation identified two main customer groups.

Segment| Customers| Avg. Income| Avg. Spending| Avg. Purchases| Response Rate
Higher-Value Customers| 1,058| 69,033.82| 1,132.60| 19.15| 20.98%
Lower-Value Customers| 1,174| 36,530.38| 130.71| 6.58| 9.37%

Segment Highlights

The Higher-Value Customers segment:

- Represents 47.4% of customers.
- Represents 66.87% of all responders.
- Has a response rate of 20.98%.
- Has approximately 2.24× the response rate of the Lower-Value segment.
- Has substantially higher spending and purchasing activity.

---

⚠️ Outlier Handling

One customer had an income value of 666,666, which was identified as a potentially suspicious extreme value.

The customer was not globally deleted from the project.

Instead:

- The record remained in the main analytical dataset.
- It was excluded specifically from K-Means segmentation.
- This prevented the extreme value from disproportionately affecting customer clusters.

This approach preserves the original data while protecting the segmentation analysis from distortion.

---

🔐 Avoiding Target Leakage

For customer segmentation, the following campaign-response variables were not used as clustering inputs:

Response
AcceptedCmp1
AcceptedCmp2
AcceptedCmp3
AcceptedCmp4
AcceptedCmp5

These variables were instead used after segmentation to evaluate how responsive each customer segment was.

This prevents the clustering model from being built using the outcome it is later evaluated against.

---

📊 Power BI Dashboard

The final analysis was transformed into an interactive Power BI dashboard.

Dashboard Includes

- Total Customers
- Responders
- Average Income
- Average Spending
- Average Purchases
- Overall Response Rate
- Response Rate by Customer Segment
- Customer Distribution by Segment
- Spending by Response
- Product Spending by Response
- Purchases by Channel
- Response Rate by Tenure
- Response Rate by Education

Dashboard Goal

The dashboard brings together the most important findings into a single decision-oriented view, allowing stakeholders to quickly understand:

«Who the customers are → How they behave → Who responds → Where the opportunity is»

📌 Dashboard preview:
An image of the final Power BI dashboard will be added here.

---

💡 Key Insights

01 — Higher-value customers are more responsive

Higher-Value Customers represent 47.4% of the customer base, but account for 66.87% of responders.

Their response rate is 20.98%, compared with 9.37% for Lower-Value Customers.

---

02 — Recent customers show stronger response

Responders had an average recency of 35.41 days, compared with 51.54 days among non-responders.

---

03 — Responders purchase more

Responders averaged 15.36 purchases, compared with 12.05 among non-responders.

---

04 — Responders spend significantly more

Average spending was:

988.40 vs 538.49

for responders and non-responders respectively.

---

05 — Longer-tenure customers show stronger response

Customers with more than 1.5 years of tenure had a 26.48% response rate, compared with 8.65% among customers with less than 6 months.

---

06 — Wines and Meat are important categories

These categories showed the largest absolute spending differences between responders and non-responders.

---

🎯 Business Recommendations

Based on the observed patterns:

1. Prioritize Higher-Value Customers

Use the Higher-Value segment as a priority audience for targeted campaigns because it shows stronger engagement and campaign response.

2. Use Recency for Targeting

Customers with more recent purchasing activity may represent stronger opportunities for campaign engagement.

3. Personalize Marketing Channels

Use customers' observed purchasing behavior to determine the most appropriate communication and sales channels.

4. Leverage High-Value Product Categories

Wines and Meat Products can be considered for targeted offers, bundles, and cross-selling strategies.

5. Strengthen Customer Retention

Longer-tenure customers showed higher response rates, suggesting an opportunity to build loyalty strategies while improving engagement among newer customers.

«Important: These recommendations are based on observed associations in the dataset and should be validated through controlled campaigns or A/B testing before being treated as causal effects.»

---

🎓 Google Data Analytics Professional Certificate

This project was designed to apply concepts learned throughout the Google Data Analytics Professional Certificate.

Course| Application in This Project
1. Foundations: Data, Data, Everywhere| Data analytics lifecycle and analyst mindset
2. Ask Questions to Make Data-Driven Decisions| Business problem and analytical questions
3. Prepare Data for Exploration| Dataset understanding and data preparation
4. Process Data from Dirty to Clean| Cleaning, validation, missing values and transformations
5. Analyze Data to Answer Questions| EDA, statistics, SQL and pattern discovery
6. Share Data Through the Art of Visualization| Power BI dashboard and data storytelling
7. Data Analysis with R Programming| Analytical concepts applied using Python instead of R
8. Google Advanced Data Analytics / Introduction to Data Analysis| Advanced analytical workflow and segmentation
9. Google Data Analytics Capstone| End-to-end portfolio case study

«🐍 Note: The project uses Python instead of R, while applying the relevant analytical concepts learned from the R-focused coursework.»

---

🧠 What I Learned

Through this project, I strengthened my ability to:

- Translate business problems into analytical questions.
- Prepare and clean real-world datasets.
- Identify and handle data-quality issues.
- Perform exploratory data analysis.
- Use SQL for business analysis.
- Engineer meaningful analytical features.
- Apply customer segmentation using K-Means.
- Evaluate clustering quality using Silhouette Score.
- Avoid target leakage during segmentation.
- Build decision-oriented Power BI dashboards.
- Communicate analytical findings through business recommendations.

Most importantly:

«Data analysis is not just about finding numbers. It is about turning data into evidence that supports better decisions.»

---

📁 Project Structure

marketing-campaign-performance-analysis/
│
├── 📄 README.md
│
├── 📓 Marketing_Campaign_Performance_Analysis.ipynb
│
├── 📊 Marketing_Campaign_Performance_Analysis.pbix
│
├── 📄 marketing_campaign_powerbi.csv
│
├── 📂 images/
│   └── dashboard-preview.png
│
└── 📄 requirements.txt

---

📌 Project Files

📓 Jupyter Notebook

Contains the complete Python workflow:

- Data preparation
- Cleaning
- EDA
- Feature engineering
- Statistical analysis
- Customer segmentation

🗄️ SQL Analysis

Contains the SQL business queries used to answer analytical questions.

📊 Power BI Dashboard

Interactive dashboard containing the project's final KPIs, comparisons, and insights.

📄 Processed Dataset

Cleaned analytical dataset prepared specifically for the Power BI dashboard.

---

🔮 Future Improvements

Possible next steps include:

- Build a campaign response prediction model.
- Test additional clustering techniques.
- Perform deeper cohort analysis.
- Add customer lifetime value analysis.
- Run A/B testing simulations.
- Build automated dashboard refresh workflows.
- Develop a more advanced marketing recommendation system.

---

⚠️ Project Disclaimer

This is a portfolio case study based on a publicly available dataset.

The business scenario, stakeholders, and recommendations are presented for analytical and educational purposes and do not represent an actual company's internal marketing data.

All findings should therefore be interpreted within the context and limitations of the dataset.

---

👨‍💻 Author

Omar Saleh

Computer Science Student | Data Analytics & Machine Learning

Interested in:

Data Analytics • Python • SQL • Machine Learning • Data Visualization

---

⭐ If you found this project useful, feel free to explore the notebook and dashboard.

Built as part of my journey toward becoming a Data Analyst.
