# Customer Segmentation: RFM Analysis

This project delivers a comprehensive **Customer Segmentation Analysis** using the **Recency-Frequency-Monetary (RFM)** model, based on transactional data from an online UK-based retail dataset (Dec 2010 – Dec 2011). The primary objective is to deeply understand customer purchasing patterns, segment customers according to value and engagement, and develop strategic insights to boost customer retention and optimize marketing initiatives.

---

## Project Objectives
- Perform detailed **Exploratory Data Analysis (EDA)** to uncover insights into sales trends, product performance, and customer behaviors.
- Calculate and analyze **RFM metrics** (Recency, Frequency, Monetary) to measure customer engagement and profitability.
- Segment customers based on RFM scoring, identifying distinct customer groups.
- Provide actionable recommendations to drive targeted marketing campaigns, enhance customer retention, and promote business growth.

---

## Dataset Overview
- **Source**: [UCI Machine Learning Repository – Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/Online+Retail)
- **Period**: 2010-12-01 to 2011-12-09
- **Transactions**: 500,000+
- **Fields**: `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`
- **Geographic Scope**: Predominantly UK, with international customers.

*Data preprocessing included duplicate removal, null-value handling, and validation using Python, with subsequent analysis in SQLite.*

---

## Exploratory Data Analysis (EDA)
### **Key Insights:**
- **Revenue Peak**: Highest in November 2011 (holiday season), with notable growth also in May & September.
- **Optimal Sales Hours**: 10 AM – 3 PM, primarily weekdays.
- **Best-selling Products**: Home décor and gift items, varying preferences across countries.
- **Market Insights**: UK contributes 82% of total revenue; notable value per customer in Netherlands & Ireland.
- **Customer Retention**: 70.8% retention over 6 months, with approximately 65% repeat buyers.

---

## RFM Model Overview
| Metric        | Description                    | Business Importance                     |
|---------------|--------------------------------|-----------------------------------------|
| **Recency**   | Days since last purchase       | Indicates customer's recent engagement   |
| **Frequency** | Number of total purchases      | Reflects customer loyalty               |
| **Monetary**  | Total spend                    | Highlights customer profitability       |

- RFM scores range from 1 to 5 for each metric (higher = better performance).
- Customer segments are based on Recency scores and the combined average of Frequency and Monetary scores.

---

## Customer Segments
| Segment               | Description                                    | Recommended Actions                  |
|-----------------------|------------------------------------------------|--------------------------------------|
| **Champions**         | High engagement & spending                     | Exclusive offers, priority rewards   |
| **Loyal Customers**   | Consistent and frequent buyers                 | Targeted upselling, loyalty programs |
| **Potential Loyalists**| Recent customers with high potential          | Personalized onboarding              |
| **At Risk**           | Valuable customers with declining activity     | Reactivation and win-back campaigns  |
| **Hibernating**       | Low activity, minimal engagement               | Targeted reactivation efforts        |

> *Complete segmentation logic and visuals available in the accompanying notebook.*

---

## Key Strategic Recommendations
- Strengthen customer retention programs targeted at **Champions**, **Loyal Customers**, and **Potential Loyalists**.
- Implement targeted reactivation campaigns for **At Risk** and **Hibernating** segments.
- Enhance customer onboarding processes for **New** and **Promising** segments with incentives and structured engagement.
- Optimize marketing schedules (peak hours: 10 AM–2 PM, weekdays) for maximum effectiveness.
- Explore and capitalize on growth opportunities in international markets (Netherlands, Ireland, France, Germany).

---

## Visualizations
- **Monthly Revenue Trends**: Seasonal patterns clearly visualized.
- **Hourly Transaction Patterns**: Ideal timing for promotional activity.
- **Top-Selling Products**: Revenue and quantity insights.
- **Geographic Revenue Distribution**: Market value mapping.
- **RFM Segment Grid & Customer Bubble Chart**: Intuitive segmentation visualization.

_Additional interactive visuals and detailed analyses are provided in the notebook._

---

## Technologies & Tools
- **Languages**: Python, SQL (SQLite)
- **Libraries**: Pandas, NumPy, Matplotlib, Seaborn, Plotly
- **Environment**: Jupyter Notebook
