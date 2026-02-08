# window-function-and-joins
# STEP 1: PROBLEM DEFINITION
1.	Business context
A tech company selling electronics (smartphones, laptops, accessories) within regions of the country.

2.	Data challenge
The company stores data on customers, products and sales separately but lacks clear visibility on the following issues makes it difficult to make data driven decisions:
•	Which product performs best in each region
•	Sale growth trends trends periodically
•	High value customer segment for targeted promotion

3.	Expected outcomes
Provide analytical insights that help:
•	Identify top performing product
•	Track sales trends over time
•	Customer quartile segmentation

#STEP 2: SUCCESS CRITERIA
1.	Identify top 5 products per region using RANK ()
2.	Calculate running monthly sales totals using SUM ()
3.	Analyze monthly sales growth using LAG ()
4.	Segment customers into quartiles based on total spending using NTILE (4)
5.	Compute a 3-month moving average of sales using AVG () OVER ()

#STEP 3: DATABASE SCHEMA DESIGN
TABLES:
•	Customer: 
	customer_id (pk)
	Customer_name
	Region
	email
![image alt](https://github.com/nicoleumutoni5-crypto/PSQL_window-function-and-joins--24925-UMUTONI/blob/main/snipe%202.png)
•	products:
	product_id (pk)
	product_name
	category
	unit_price
![image alt](https://github.com/nicoleumutoni5-crypto/PSQL_window-function-and-joins--24925-UMUTONI/blob/main/SNIPE1.png)
•	sales:
	sale_id(pK)
	customer_id
	product_id
	sale_date
	quantity
	amount
![image alt](https://github.com/nicoleumutoni5-crypto/PSQL_window-function-and-joins--24925-UMUTONI/blob/main/SNIPE%203.png)
# ER DIAGRAM
![image alt](https://github.com/nicoleumutoni5-crypto/PSQL_window-function-and-joins--24925-UMUTONI/blob/main/Screenshot%202026-02-08%20180225.png)
#Step 4: SQL JOINS implementation
1.	INNER JOIN
Retrieve transactions with valid customers and products
![image alt](
