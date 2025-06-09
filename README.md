# E-commerce Customer & Sale Analysis

## 1. Project Overview

This project aims to segment customers of an online retailer into meaningful groups based on their transaction history. It primarily utilizes the classic **RFM (Recency, Frequency, Monetary) model** to quantify customer value and combines it with the **KMeans clustering algorithm** to create distinct customer profiles.

The objective is to provide data-driven support for precision marketing and refined operational strategies. This analysis helps the business identify different value-based customer groups and tailor marketing campaigns accordingly, ultimately aiming to increase Customer Lifetime Value (LTV) and overall profitability.

## 2. Data

* **Records:** 541,909
* **Key Attributes:** `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`

## 3. Tech Stack
* **Programming Language:** Python 3
* **Core Libraries:**
    * Data Processing & Analysis: `Pandas`, `NumPy`
    * Data Visualization: `Matplotlib`, `Seaborn`
    * Machine Learning: `Scikit-learn`

## 4. Analysis Workflow

The analysis for this project included the following key stages:

1.  **Data Cleaning & Preprocessing:**
    * Handled missing values.
    * Cleaned anomalous data.
    * Converted data types, especially parsing `InvoiceDate` into a datetime format.
    * Calculated the `TotalPrice` feature as a core metric for analysis.

2.  **Explotary Data Analysis:**
    * Found Top 10 popular products and their sales trends over time.
    * Identified unique buying patterns within countries.
    * Explored the impact of cancellation.

3.  **RFM Model Construction:**
    * Calculated three core metrics for each unique customer based on their transaction history:
        * **Recency (R):** The number of days since the customer's last purchase.
        * **Frequency (F):** The total number of purchases made by the customer.
        * **Monetary (M):** The total monetary value of all purchases made by the customer.

4.  **Data Transformation & Scaling:**
    * Used the `StandardScaler` to **scale the data**, eliminating the influence of different units and scales across the R, F, and M metrics.

5.  **KMeans Clustering & Modeling:**
    * Employed the **Elbow Method** and **Silhouette Score** to scientifically determine the optimal number of clusters (K).
    * Trained the KMeans algorithm on the transformed and scaled RFM data to partition customers into distinct groups.

6.  **Cluster Profiling & Interpretation:**
    * Analyzed the characteristics of each cluster by calculating the mean RFM values, which allowed for the creation of descriptive and commercially relevant personas for each group.



## 5. Key Findings & Visualization

Through modeling and analysis, customers were successfully segmented into several distinct groups with clear characteristics, such as:

* **Best Customers:** Low Recency, high Frequency & Monetary values. The core profit drivers.
* **Potential Customers / Newcomers:** Low Recency, but low Frequency & Monetary values. Key targets for growth.
* **At-Risk / Almost Lost Customers:** High Recency, but previously had high Frequency & Monetary values. Require immediate retention efforts.
* **Lost Customers:** High Recency, low Frequency & Monetary values.

![image](https://github.com/ericxq27/E-commerce-Customer-Sales-Analysis/blob/main/Images/Top%2010%20Popular%20Products%20by%20Quantity%20Sold.png)
![Monthly Sales Quantity of Top 10 Popular Products](https://github.com/ericxq27/E-commerce-Customer-Sales-Analysis/blob/main/Images/Monthly%20Sales%20Quantity%20of%20Top%2010%20Popular%20Products.png)
![Customer Segmentation based on RFM](https://github.com/ericxq27/E-commerce-Customer-Sales-Analysis/blob/main/Images/Customer%20Segmentation%20based%20on%20RFM.png)
![Kmeans Clusters](https://github.com/ericxq27/E-commerce-Customer-Sales-Analysis/blob/main/Images/Visualisation%20of%20Kmeans%20Clusters.png)
![Top 15 Countries by Sales Revenue (incl. UK)](https://github.com/ericxq27/E-commerce-Customer-Sales-Analysis/blob/main/Images/Top%2015%20Countries%20by%20Sales%20Revenue%20(incl.%20UK).png)
![Top 15 Countries by Sales Revenue (excl. UK)](https://github.com/ericxq27/E-commerce-Customer-Sales-Analysis/blob/main/Images/Top%2015%20Countries%20by%20Sales%20Revenue%20(excl.%20UK).png)
![Monthly Sales vs. Cancellations](https://github.com/ericxq27/E-commerce-Customer-Sales-Analysis/blob/main/Images/Monthly%20Sales%20vs.%20Cancellations.png)

## 6. Business Insights & Recommendations

Key Takeaways:

1. **Sales are Seasonal:** The business has a strong seasonal peak in Q4, driven by holiday shopping. This is a critical period for revenue, and marketing/inventory planning should be heavily focused here.

2. **Customer Value varies Greatly:** A core group of "Improtant" and "VIP" customers drives a significant portion of the business. Retention and engagement strategies for these segments are crucial. Conversely, "At Risk" customers present a key opportunity for re-engagement before they are lost.

3. **UK is the Core Market, Europe is the Opportunity:** While the UK is the primary market, nearby European countries like the Netherlands, Ireland, and Germany represent the biggest growth opportunities for international expansion.

4. **Cancellations are a Costly Issue:** Cancellations represent a tangible loss of revenue. A deeper dive into why orders are cancelled could lead to process improvements and cost savings.

Based on the customer segmentation results, the following targeted marketing strategies can be recommended:

* **For High-Value Customers:** Offer VIP services, exclusive discounts, and early access to new products to maintain high loyalty.
* **For Potential Customers:** Nurture their purchasing habits with welcome offers, loyalty points, and personalized recommendations to increase their frequency.
* **For At-Risk Customers:** Launch targeted re-engagement campaigns with special promotions or personalized outreach to win them back.
* **For Lost Customers:** Can be used as a sample for churn analysis to understand reasons for leaving, helping to reduce future churn.

## 7. Dashboard
![page1](https://github.com/ericxq27/E-commerce-Customer-Sales-Analysis/blob/main/Images/Dashboard-page-1.jpeg)
![page2](https://github.com/ericxq27/E-commerce-Customer-Sales-Analysis/blob/main/Images/Dashboard-page-2.jpeg)
