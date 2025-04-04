# Python_RFM_Analysis
# **1. Project Introduction**

## **Company Background**

**Real Canadian Superstore** is a major Canadian supermarket chain operated by **Loblaw Companies Limited**, one of the largest food and pharmacy retailers in Canada. The chain functions as a **hypermarket**, offering a wide selection of both **groceries** and **general merchandise**, including:

- **Groceries:** Fresh produce, meat, dairy, seafood, frozen foods, and baked goods
- **General Merchandise:** Clothing (notably under the Joe Fresh brand), home goods, electronics, and personal care items
- **Private Label Products:** Notably under Loblaw’s own brands such as *President’s Choice* and *No Name*
- **Services:** Pharmacy, photo lab, gas stations (e.g., Mobil), fitness centers, and in-store medical clinics

## **Business Challenge**

With the approach of the holiday season (Christmas and New Year), the **Marketing Department** wants to launch targeted campaigns to:

- **Show appreciation** to long-time loyal customers
- **Engage and nurture potential customers** who have shown interest but haven’t yet become loyal customers

The **Marketing Director proposed using the RFM model** to segment the customer base based on purchase behavior to support this effort. The goal is to make data-driven decisions that increase customer retention and loyalty.

## **Why Use RFM Analysis?**

**RFM (Recency, Frequency, Monetary)** analysis is a customer segmentation technique used to:

- **Recency (R):** Measures how recently a customer made a purchase
- **Frequency (F):** Measures how often they purchase
- **Monetary (M):** Measures how much money they have spent

In this project, we narrowed our focus to:

- **Loyal Customers:** Highly engaged and valuable, perfect for thank-you campaigns and loyalty rewards
- **Potential Customers:** Show promise but need nurturing—ideal for upselling, retargeting, and onboarding
- **Non-loyal Customers:** Inconsistent or low engagement—can be reactivated with win-back or reminder campaigns

# **2. Dataset Overview**

The dataset used in this project is an **e-commerce retail transaction dataset**, which includes detailed records of customer purchases. It contains:

- **Transactional-level data**, with each row representing a single item purchase
- **Key fields include:**
    - `InvoiceNo`: Unique identifier for each transaction
    - `InvoiceDate`: Date and time of the transaction
    - `CustomerID`: Anonymized ID of the customer
    - `Quantity`: Number of items purchased
    - `UnitPrice`: Price per item
    - `Country`: Country where the transaction occurred
    - `Description`: Product name

From this dataset, an **Invoice Summary table** was created to calculate:

- **Recency**: Days since the customer’s last purchase
- **Frequency**: Total number of unique transactions
- **Monetary**: Average order value per customer

These RFM values were then used to segment customers and generate actionable business insights.

# 3. EDA

### Data Exploration

![Screenshot 2025-04-04 at 4.04.57 pm.png](attachment:91a1b0b9-5586-4a14-9336-24706a9eb3c1:Screenshot_2025-04-04_at_4.04.57_pm.png)

![Screenshot 2025-04-04 at 4.05.22 pm.png](attachment:4a0af577-1d6e-4d1f-a9b4-a780e6fa5f40:Screenshot_2025-04-04_at_4.05.22_pm.png)

![Screenshot 2025-04-04 at 4.05.36 pm.png](attachment:7abaed8e-5d36-4fea-9e7e-441a420dd146:Screenshot_2025-04-04_at_4.05.36_pm.png)

### **Check missing values**

![Screenshot 2025-04-04 at 4.07.45 pm.png](attachment:0342d395-a558-47e4-800a-f96d12c394cf:Screenshot_2025-04-04_at_4.07.45_pm.png)

![Screenshot 2025-04-04 at 4.08.13 pm.png](attachment:11f54358-dcb3-4a39-82f3-03a80c833aef:ca850485-a6d8-4339-8db3-4407f4400ee6.png)

![Screenshot 2025-04-04 at 4.08.46 pm.png](attachment:37e2038a-2870-4003-9b8a-c4ef9c2b3fce:3f5c15cf-8745-47c1-aa77-9ed526cb1c07.png)

### Handle missing values

![Screenshot 2025-04-04 at 4.09.22 pm.png](attachment:516814b2-2e6e-4b96-956c-2bea59d2983f:Screenshot_2025-04-04_at_4.09.22_pm.png)

### **Check duplicate values**

![Screenshot 2025-04-04 at 4.10.34 pm.png](attachment:92ddbf6a-b895-4c57-b959-51af1f0f8586:Screenshot_2025-04-04_at_4.10.34_pm.png)

![Screenshot 2025-04-04 at 4.10.53 pm.png](attachment:3ae6af9a-6c7a-4e49-8a2b-33c7944c5e43:Screenshot_2025-04-04_at_4.10.53_pm.png)

# **4. Data Processing**

### Invoice Summary Table

![Screenshot 2025-04-04 at 4.13.34 pm.png](attachment:0b925839-8f4d-4d89-b88c-c9e9a73e8ea1:Screenshot_2025-04-04_at_4.13.34_pm.png)

### RFM

![Screenshot 2025-04-04 at 4.14.45 pm.png](attachment:47e66859-8dab-451f-ad35-c9ed666ad92a:Screenshot_2025-04-04_at_4.14.45_pm.png)

![Screenshot 2025-04-04 at 4.15.14 pm.png](attachment:48087bb0-f152-4707-841c-11f9b998a2c7:Screenshot_2025-04-04_at_4.15.14_pm.png)

![Screenshot 2025-04-04 at 4.15.31 pm.png](attachment:f31b0646-6f27-4711-923b-bc09d8fb1f9f:Screenshot_2025-04-04_at_4.15.31_pm.png)

### Customer Segmentation Information

![Screenshot 2025-04-04 at 4.17.18 pm.png](attachment:d347b6aa-2373-4f40-b966-c7d5db140da8:Screenshot_2025-04-04_at_4.17.18_pm.png)

# **5. Visualization**

![Screenshot 2025-04-04 at 4.18.40 pm.png](attachment:6a77d754-8b17-438c-9c8f-e41f5e72f826:Screenshot_2025-04-04_at_4.18.40_pm.png)

- Potential Loyalists make up the largest customer group. These are customers who have purchased recently and frequently buy. => Recommend: marketing campaigns, such as personalized promotions or loyalty incentives, to encourage repeat purchases with higher average transaction value them into Loyal or Champion customers.
- Champions and Loyal segments already represent engaged and high-value customers. => Recommendation: Launching appreciation campaigns (e.g., exclusive offers, thank-you emails) will help strengthen relationships and retain them long term.
- At-risk customers are the second largest group. => Recommendation: Reactivation campaigns (e.g., win-back discounts or reminders) can prevent them from dropping into Lost.

![Screenshot 2025-04-04 at 4.19.32 pm.png](attachment:6f203deb-bccd-44c0-97a3-c673405c7484:Screenshot_2025-04-04_at_4.19.32_pm.png)

**Loyal customers:**

- Highest median
- Wider IQR => more variation in how much they spend
- Extreme outliers — some customers spend significantly more

**Potential Loyalists:**

- Lowest median and smaller spread
- Narrow box => low consistency in spending

**Non-loyal customers:**

- Lower median than Loyal
- Moderate variability, but some spend a decent amount

![Screenshot 2025-04-04 at 4.20.13 pm.png](attachment:2aea7112-821c-40ec-80cd-c67f3c7889c1:Screenshot_2025-04-04_at_4.20.13_pm.png)

- The majority of potential customers placed their second order within the first 30 days after the first one => strong early engagement.
- After 50 days, there is a sharp drop in follow-up orders, with frequency continuing to decline steadily over time.
- A long tail exists where some customers take more than 6 months to make their second purchase.

**Actions:** Target potential loyal customers with follow-up campaigns or promotions within the first 30 days and some vouchers to increase the chances of converting them into loyal buyers.

![Screenshot 2025-04-04 at 4.20.52 pm.png](attachment:d1afc0eb-61a8-4238-90f2-b59638a03327:Screenshot_2025-04-04_at_4.20.52_pm.png)

- Loyal customers also tend to make their second purchase very quickly, with most of them doing so within 30 days.
- Only a small portion delayed their second order beyond 150 days, which suggests these are less consistent or slower repeaters.

**Actions:** Launching thank-you campaigns, early-access deals, or loyalty points programs right after the first order.

![Screenshot 2025-04-04 at 4.21.37 pm.png](attachment:8c6b438b-9c30-425d-a23f-069d5c93bdb4:Screenshot_2025-04-04_at_4.21.37_pm.png)

As we can see, the UK has a much larger number of customers in each category compared to other countries. Therefore, it's hard to evaluate.

![Screenshot 2025-04-04 at 4.22.18 pm.png](attachment:45c10fc3-b7a8-43b4-8be7-6821d9aa8579:Screenshot_2025-04-04_at_4.22.18_pm.png)

Loyal Customers:

- 100% in Iceland, Singapore
- High in EIRE, Marta, Norway

Non-loyal:

- 100% in Brazil, Czech, Greece, Isarel
- High in Austria, Denmark, Italy, Japan

Potential:

- High in Sweden, UK, Spain, Netherlands

**Actions:** Conduct proper campaigns in each country to target suitable types of consumers

**Primary focus:** R (Recency) Since if a customer hasn’t purchased recently, they may be at risk of churn — so reactivation should be a priority.

# 6. Project Summary

Using a real-world e-commerce retail dataset, I preprocessed transactional data to calculate RFM scores for each customer. These scores were then translated into behavioral segments to support marketing decisions, particularly during the holiday season.

The insights generated from the segmentation were used to:

- **Recognize and reward Loyal customers** with appreciation campaigns
- **Target Potential Loyalists** with nurturing strategies
- **Re-engage Non-loyal customers** through personalized outreach

Through data analysis and visualization (bar plots, histograms, stacked charts, and FacetGrids), this project demonstrates how data-driven segmentation can enhance customer retention, improve campaign efficiency, and increase long-term customer value in a retail context.
