📊 Marketing Campaign Performance Analysis

«An end-to-end Data Analytics portfolio project combining Python, SQL, Customer Segmentation, and Power BI.»

This project analyzes customer behavior and marketing campaign performance to identify high-value customers, response patterns, purchasing behavior, and actionable marketing opportunities.

The project follows a complete analytics workflow:

Business Understanding → Data Preparation → Data Cleaning → Exploratory Analysis → SQL Analysis → Customer Segmentation → Visualization → Business Recommendations

---

🎯 Project Overview

The main business question is:

«How can a company better understand its customers and marketing campaign performance to make more informed marketing decisions?»

The analysis focuses on:

- Customer demographics and household characteristics
- Customer spending behavior
- Purchasing channels
- Marketing campaign responses
- Previous campaign acceptance
- Customer recency and tenure
- Customer segmentation
- Factors associated with campaign responsiveness

---

📌 Business Questions

This project answers questions such as:

1. What percentage of customers responded to the latest campaign?
2. Which customer groups are more responsive?
3. How does spending differ between responders and non-responders?
4. Which purchasing channels are most active among responders?
5. Which product categories generate the highest spending?
6. Does customer recency relate to campaign response?
7. Does customer tenure relate to campaign response?
8. Can customers be segmented based on their value and purchasing behavior?
9. Which customer segment should receive greater marketing attention?
10. What business actions can be recommended from the analysis?

---

📊 Dataset

Dataset: Customer Personality Analysis

The dataset contains customer demographic, purchasing, and marketing campaign information.

Dataset characteristics

Metric| Value
Original customers| 2,240
Original columns| 29
Customers after cleaning| 2,233
Analytical columns| 33+
Missing values| Mainly "Income"
Duplicate records| 0

The dataset is used as a public-data portfolio case study.
The business scenario presented in this project is fictional and is intended to demonstrate how a Data Analyst could approach a real marketing analytics problem.

---

🛠️ Tools & Technologies

Tool| Purpose
🐍 Python| Data cleaning, exploration, analysis
🐼 Pandas| Data manipulation
🔢 NumPy| Numerical analysis
🗃️ SQL / SQLite| Business-oriented data analysis
🤖 Scikit-learn| Customer segmentation
📊 Power BI| Dashboard and visualization
📓 Jupyter / Google Colab| Analysis environment

---

🔄 Project Workflow

1. Business Understanding

The project starts by defining the business problem and translating it into measurable analytical questions.

The objective is not simply to describe the dataset, but to understand:

Customer → Behavior → Campaign Response → Segment → Business Action

---

2. Data Preparation

The original dataset was inspected to understand:

- Dataset dimensions
- Data types
- Missing values
- Duplicate records
- Categorical values
- Potential data-quality issues
- Constant columns
- Suspicious values and outliers

Initial inspection

2,240 customers × 29 columns

Only the "Income" column contained missing values, with 24 missing records.

No duplicate customer records were identified.

---

🧹 3. Data Cleaning

Several data-quality improvements were performed.

Missing Income

The 24 missing income values were replaced using the median income to avoid losing customer records.

Marital Status

Marital categories were consolidated into two analytical groups:

- Partner
- Alone

Invalid/ambiguous categories such as "YOLO" and "Absurd" were removed.

Age

Age was calculated using the dataset's reference year.

Suspicious birth-year records producing unrealistic ages were excluded through an age-quality filter.

Final analytical age range:

18–74 years

Feature Engineering

Additional analytical features were created:

- "Children"
- "Age"
- "Total_Spending"
- "Total_Purchases"
- "Family_Size"
- "Customer_Tenure_Days"
- "Customer_Segment"

Constant columns that provided no analytical value were removed from the analytical dataset.

---

🔎 4. Exploratory Data Analysis

The analysis explored relationships between customer characteristics, spending behavior, purchasing activity, and campaign response.

---

📈 Overall Campaign Performance

Metric| Result
Customers analyzed| 2,233
Responders| 332
Response Rate| 14.87%

The overall campaign response rate was approximately 14.87%.

---

💰 Spending & Campaign Response

Customer Group| Avg. Total Spending
Non-Responders| 538.49
Responders| 988.40

Responders had substantially higher average spending than non-responders.

«💡 Insight: Customers who responded to the campaign were also associated with considerably higher spending levels.»

---

🛒 Purchasing Behavior

Customer Group| Avg. Purchases
Non-Responders| 12.05
Responders| 15.36

Responders were more active across the purchasing channels represented in the dataset.

---

🧮 5. SQL Business Analysis

SQL was used to answer business questions directly from the analytical dataset.

The SQL analysis covered:

- Overall campaign response rate
- Response by education
- Response by number of children
- Spending by response
- Purchases by response
- Income by response
- Recency by response
- Channel behavior
- Previous campaign acceptance
- Product-category spending
- Customer tenure and response

This demonstrates how SQL can be used to move from raw customer records to business-focused answers.

---

🤖 6. Customer Segmentation

Customer segmentation was performed using K-Means clustering.

The segmentation features were based on:

- Income
- Recency
- Total Spending
- Total Purchases
- Web Purchases
- Catalog Purchases
- Store Purchases

Important methodological decision

Campaign response variables were not used as clustering inputs.

This avoided target leakage and ensured that customer segments were created from customer characteristics and behavior rather than from the outcome we were trying to evaluate.

---

📐 Choosing the Number of Clusters

Silhouette scores were evaluated across multiple values of K.

K| Silhouette Score
2| 0.436
3| 0.311
4| 0.247
5| 0.247
6| 0.247
7| 0.251
8| 0.248

Based on the results, K = 2 was selected.

---

👥 Customer Segments

Two practical customer segments were identified.

Segment| Customers| Share| Avg. Income| Avg. Spending| Avg. Purchases| Response Rate
Lower-Value Customers| 1,174| 52.6%| 36,530| 130.71| 6.58| 9.37%
Higher-Value Customers| 1,058| 47.4%| 69,034| 1,132.60| 19.15| 20.98%

Key segmentation finding

The Higher-Value Customers segment represents approximately 47.4% of customers, but contributes approximately 66.9% of all campaign responders.

Its response rate is approximately 2.24× higher than the Lower-Value segment.

«💡 Business implication: Higher-value customers represent a particularly important audience for targeted marketing campaigns.»

---

📅 Customer Recency

Average recency differed noticeably between responders and non-responders.

Customer Group| Avg. Recency
Non-Responders| 51.54 days
Responders| 35.41 days

Responders were associated with approximately 16 fewer days since their most recent purchase.

«💡 Insight: More recently active customers appear more responsive to the campaign.»

---

⏳ Customer Tenure

Customer tenure was also examined.

Tenure Group| Response Rate
Less than 6 months| 8.65%
6–12 months| 9.38%
1–1.5 years| 16.61%
More than 1.5 years| 26.48%

Longer-tenure customers showed higher campaign response rates in this dataset.

«⚠️ These results indicate association, not causation.»

---

🍷 Product Spending

Responders showed higher average spending across all major product categories.

The largest absolute differences were observed in:

- 🍷 Wines
- 🥩 Meat Products

These categories therefore represent potential opportunities for targeted offers and cross-selling.

---

📊 Power BI Dashboard

The final analysis was transformed into an interactive Power BI dashboard.

The dashboard brings together:

- Customer KPIs
- Response Rate
- Customer Segmentation
- Customer Distribution
- Spending by Response
- Product Spending
- Purchasing Channels
- Response by Tenure
- Response by Education

Dashboard KPIs

KPI| Value
Total Customers| 2,233
Responders| 332
Average Income| 52.21K
Average Spending| 605.38
Average Purchases| 12.54
Response Rate| 14.87%

«📌 Dashboard file: "Marketing_Campaign_Performance_Analysis.pbix"»

---

💡 Key Insights

01 — Higher-value customers matter more

Higher-value customers represent less than half of the customer base but contribute roughly two-thirds of campaign responders.

02 — Recent customers are more responsive

Responders had an average recency of 35.41 days, compared with 51.54 days among non-responders.

03 — Responders purchase more

Responders averaged 15.36 purchases, compared with 12.05 among non-responders.

04 — Responders spend considerably more

Average spending among responders was 988.40, compared with 538.49 for non-responders.

05 — Tenure is associated with response

Customers with longer tenure showed substantially higher response rates.

06 — Previous campaign engagement matters

Customers who had accepted previous campaigns showed stronger responsiveness to the current campaign.

---

🎯 Business Recommendations

Based on the analysis, a company could consider:

1. Prioritize Higher-Value Customers

Allocate greater targeting attention to customers with stronger spending and purchasing behavior.

2. Use Recency for Targeting

Recent customers may be valuable candidates for timely campaign communication and re-engagement strategies.

3. Personalize Marketing Channels

Use observed purchasing behavior to tailor communication and offers across web, catalog, and store channels.

4. Focus on High-Value Product Categories

Wines and Meat Products showed particularly strong spending differences between responders and non-responders.

5. Build Different Strategies by Segment

Instead of treating all customers equally:

Higher-Value Customers → Retention + Cross-Sell + Targeted Offers

Lower-Value Customers → Engagement + Activation + Conversion

6. Strengthen Customer Lifecycle Strategies

Newer customers may benefit from onboarding and engagement campaigns, while long-tenure customers may be suitable for loyalty-focused strategies.

«⚠️ Recommendations are based on observed associations in the dataset and should be validated through controlled marketing experiments before assuming causal effects.»

---

📁 Project Structure

marketing-campaign-performance-analysis/
│
├── Marketing_Campaign_Performance_Analysis.ipynb
├── Marketing_Campaign_Performance_Analysis.pbix
├── README.md
│
└──
    Additional SQL and project documentation

---

📚 Google Data Analytics Certificate Application

This project applies concepts covered throughout the Google Data Analytics Professional Certificate, including:

Course| Applied Concept
Foundations: Data, Data, Everywhere| Analytics workflow & role of a Data Analyst
Ask Questions to Make Data-Driven Decisions| Business questions & stakeholder thinking
Prepare Data for Exploration| Dataset understanding & preparation
Process Data from Dirty to Clean| Data cleaning & quality checks
Analyze Data to Answer Questions| EDA, statistics & insights
Share Data Through the Art of Visualization| Dashboard & data storytelling
Data Analysis with R Programming| Analytical concepts implemented in Python
Introduction to Data Analysis| End-to-end analytical workflow
Google Data Analytics Capstone| Complete portfolio project

Python instead of R

Although one course focuses on R programming, the analytical concepts were implemented using Python, Pandas, NumPy, and Scikit-learn because Python aligns with the technical direction of this portfolio.

The goal was to apply the analytical thinking and concepts, not simply reproduce the course exercises in another language.

---

🧠 What I Learned

This project helped strengthen practical skills in:

- Translating business problems into analytical questions
- Data cleaning and data-quality validation
- Exploratory Data Analysis
- Python with Pandas and NumPy
- SQL business analysis
- Customer segmentation with K-Means
- Feature engineering
- Statistical comparison
- Data visualization
- Power BI dashboard development
- Turning analytical findings into business recommendations
- Communicating insights without confusing correlation with causation

Most importantly, the project reinforced one principle:

«Data analysis is not just about finding numbers. It is about turning data into decisions.»

---

📂 Project Files

📓 Python Analysis

"Marketing_Campaign_Performance_Analysis.ipynb"

Contains the complete Python workflow including:

- Data loading
- Data inspection
- Cleaning
- Feature engineering
- EDA
- Statistical analysis
- Customer segmentation
- Business insights

📊 Power BI Dashboard

"Marketing_Campaign_Performance_Analysis.pbix"

Contains the interactive dashboard built from the cleaned analytical dataset.

---

⚠️ Project Note

This is a portfolio project based on a public customer marketing dataset.

The company/business scenario is fictional and is used only to demonstrate a realistic Data Analyst workflow.

The findings represent patterns observed in the dataset and should not be interpreted as causal conclusions without further experimentation.

---

🚀 Future Improvements

Potential next steps include:

- Adding an interactive dashboard screenshot gallery
- Extracting SQL queries into a dedicated ".sql" file
- Adding automated analysis scripts
- Building a predictive campaign-response model
- Testing campaign strategies using A/B testing concepts
- Adding customer lifetime value analysis
- Deploying selected insights through an interactive web application

---

👨‍💻 Author

Omar Saleh

Computer Science Student | Data Analytics & Machine Learning

---

⭐ If you found this project useful, feel free to explore the notebook and Power BI dashboard.
