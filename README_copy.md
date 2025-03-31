
![RFM Metrics](images/RFM-Metrics.webp)

---

## 📄 Overview

**RFM Analysis** is a powerful customer segmentation technique that classifies customers based on:
---
| **RFM Component** | **What it Measures**            | **Why It Is Important**                                                                                           |
|------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **Recency (R)**   | Days since the last purchase    | Helps identify how recently a customer has interacted with the business, indicating their current level of engagement. |
| **Frequency (F)** | Number of purchases              | Reveals how often a customer makes purchases, reflecting their loyalty and long-term relationship with the brand.       |
| **Monetary (M)**  | Total money spent                | Shows how much revenue a customer generates, helping identify high-value and profitable customers.                      |

---

By analyzing these three metrics, businesses can:
- Identify **high-value customers**
- Design **targeted marketing campaigns**
- Increase **customer retention and loyalty**

📌 **Dataset Source**:  
[US Regional Sales Data](https://data.world/dataman-udit/us-regional-sales-data)

# Customer Segmentation - RFM Analysis

This project presents an in-depth analysis of an online UK-based retail dataset using **Recency-Frequency-Monetary (RFM)** modeling and various customer behavior analytics to uncover insights and opportunities for business growth.

## Project Objective
The aim of this project is to:
- Identify **profitable customer segments** using RFM analysis.
- Analyze **retention**, **churn**, **acquisition**, and customer behavior.
- Reveal **behavioral trends**, **purchase patterns**, and **regional performance**.
- Offer actionable **business recommendations** to improve marketing and retention strategies.

## Project Overview
This project includes:
- Data preprocessing and cleaning using **SQLite & Python**
- RFM scoring and customer segmentation
- Time-based analysis by **month, hour, and weekday**
- Visualizations using **Seaborn**, **Matplotlib**, and **Plotly**

## Dataset Description
- **Time Range**: December 2010 to December 2011
- **Transactions**: ~50,000
- **Columns**:
| Column Name  | Description                                           |
|--------------|-------------------------------------------------------|
| InvoiceNo    | Invoice number (6 digits). 'C' prefix indicates cancellation. |
| StockCode    | Product code (5 digits).                              |
| Description  | Product name.                                         |
| Quantity     | Quantity of each product per transaction.             |
| InvoiceDate  | Date and time of transaction generation.              |
| UnitPrice    | Price per unit of product.                            |
| CustomerID   | Unique customer identifier (5 digits).               |
| Country      | Country where the customer resides.                   |

## Customer Segments
---
| S. No | **Customer Segment**       | Description                                                                 | Marketing Action & Recommendations | **R Score** | **(F+M)/2 Score** |  
|------|----------------------------|---------------------------------------------------------------------------|----------------------------------|------------|-----------------|  
| 1    | <span style="color:#339AF0;">**Champions**</span>             | Most loyal and valuable customers who frequently purchase and engage with your brand. | Introduce new and upcoming products and drops. Reward them and help them share updates. Provide priority access and loyalty perks. | 5          | 4 - 5        |  
| 2    | <span style="color:#DA77F2;">**Potential Loyalists**</span>   | Customers with growing interest and engagement, indicating potential loyalty. | Offer membership/loyalty programs, recommend other products, nurture with personalized offers and incentives. | 4 - 5      | 2 - 3        |  
| 3    | <span style="color:#91A7FF;">**Loyal Customers**</span>       | Regular customers who consistently engage with and purchase from your brand. | Upsell higher-value products, ask for reviews, maintain engagement with personalized communication and loyalty programs. | 3 - 4      | 4 - 5        |  
| 4    | <span style="color:#0CA678;">**New Customers**</span>      | First-time buyers who recently started engaging with your brand. | Provide onboarding support, give them early success, start building a relationship with welcome emails and special offers. | 5          | 1            |  
| 5    | <span style="color:#38D9A9;">**Promising**</span>             | New or occasional customers with good potential based on recent behavior. | Encourage further engagement with special offers, tailored content, or invitations to loyalty programs. Check on their need for replenishment. | 4          | 1            |  
| 6    | <span style="color:#FFA8A8;">**Needs Attention**</span>       | Customers with decent engagement but show early signs of decreasing interest or activity. | Make limited-time offers, recommend products based on past purchases, re-engage with personalized outreach. | 3          | 3            |  
| 7    | <span style="color:#FAB005;">**About to Sleep**</span>        | Customers who have purchased before but have shown declining engagement or inactivity. | Send personalized re-engagement campaigns, offer discounts or reminders about their previous activity. Introduce them to new products. | 3          | 1 - 2        |  
| 8    | <span style="color:#E03131;">**Can't Lose Them**</span>       | High-value customers with recent inactivity or signs of disengagement. | Provide VIP treatment, personalized outreach, exclusive offers, and reconnect with high-value incentives. | 1 - 2      | 5            |  
| 9    | <span style="color:#F76707;">**At Risk**</span>               | Customers with reduced frequency of purchase or engagement, indicating potential churn. | Send personalized emails to reconnect, offer renewals, provide helpful resources, and recommend popular products. | 1 - 2      | 3 - 4        |  
| 10   | <span style="color:#757575;">**Hibernating**</span>           | Customers who were once active but have not engaged in a significant period. | Offer other relevant products and special discounts. Recreate brand value and reactivate through targeted campaigns. | 1 - 2      | 1 - 2        |

---


## 📎 Sample Image
![RFM Metrics](RFM-Metrics.webp)



---

## 🔍 Dataset Overview

- **Source**: UCI Machine Learning Repository  
- **Scope**: 500K+ transactions from 2010-12-01 to 2011-12-09  
- **Attributes**: InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country  

---

## ⚙️ Tools & Technologies

- **Languages**: Python, SQL (SQLite)
- **Libraries**: Pandas, NumPy, Matplotlib, Seaborn, Plotly
- **Environment**: Jupyter Notebook
- **Database**: SQLite for structured querying

---

## 🔬 Exploratory Data Analysis (EDA)

### ✅ Highlights:
- **Total Revenue**: £8.74M  
- **Unique Customers**: 4,334  
- **Average Order Value**: £474.80  
- **Sales Patterns**:
  - **Peak Sales Hours**: 10 AM – 2 PM (67.7% of transactions)
  - **Peak Days**: Thursday and Friday
- **Revenue Peaks**: March, May, September, and November 2011  
- **Product Insights**:
  - Top product: *"PAPER CRAFT, LITTLE BIRDIE"* (£168K)
  - Strong demand for **home décor** and **gift items**
- **Country Insights**:
  - **UK** dominates (82% revenue)
  - **Netherlands**, **Ireland**, **Germany**, and **France** are high-value markets

*See `/figures/` for all visuals.*

---

## 🧠 RFM Analysis & Segmentation

RFM scores are calculated and assigned to customers using a scale of 1–5:
- **Recency**: Days since last purchase (lower = better)
- **Frequency**: Number of purchases (higher = better)
- **Monetary**: Total spend (higher = better)

### 🎯 Customer Segments
| Segment             | Description                                     | Example Actions                           |
|---------------------|--------------------------------------------------|--------------------------------------------|
| **Champions**       | Highly loyal and valuable                       | VIP perks, early access, new launches      |
| **Loyal Customers** | Consistent, engaged buyers                      | Upsell, loyalty rewards                    |
| **Potential Loyalists** | Recent buyers with growth potential        | Personalized onboarding                    |
| **At Risk**         | Formerly active, now inactive                   | Win-back campaigns, exclusive discounts    |
| **Hibernating**     | Long inactive with low value                   | Reactivation emails                        |

> See full segment logic and scoring in the notebook.

---

## 📈 Visual Highlights

- 📦 **Distribution of RFM metrics**
- 📊 **RFM boxplot by segment**
- 🔥 **Customer heatmaps by Recency, Frequency, and Monetary**
- 🧩 **Segment map by Recency & FM scores**
- 🧮 **Revenue trends by segment**
- 🫧 **Segment bubble plot (Recency vs Frequency, size = customer count)**

*All visualizations are available in `/figures` or embedded inside the notebook.*

---

## 💡 Key Insights & Recommendations

- Focus retention on **Champions**, **Loyal**, and **Can’t Lose Them** segments through VIP offers and personalized outreach.
- Reactivate **At Risk** and **Hibernating** customers using targeted campaigns and reminders.
- Strengthen onboarding journeys for **New** and **Promising** customers with incentives and guided engagement.
- Leverage peak hours and days (10 AM–2 PM, Tue–Thu) for email campaigns, flash sales, and retargeting.
- Explore international growth opportunities in **Netherlands, Ireland, France**, and **Germany**.

---

## 🚀 Future Enhancements

- Build predictive models for churn and lifetime value.
- Integrate cohort analysis and CLTV forecasting.
- Deploy as a dashboard with filters by segment/country.

---

## 📌 How to Run

1. Clone the repository
2. Ensure Python & SQLite are installed
3. Install dependencies:

## 🔗 Tags & Keywords




# 🛍️ Customer Segmentation – RFM Analysis

This project performs detailed customer segmentation using **Recency, Frequency, and Monetary (RFM) analysis** on transactional data from a UK-based online retail store. The goal is to identify high-value customer groups, analyze purchasing behavior, and provide actionable business insights for improving customer engagement, retention, and marketing strategies.

---

## 📌 Project Objectives

- Analyze customer purchasing behavior using RFM metrics.
- Segment customers based on engagement and value.
- Identify high-value, at-risk, and inactive customers.
- Recommend marketing strategies tailored to each segment.
- Visualize key patterns in sales, segments, and customer dynamics.

---

## 📊 What is RFM Analysis?

| RFM Component | What it Measures              | Why It’s Important |
|---------------|-------------------------------|--------------------|
| **Recency (R)** | How recently a customer made a purchase | Indicates engagement and likelihood of reactivation |
| **Frequency (F)** | How often a customer purchases | Reflects loyalty and purchasing consistency |
| **Monetary (M)** | How much a customer spends | Helps identify high-revenue contributors |

Each customer is scored from 1–5 for each metric, with **5 being the best**. These scores are then combined to assign customers into segments such as *Champions*, *Loyal Customers*, *At Risk*, *New Customers*, etc.

---

## 📦 Dataset Overview

- **Source**: [UCI Machine Learning Repository – Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/Online+Retail)
- **Country**: Primarily United Kingdom with international customers
- **Time Period**: December 2010 to December 2011
- **Rows**: ~50,000 cleaned transactions
- **Key Features**: `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`

> Data was cleaned using Python and loaded into an SQLite database for efficient querying.

---

## 🧪 Methodology

### 🔹 1. Data Preprocessing
- Removed nulls and invalid records
- Calculated `Total Sales = Quantity × Unit Price`
- Split `InvoiceDate` into date and time
- Loaded into SQLite for SQL-based exploration and analysis

### 🔹 2. Exploratory Data Analysis (EDA)
- Key Performance Metrics (Total Revenue, AOV, Customers)
- Revenue Trends over Time
- Sales Patterns by Day and Hour
- Product Performance Analysis
- Customer Profitability by Country
- Retention, Churn & Acquisition Trends

### 🔹 3. RFM Analysis & Segmentation
- Calculated RFM metrics per customer
- Scored customers from 1 to 5 using quantiles
- Assigned each customer to a behavioral segment
- Built visualizations: distributions, heatmaps, score grids, and segment maps

---

## 🧠 Key Insights & Highlights

> A full [Insights & Recommendations](#) section is provided in the report.

- **Champions** (589 customers) contributed nearly **£4.5M+** revenue with high frequency and engagement.
- **Loyal Customers** and **Potential Loyalists** show strong growth potential with tailored communication.
- **At Risk** and **Can’t Lose Them** are high-value customers with recent inactivity — requiring recovery strategies.
- Mid-day (10AM–2PM) and mid-week (Tue–Thu) drive the most sales — ideal for targeted promotions.
- UK dominates the customer base, but countries like Netherlands and Ireland generate high revenue per customer.
- Seasonal spikes in November suggest opportunities for planned holiday campaigns and follow-ups.

---

## 📈 Tools & Technologies

- **Python** (Pandas, NumPy, Seaborn, Matplotlib, Plotly)
- **SQL** (SQLite, complex queries, views)
- **Jupyter Notebook**
- **Data Visualization** (Interactive + Static)
- **EDA + Customer Segmentation + RFM Modeling**

---

# 🛍️ Customer Segmentation – RFM Analysis

This project performs detailed customer segmentation using **Recency, Frequency, and Monetary (RFM)** analysis on transactional data from an online UK-based retail store. The goal is to identify high-value customers, understand behavior patterns, and enable personalized marketing strategies that enhance customer retention, loyalty, and revenue growth.

---

## 📌 Project Objectives

- Segment customers based on RFM metrics to uncover key behavioral patterns.
- Understand sales activity by time, day, product, and region.
- Identify valuable customer groups and churn risks.
- Generate actionable marketing and retention strategies.

---

## 🗂️ Dataset

- **Source**: UCI Online Retail Dataset  
- **Period**: December 2010 to December 2011  
- **Customers**: 4,334  
- **Transactions**: 18,402  
- **Revenue**: £8.74M  
- **Format**: Cleaned and loaded into an SQLite database for analysis.

---

## 🧰 Tools & Technologies

- **Language**: Python  
- **Database**: SQLite (via `sqlite3`)  
- **Visualization**: Matplotlib, Seaborn, Plotly  
- **Notebook Environment**: Jupyter Notebook  

---

## 🔎 Project Structure


---

## 📊 Key Analysis Sections

### 1. Exploratory Data Analysis (EDA)
- Sales trends over time (monthly revenue, MoM growth)
- Sales activity by hour and weekday
- Product performance
- Regional profitability
- Customer retention, frequency, and acquisition trends

### 2. RFM Analysis
- Calculation and distribution of Recency, Frequency, and Monetary metrics
- RFM scoring and customer segmentation
- Segment-wise performance analysis
- Heatmaps and score grids for deep dive

---

## 💡 Insights & Recommendations

> A few highlights from the analysis:

- **Champions** (589 customers) contributed over **£4.46M** in revenue. These should be nurtured with loyalty rewards and early product access.
- **Loyal Customers** and **Potential Loyalists** show consistent engagement—ideal for upselling and membership campaigns.
- **Hibernating** and **At Risk** customers represent re-engagement opportunities with targeted offers.
- **New Customers** show promising early behavior and should be guided through the customer journey.

🎯 **Actionable Strategy**: Prioritize retention of high-value segments, re-engage dormant users with tailored campaigns, and focus acquisition in profitable geographies (e.g., Netherlands, Ireland, Germany).

---

## 📌 Sample Visualizations

Here are some recommended visuals to include:

### 📈 Revenue Trends Over Time  
_A line chart showing month-wise revenue and growth._

### ⏰ Purchases by Time of Day  
_A bar chart highlighting peak shopping hours (10 AM–2 PM)._

### 📦 Top Products by Revenue & Quantity  
_Compare revenue drivers with volume movers._

### 🌍 Revenue Distribution by Country  
_An interactive choropleth showing global sales contribution._

### 🧱 RFM Segment Heatmap  
_Showing segment concentration across Recency and Frequency/Monetary scores._

### 🫧 Customer Segment Bubble Chart  
_A beautiful summary of all segments on a 2D axis, with size and color for customer count and monetary value._

---

# 🧠 Customer Segmentation using RFM Analysis

This project analyzes one year of transactional data from a UK-based online retail store to uncover meaningful customer segments using **RFM (Recency, Frequency, Monetary)** analysis. The goal is to identify key customer groups, understand behavioral trends, and provide actionable insights for improving customer retention, targeting, and profitability.

---

## 📦 Dataset Overview

- **Source**: UK Online Retail Data (2010-12 to 2011-12)
- **Transactions**: 18,402 unique invoices
- **Customers**: 4,334 unique customers
- **Revenue**: £8.74 million
- **Data Columns**: Invoice No, Date, Customer ID, Product Description, Quantity, Unit Price, Country, Total Sales
- **Preprocessing**:
  - Cleaned using Python (removal of duplicates, nulls, and invalid records)
  - Stored in a structured **SQLite database** for analysis

---

## 🔍 Project Objectives

- Explore purchasing patterns across time, geography, and products
- Measure customer engagement and value using RFM scores
- Group customers into actionable segments
- Recommend data-driven marketing and retention strategies

---

## 🧪 Technologies Used

- **Python**: Data cleaning, analysis, visualizations
- **SQLite**: SQL-based data querying and RFM logic
- **Matplotlib / Seaborn / Plotly**: Static and interactive visualizations
- **Jupyter Notebook**: Workflow management and documentation

---

## 📊 Exploratory Data Analysis (EDA)

A comprehensive analysis was performed covering:

1. **Key Performance Indicators (KPIs)**  
2. **Revenue Trends Over Time**  
3. **Sales Activity by Time and Day**  
4. **Product Performance Analysis**  
5. **Customer Profitability by Country**  
6. **Customer Retention & Churn**  
7. **Customer Purchase Frequency**  
8. **Customer Acquisition Trends**

> 📌 [Click here to see EDA summaries](#)

---

## 🧮 RFM Analysis

### RFM Metrics

| Metric     | Description                                |
|------------|--------------------------------------------|
| Recency    | Days since the last purchase               |
| Frequency  | Number of unique purchase occasions        |
| Monetary   | Total spending across all purchases        |

- Each customer received an **RFM score (1 to 5)** based on quantiles
- Scores were then combined into meaningful **customer segments**

---

## 🧩 Customer Segments

| Segment             | Description                                  | Action Recommendation |
|---------------------|----------------------------------------------|------------------------|
| **Champions**        | Most active & high-spending customers       | Priority access, rewards |
| **Loyal Customers**  | Frequent buyers with consistent value       | Upsell, loyalty programs |
| **Potential Loyalists** | New but promising customers            | Nurture & retain        |
| **At Risk**          | High value, no recent activity              | Personalized win-backs |
| **Hibernating**      | Inactive low-spend customers                | Reactivation campaigns  |
| *(+ more)*           | ...                                          | ...                    |

> 📌 Full segmentation logic and visuals included in the notebook

---

## 📈 Visualizations

- Distribution plots for Recency, Frequency, and Monetary
- Segment-wise **RFM score boxplots**
- Segment performance tables
- Comparative **heatmaps** of RFM values
- **Customer density heatmaps** by score
- Segment-wise revenue trends and contributions
- Bubble charts of segment behavior and value

---

## 💡 Insights & Recommendations

> 🚀 All insights are backed by quantitative metrics and visual analysis.

- **Champions (13% of customers)** generated over **50% of revenue**. Focus on retention through VIP offers and early access.
- **At Risk** and **Can’t Lose Them** are high-value but inactive. Prioritize with win-back strategies.
- **Hibernating** and **About to Sleep** form a large base with low engagement. Launch personalized reactivation campaigns.
- **New & Promising Customers** need onboarding support and offers to build loyalty.
- **Netherlands, Ireland, and Australia** have high revenue per customer. Explore these markets further.

---

## 🗂️ Project Structure



## ✅ How to Run

```bash
# Clone the repository
git clone https://github.com/your-username/customer-segmentation-rfm.git
cd customer-segmentation-rfm

# Install requirements
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook

---

## 🖼️ Recommended Visuals to Include in README

1. **Monthly Revenue Trend (Line Chart)** – shows seasonal impact.
2. **Purchases by Hour of Day (Bar Chart)** – for timing-based targeting.
3. **Top Products (Bar or Scatter)** – revenue vs quantity.
4. **Revenue by Country (Choropleth)** – highlights geographic value.
5. **RFM Segment Grid (`fig-rfm5`)** – shows where segments cluster.
6. **Customer Bubble Chart (`fig-rfm7`)** – intuitive and visually striking summary.
7. *(Optional)* Interactive `rfm6` or `rfm7` can be linked if hosted.

Let me know if you'd like help exporting figures into `/figures/` and embedding a few into the Markdown!



## 📁 Project Structure

```bash
customer-segmentation-rfm/
│
├── data/
│   └── online_retail_cleaned.csv
├── notebooks/
│   ├── 01_data_preprocessing.ipynb
│   ├── 02_eda_analysis.ipynb
│   └── 03_rfm_segmentation.ipynb
├── figures/
│   └── rfm1.png, rfm2.png, rfm6.html, ...
├── README.md
└── requirements.txt

`#RFMAnalysis` `#CustomerSegmentation` `#Retention` `#ECommerceAnalytics` `#CLV` `#CohortAnalysis` `#Python` `#SQL`

