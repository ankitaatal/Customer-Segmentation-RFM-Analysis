
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

## 🔗 Tags & Keywords
`#RFMAnalysis` `#CustomerSegmentation` `#Retention` `#ECommerceAnalytics` `#CLV` `#CohortAnalysis` `#Python` `#SQL`

