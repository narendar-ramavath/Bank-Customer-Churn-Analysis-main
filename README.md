🏦 Bank Customer Churn Analysis

::: {align="center"}

📊 Power BI | SQL | Excel | DAX | Data Modeling

An end-to-end banking analytics project to understand customer churn,
identify high-risk segments, and support data-driven retention
strategies.






:::

📌 Table of Contents

Project Overview

Business Problem

Project Objectives

Dataset

Data Dictionary

Data Cleaning & Preparation

Data Modeling

Dashboard

Key Dashboard KPIs

Key Insights

Business Recommendations

End-to-End Data Analyst
Workflow

Tools & Technologies

Power BI Report

Project Outcome

🎯 Project Overview

The Bank Customer Churn Analysis project analyzes customer data from
a banking domain to understand why customers leave the bank and
which customer characteristics are associated with higher churn.

The project uses Power BI, SQL, and Excel to clean, model, analyze,
visualize, and communicate customer behavior.

The final dashboard helps business stakeholders:

Monitor customer churn and retention

Identify high-risk customer segments

Analyze churn by geography, gender, credit profile, activity,
products, and time

Understand customer behavior patterns

Develop targeted customer-retention strategies

Reduce potential customer-acquisition costs

🚨 Business Problem

The bank is experiencing a significant customer churn challenge.

Acquiring a new customer can require additional marketing and
operational investment. Therefore, understanding which customers are
leaving and what patterns are associated with their exits is important
for developing targeted retention strategies.

The business needs answers to questions such as:

Who is leaving?

Where is churn highest?

Which customer characteristics are associated with churn?

When are customers most likely to leave?

What actions can the bank take to improve retention?

🎯 Project Objectives

01 --- Understand Churn

Analyze customer exits and calculate important churn and retention KPIs.

02 --- Identify Risk Segments

Find customer groups with relatively higher churn based on geography,
gender, credit profile, activity, age, tenure, and product usage.

03 --- Discover Trends

Analyze customer exits across years and months to identify patterns and
changes over time.

04 --- Support Business Decisions

Convert analytical findings into practical recommendations for customer
retention.

📂 Dataset

Domain

Banking

Dataset Size

10,000 customers

Time Period

4 years

Data Formats

CSV + Excel

Dataset Files

Bank_Churn.csv
ActiveCustomer.xlsx
CreditCard.xlsx
CustomerInfo.csv
ExitCustomer.xlsx
Gender.xlsx
Geography.xlsx

📖 Data Dictionary

Column              Business Meaning

RowNumber         Record/row number; does not affect customer churn
CustomerId        Unique customer identifier
Surname           Customer surname
CreditScore       Customer credit score
Geography         Customer location
Gender            Customer gender
Age               Customer age
Tenure            Number of years the customer has been with the bank
Balance           Customer account balance
NumOfProducts     Number of banking products used
HasCrCard         Credit-card ownership indicator
IsActiveMember    Customer activity indicator
EstimatedSalary   Estimated customer salary
Exited            Customer churn indicator
Bank DOJ          Date the customer joined the bank

Credit Score Categories

Category         Score Range

🟢 Excellent        800--850
🟢 Very Good        740--799
🔵 Good             670--739
🟠 Fair             580--669
🔴 Poor             300--579

Churn Indicator

Exited = 0  →  Retained Customer
Exited = 1  →  Exited Customer

Customer Activity

IsActiveMember = 1  →  Active Member
IsActiveMember = 0  →  Inactive Member

🧹 Data Cleaning & Preparation

Before analysis, the data was prepared through the following steps:

✅ Checked for duplicate records and removed duplicates

✅ Removed irrelevant columns

✅ Standardized data types

✅ Standardized date formats

✅ Formatted numerical fields consistently

✅ Cleaned text values and special characters

✅ Handled null/missing values

✅ Prepared datasets for modeling and reporting

🧩 Data Modeling

A Star Schema approach was established between the fact table and
supporting dimension tables using Power Pivot.

Conceptual Model

                    ┌─────────────────┐
                    │    Geography    │
                    └────────┬────────┘
                             │
┌───────────────┐     ┌──────▼───────┐     ┌───────────────┐
│     Gender    │────►│  Customer /  │◄────│  Credit Card  │
└───────────────┘     │  Churn Fact  │     └───────────────┘
                      └──────┬───────┘
                             │
                    ┌────────▼────────┐
                    │ Active Customer │
                    └─────────────────┘

This structure supports interactive analysis across customer attributes,
activity, geography, credit-card status, gender, and churn.

📊 Dashboard

Dashboard --- Customer Churn Overview

The Power BI dashboard provides an executive-level view of:

Total customers

Active vs. inactive customers

Credit-card holders

Exited vs. retained customers

Customer trends by year

Monthly exit trends

Exit customers by credit type

Exit customers by customer category

Geography distribution

Gender distribution

Monthly churn percentage

🖥️ Dashboard Page 1



📈 Dashboard Page 2



📌 Key Dashboard KPIs

KPI                                       Value

👥 Total Customers                   10,000
🟢 Active Customers                   5,151
⚪ Inactive Customers                 4,849
💳 Credit Card Holders                7,055
💳 Non-Credit Card Holders            2,945
🚪 Exit Customers                     2,037
🤝 Retained Customers                 7,963
📉 Churn Rate                        20.37%
📈 Retention Rate                    79.63%
👤 Active Customer Rate              51.51%
💳 Credit Card Holder Rate           70.55%
🛒 Average Products / Customer         1.53
⏳ Average Tenure                   5 Years
🎂 Average Age                     39 Years
💰 Average Balance / Customer         ~75K

🔎 Key Insights

1. 📉 Customer Churn

The analysis reports:

10,000 total customers

2,037 exited customers

7,963 retained customers

20.37% churn rate

79.63% retention rate

The project identifies the churn level as a significant business concern
and recommends targeted retention actions.

2. 🟡 Customer Activity

The active customer rate is 51.51%.

The analysis indicates that inactive customers have a higher churn
tendency, making customer engagement an important retention area.

Business Opportunity

Increase engagement through:

Personalized communication

Relevant offers

Loyalty benefits

Customer feedback

Product education

3. 💳 Credit Card Segment

70.55% of customers are credit-card holders.

The analysis identifies notable exits among credit-card customers, with
customers in the Fair and Poor credit-score categories showing
particularly important churn patterns.

Exit Customers by Credit Type

Credit Category     Exit Customers

Fair                       685
Poor                       520
Good                       452
Very Good                  252
Excellent                  128

4. 🛒 Product Adoption

Customers use between 1 and 4 products, with an average of 1.53
products per customer.

The analysis reports higher churn among customers using fewer products.

Business Opportunity

Use customer segmentation to identify suitable:

Cross-selling opportunities

Complementary financial products

Personalized product bundles

Loyalty benefits

5. ⏳ Customer Tenure

The average customer tenure is approximately 5 years.

The analysis indicates that many customers leave around the 4--5
year tenure period.

Business Opportunity

Create proactive retention campaigns before customers reach higher-risk
tenure periods.

6. 🌍 Geography

Customer Distribution

Country        Customers        Share

🇫🇷 France      5,014   50.14%
🇩🇪 Germany     2,509   25.09%
🇪🇸 Spain       2,477   24.77%

The analysis reports Germany as the highest-churn geography at
32.44%, while France and Spain are around 16%.

Priority

Germany should be investigated further to understand the specific
drivers behind its higher churn.

7. 👥 Gender

Customer Distribution

Gender     Customers        Share

Male       5,457   54.57%
Female     4,543   45.43%

The analysis reports that female customers have a higher churn rate
than male customers, despite males representing the larger customer
base.

8. 📅 Yearly Churn

The analysis reports:

Year                             Churn Rate

2016                             19.27%
2017                             22.35%
2018     Reported in dashboard analysis
2019     Reported in dashboard analysis

Key Observation

2017 recorded the highest reported annual churn rate at 22.35%, while
2016 recorded the lowest at 19.27%.

9. 📆 Monthly Exit Pattern

The dashboard identifies:

🔴 November: highest exit count --- 307

🟢 February: lowest exit count --- 58

The analysis also reports a positive relationship between current-month
exits and previous-month exits.

10. 🔮 Churn Forecast

The project documentation includes a forecast for the next four
quarters.

The reported forecast range is approximately:

Lower Bound  → 15–16%
Upper Bound  → 24–25%
Confidence   → 95%

This forecast can help the bank prepare proactive retention strategies.

💡 Business Recommendations

01 --- Improve Customer Service

Resolve customer issues quickly and provide more personalized customer
experiences.

02 --- Introduce Loyalty Programs

Reward long-term customers with benefits designed to improve retention.

03 --- Personalize Communication

Use customer behavior and profile information to provide relevant
updates and offers.

04 --- Act on Customer Feedback

Collect customer feedback regularly and identify recurring pain points.

05 --- Increase Customer Engagement

Encourage inactive customers to use relevant banking services through
personalized campaigns.

06 --- Upselling & Cross-Selling

Recommend complementary products based on customer profiles and existing
product usage.

07 --- Customer Segmentation

Create targeted customer groups based on:

Geography
     ↓
Credit Profile
     ↓
Activity
     ↓
Products
     ↓
Tenure
     ↓
Customer Behavior

Then design retention strategies specifically for each segment.

🔄 End-to-End Data Analyst Workflow

┌──────────────────────────────┐
│  01. Requirement Gathering   │
│       BRD / FRD              │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│  02. Data Collection         │
│       CSV / Excel / DB       │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│  03. Data Cleaning           │
│       Pre-processing         │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│  04. Data Modeling           │
│       Star Schema            │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│  05. DAX Calculations        │
│       KPIs / Measures        │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│  06. Power BI Dashboard      │
│       Charts / Filters       │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│  07. Business Insights       │
│       Trends / Segments      │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│  08. Recommendations         │
│       Retention Strategy     │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│  09. Power BI Service        │
│ Publish • Refresh • RLS      │
│ Share • Alerts • App         │
└──────────────────────────────┘

🛠️ Tools & Technologies

Technology                          Usage

📊 Power BI                     Dashboard development,
visualization and reporting

🧮 DAX                          Measures and business calculations

🗄️ SQL                          Data querying and analysis

📗 Microsoft Excel              Data preparation and analysis

🔗 Power Pivot                  Data modeling

📋 Data Analyst Tasks Performed

Data & Analysis

Requirement Gathering

Data Collection

Data Cleaning

Data Pre-processing

Data Modeling

Exploratory Analysis

KPI Development

DAX Calculations

Customer Segmentation

Trend Analysis

Power BI

Report Development

Interactive Filters / Slicers

Dashboard Creation

Workspace Creation

Report Publishing

Gateway Configuration

Scheduled Refresh

Row-Level Security (RLS)

Roles

Subscriptions

Alerts

Report Sharing

Power BI App Creation

🔗 Power BI Report

📊 Report

Open Power BI Report
→

📈 Live Dashboard

Open Live Power BI Dashboard
→

🏆 Project Outcome

This project transforms raw banking customer data into a
business-focused customer churn analytics solution.

The analysis helps stakeholders understand:

👤 WHO

is leaving the bank?

🌍 WHERE

is churn concentrated?

📊 WHAT

customer characteristics are associated with higher churn?

📅 WHEN

are customer exits increasing?

💡 WHY

should the bank focus on specific customer segments?

🎯 HOW

can the bank improve retention?

💼 Portfolio Value

This project demonstrates practical Data Analyst capabilities across
the complete analytics lifecycle:

Raw Data → Cleaning → Modeling → SQL/Excel Analysis → DAX → Power BI →
Insights → Business Recommendations

It can be presented as a portfolio project for Data Analyst, Business
Analyst, Power BI Developer, and BI Analyst opportunities.

::: {align="center"}

⭐ Bank Customer Churn Analysis

Turning customer data into actionable business decisions.

Power BI • SQL • Excel • DAX • Data Analytics
:::
