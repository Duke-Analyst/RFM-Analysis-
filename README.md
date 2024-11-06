# Introduction
As the holiday season approaches, the Marketing Department is preparing a series of campaigns to express appreciation to our customers. In addition, the Marketing Director has proposed using the RFM model to segment our customers. This model will help us identify valuable customer segments, particularly those with high potential to become long-term, loyal customers.

## 1. What is the RFM model
In RFM analysis, customers are scored based on three factors (Recency - Frequency - Monetary), then labeled based on the combination of RFM scores.
- Recency (R): How recently customers made a purchase.
- Frequency (F): How often customers make purchases.
- Monetary (M): How much customers spend.

This model could be very useful, especially for small and medium-sized enterprises (SMEs) with limited marketing resources, helping them focus on the potentially right customer segments to increase ROI, reduce churn, reduce cost, improve customer relationships, and a lot more.


## 2. Dataset
This is a transnational dataset, which contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail. The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.
![image](https://github.com/user-attachments/assets/006a1006-3ad7-4159-915c-5ee09128df9d)

- InvoiceNo: Invoice number. Nominal, a 6-digit integral number uniquely assigned to each transaction. If this code starts with the letter 'C', it indicates a cancellation.
- StockCode: Product (item) code. Nominal, a 5-digit integral number uniquely assigned to each distinct product.
- Description: Product (item) name. Nominal.
- Quantity: The quantities of each product (item) per transaction. Numeric.
- InvoiceDate: Invoice Date and time. Numeric, the day and time when each transaction was generated.
- UnitPrice: Unit price. Numeric, Product price per unit in sterling.
- CustomerID: Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer.
- Country: Country name. Nominal, the name of the country where each customer resides.

### My project has 2 parts:
- Part 1: Data processing with Python (including EDA, Wrangling data, and visualization)
- Part 2: Customers Analysis
  
# Part 1: Data processing with Python 
You can check it out at this link: 
https://colab.research.google.com/drive/1FXAO1v8xRu49wbNgPDl74wr00Xph-3rV#scrollTo=tz-eDxEJsJ_8

After data processing, I created a customer segmentation table: 
![image](https://github.com/user-attachments/assets/e5166fda-d54f-4641-a6bc-c4c9e85ddd90)

This is the segmentation criteria table, which the Marketing Department provided
![image](https://github.com/user-attachments/assets/af247523-202b-4ab0-8ec7-061777ed8b25)

# Part 2: Customers Analysis 
## I. Overview
### 1. Recency (Purchase frequency based on time):
- The purchase frequency is calculated from the last time a customer made a purchase (the last day a - CustomerID generated an order).
- Data: The earliest date a CustomerID order appears is 01/12/2010, and the calculation date for the Recency score is 12/31/2011.

Observing the chart, we can see:
![image](https://github.com/user-attachments/assets/90ee6315-d17b-4713-90b2-ecded48ce1cf)

- There are two peaks with the highest number of Customer IDs, both under 50 days (<2 months). This indicates that the company has a large number of customers who have purchased recently.

- The number of customers who have purchased recently is 1,629 (accounting for 37%). The portion of customers whose last purchase was over 50 days ago makes up 63% of the company's total customer base.![image](https://github.com/user-attachments/assets/f1fb468f-996a-465e-961e-49e473c13fe3)

**Suggestion**: A campaign is needed to attract former customers to return.

### 2. Frequency (Number of orders a customer has placed):
Observing the chart, we can see:
![image](https://github.com/user-attachments/assets/93f451f3-c1c7-418c-b509-9e8d1a321cc1)

- The majority of customers have very low purchase frequency.
- Zooming into the left side of the chart (for customers with fewer than 10 orders): most of the company’s customers place between 1-5 orders in a year. This may stem from the nature of the company’s products or a lack of customer retention strategies.
![image](https://github.com/user-attachments/assets/90d20e75-9c47-4cd5-90a9-1921f5a7056e)


**Suggestion**: Find out the main reason and take appropriate action

### 3. Monetary (Spending value):
![image](https://github.com/user-attachments/assets/a5029360-ee6e-469b-9cf6-fec4233ec6f6)

- The distribution of Monetary values is highly skewed, with most customers having low spending amounts, while a small number of customers have very high spending.

- Zooming in, we can see: the number of customers spending less than $5,000 is 4,065 (94% of the total customer base). Among them, customers spending less than $1,000 make up 2,675 (over 60% of the total number of customers).

- This indicates that the company’s revenue mainly comes from a customer segment with low spending (<$1,000).
![image](https://github.com/user-attachments/assets/7650dec2-c055-4d22-adae-5cd30ff95d6f)


## II. Segment Analysis
### 1. Segment by Customer
![image](https://github.com/user-attachments/assets/c9125a41-12f3-42e4-82e3-9805736fb91e)

- Champions (19.23%) is the largest segment. These are likely customers who have purchased recently, frequently, and have a high monetary value. This customer group needs to be carefully nurtured.

- Loyal Customers (9.82%) and Potential Loyalists (9.47%) represent an important part of the customer base and have the potential to convert into Champions with the right engagement strategies.

- Hibernating customers (15.98%) and At-Risk (9.75%) indicate a significant portion of customers who have not interacted for a long time. They purchased frequently before but have not recently engaged. Strategies could include nurturing the "At-Risk" and "Hibernating" customers to re-engage them and prevent churn.

- Lost Customers (11.18%) & New Customers (6.18%) represent a small but important group. Promotional campaigns could be launched to improve these two customer segments.

### 2. Segment by Total Sales
- Champions (62.92%) account for the majority of total sales, contributing primarily to revenue. This aligns with their high frequency and monetary value.

- Loyal Customers (11.43%) also contribute significantly to sales, followed by At-Risk (8.45%) and Need Attention (5.26%).

- Lost Customers (1.09%), Hibernating Customers (3.18%), and New Customers (0.67%) contribute very little to total sales.

## Recommendation
- Customer Retention: Launch targeted re-engagement campaigns for inactive customers to reduce churn and boost revenue.

- Champion Loyalty: Focus on retaining Champions, who contribute most of the revenue, with exclusive support and offers.

- Increase Low-Spender Value: Encourage higher spending among low-spending customers through bundle deals and loyalty discounts.

- Develop Loyalty Pipeline: Incentivize Loyal and Potential Loyalist segments to nurture them into future Champions.

- Revive At-Risk and Hibernating Customers: Use personalized campaigns to win back these segments and recover potential lost revenue.
