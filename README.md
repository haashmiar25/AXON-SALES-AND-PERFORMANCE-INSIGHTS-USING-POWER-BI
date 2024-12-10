
AXON SALES AND PERFORMANCE INSIGHTS


PROBLEM STATEMENT:
A small company, “Axon”, which is a retailer selling classic cars, is facing issues in managing and analyzing their sales data. The sales team is struggling to make sense of the data and they do not have a centralized system to manage and analyze the data. The management is unable to get accurate and up-to-date sales reports, which is affecting the decision-making process.

AIM:
The goal of the project is to design and implement a BI solution using PowerBI and SQL that can help the company manage and analyze their sales data effectively.

DATABASE DESCRIPTION:
The dataset contains data from 06-01-2003 to 31-05-2005.
•	Customers – Holds basic information about the customers.
•	Employees – Holds information about all employees in the company.
•	Offices- Holds information about the different office locations.
•	Order details – Holds information about quantity and price of products in the orders.
•	Orders – Holds information about the shipping status of the orders.
•	Payments – Holds information about the payment amount made by customers.
•	Product Lines –Contains detailed description of the product lines.
•	Products – Holds information about the vendor prices and stock details.

ETL Steps in PowerBI:
The MySQL database was connected to PowerBI and basic data transformation steps like Removal of unwanted columns, Removal of duplicates, Removal of Null values were performed.

Calculated columns Added:
•	Table : Orderdetails
Columns added: costAmount, billAmount, profit, MSRPAmount, MRP_Profit
•	Table : Orders
Columns added: DaystoShip
•	Table : products
Columns added: Discount, stock_range 

Measures Added:
•	Total_sales : summation of the billAmount column
•	Stock_range :  Value given based on the stock quantity (Low, Good and High)
•	lastQuarter,Q0Q%,currentYTD : Time series analysis of sales for each quarter

Data Visualization:

Key Performance Indicators:

*	TOTAL SALES: 9.6M
Calculated by finding the sum of the custom column “billAmount” in the orderdetails table, where the bill amount was calculated as the product of the columns “quantityordered” and “priceeach”.

*	TOTAL PROFIT: 3.9M
Calculated as the sum of the custom column “profit” in the orderdetails table, where the profit column was calculated as the difference between the “billAmount” and the “costAmount” columns.

*	MAXIMUM ACHIEVABLE PROFIT : 4.9M
Calculated as the sum of the custom column “MRP_Profit”, which is the profit that would have been achieved had the products been sold at MRP suggested by vendors.

Insights from the Analysis:

Overview:
*	The company has a total of 7 offices in different locations, of which the office at “Paris” has made the maximum sales.
*	The company offers a vast range of 110 products procured from 13 vendors.
*	A total of 312 orders were taken up by the company of which 303 orders were successfully shipped, very few orders are in the status disputed which can be ignored.
*	On average the company takes up to 4 days to ship the products.
*	The company made a total Profit of 3.9M with total sale of 9.6M.
*	The company has 23 employees in total

 

*	The employee Gerard working at the location “Paris” is the star performer. He has performed consistently and has contributed to the maximum of the profit achieved. Employee training programs can be conducted by the top performing sales executives to enhance the performance of the company.

 
Analysis on Profit: 
*	The productline “Classic Cars” has made the highest profit among all productlines.
*	The maximum achievable profit for the sale made so far was 4.9M; initiatives can be done to minimize the difference of 1 million.
*	The top 5 products which made the highest profits are as follows:
 

*	The top five vendors that contribute to the highest profit are as follows:
  ![image](https://github.com/user-attachments/assets/994809e0-a75d-4ad1-af5f-2f6896be8c95)

 
Sales Summary
	The sales have gone up significantly in the month of November in both 2003 and 2004.
	Maximum orders were received in the month of November.
	When analysing sales across different customer locations it was found that the cities Madrid and SanRafael have the highest sales volume followed by NYC.
 

	 The product,”1969 Dodge Charger” remained highest sold product consistently so far.
	The customers “Euro + Shopping Channel” and “Mini Gifts Distributors Ltd” have consistently placed huge amount of orders so far and therefore enjoy very high creditlimits offered by the company.
	The country with maximum sales volume is USA, in which the most ordered productlines are Classic Cars and Vintage Cars.
	The sales in first quarter have gone up relatively over the years.
	The QoQ sales analysis reveals that the sales are very high during the third quarter.
	Most of the vendors have a fairly high amount of stock, very few vendors namely “Autoart Studio Design” and “Highway 66 Mini Classics” have very less stock of few products which has to be noted.
	The vendors offering maximum discount in buy price are “Autoart Studio Design”,” Studio M Art Models” which have a range of 8 products each. Procurement from these vendors could result in higher profit margins.
 
Recommendations
	So far, the company has a stronghold in USA and European countries like France and Spain. Conducting market research on favourable products in other countries and   focussing on them could result in increase in sales in the other countries as well.
	Maximum profit could be achieved if the products were sold more close to the MSRP rate suggested by the vendors.

