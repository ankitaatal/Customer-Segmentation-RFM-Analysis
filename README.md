# 🛒 RFM Analysis (Customer Segmentation)

This project implements **RFM (Recency, Frequency, Monetary)** analysis to segment customers and identify opportunities for targeted marketing campaigns. The goal is to understand customer behavior, optimize engagement strategies, and improve **Customer Lifetime Value (CLV)** and **retention** in a **global retail/e-commerce** context.

![RFM Metrics](images/RFM-Metrics.webp)

---

## 📄 Overview

**RFM Analysis** is a powerful customer segmentation technique that classifies customers based on:
- **Recency**: How recently a customer made a purchase.
- **Frequency**: How often they make purchases.
- **Monetary**: How much money they spend.

By analyzing these three metrics, businesses can:
- Identify **high-value customers**
- Design **targeted marketing campaigns**
- Increase **customer retention and loyalty**

This project applies RFM and **cohort analysis** to uncover actionable insights about customer behavior, retention trends, and acquisition strategies.

---

## 🛠 Technologies Used
- **Python**: Pandas, NumPy, Matplotlib, Seaborn, Lifetimes
- **Jupyter Notebook** 
- **SQL (SQLite)** for data querying and analysis

---

## 📂 Project Type
- Data Preprocessing & Cleaning
- Advanced Visualization Techniques
- RFM Analysis & CLV Segmentation
- Cohort Analysis
- Customer Retention & Acquisition Insights

---

## 📊 Data Description

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

📌 **Dataset Source**:  
[US Regional Sales Data](https://data.world/dataman-udit/us-regional-sales-data)

---

## ✅ Solution Approach

This project follows a structured data analytics workflow:

1. **Data Cleaning & Preprocessing**  
   - Handled missing values and outliers.
   - Converted data types and ensured data consistency.

2. **Exploratory Data Analysis (EDA)**  
   - Explored revenue trends, purchase behavior, and customer demographics.

3. **RFM Analysis**  
   - Scored and segmented customers based on recency, frequency, and monetary metrics.
   - Grouped customers into **High**, **Mid**, and **Low** value segments.

4. **Cohort Analysis**  
   - Analyzed customer retention trends over time.
   - Tracked customer lifecycle patterns and churn.

5. **Visualization & Reporting**  
   - Created heatmaps, bar charts, area charts, and bubble plots to visualize customer segments and retention insights.

---

## 📈 Key Data Insights

1. **Customer Segmentation**
   - Identified **1,306 loyal customers**, contributing significantly to monthly revenue.
   - **High-Value Customers** (Top 20%) account for a majority of revenue.
   
2. **Customer Retention**
   - Retention rates **decline sharply** after the second cohort month.
   - Highlights the need for **stronger post-onboarding engagement**.

3. **Revenue Contribution**
   - Loyal customers contribute **over 75% of total revenue**.
   - **At-risk customers** identified for re-engagement campaigns.

4. **Purchase Behavior**
   - **Higher purchasing frequency** observed on weekdays.
   - Best time to run **targeted promotions** for high engagement.

---

## 📝 Customer Segments Identified

| Segment Name       | Description                                                                               |
|--------------------|-------------------------------------------------------------------------------------------|
| **VIP Customers**       | Recent, frequent purchasers with high monetary value. Most valuable and loyal.           |
| **Regular Customers**   | Purchase frequently but with lower monetary value. Reliable and consistent buyers.       |
| **Dormant Customers**   | Have not made recent purchases but have a past purchase history. Need reactivation.     |
| **New Customers**       | Recently made their first purchase. Require nurturing and onboarding efforts.          |
| **Churned Customers**   | Previously active customers with no recent purchases. Need win-back campaigns.         |

---

## 🔑 Business Recommendations

1. **Retention Strategies**
   - Launch loyalty programs targeting **at-risk** and **VIP** segments.
   - Automate re-engagement campaigns (emails, push notifications).

2. **Acquisition Optimization**
   - Focus marketing on high-growth regions (ex: California).
   - Run **location-based promotions** in underperforming regions.

3. **Customer Experience Enhancement**
   - Collect feedback from churned and dormant customers.
   - Offer **exclusive perks** for new customers to boost early retention.

4. **Data-Driven Campaigns**
   - Leverage **RFM segmentation** for personalized offers.
   - Prioritize **high-value segments** in marketing efforts.

---

## 📚 References
- [RFM Analysis Case Study](https://statso.io/rfm-analysis-case-study/)
- [RFM Analysis Using Python](https://thecleverprogrammer.com/2023/06/12/rfm-analysis-using-python/)

---

## 🔗 Tags & Keywords
`#RFMAnalysis` `#CustomerSegmentation` `#Retention` `#ECommerceAnalytics` `#CLV` `#CohortAnalysis` `#Python` `#SQL`

