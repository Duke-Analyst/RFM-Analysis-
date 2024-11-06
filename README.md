# I. Introduction
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
