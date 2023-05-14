## SHIPPING COMPANY SALES REPORT
## INTRODUCTION
This is a sales report of a leading shipping company with a global presence that deals with sales and shippment of seven (7) products such as cars, motorcycles, trucks and buses, planes, ships and trains. The products are in vaious sizes (small, medium and large). Their customers are located in nineteen (19) countries belonging to four (4) regions across the world. The company hopes to use the Data to improve its sales performance across the various countries of operation. This dataset was sourced from Kaggle.

## Project goal
To provide actionable information from extracted data to improve company’s sales and customer performance.

## Project Tools/Skills
### SQL 
#### Data manipulation 
•	Views
•	CTE
•	Windows Functions
•	Query.
### PowerBI
#### Data Manipulation
•	Power Query editor
•	DAX functions (CALCULATE, AVERAGE, SUM etc)
•	Measures
•	Data-Modeling (star schema)
•	New Tables
#### Data Visualization

## Project Problems
•	What is the sales performance over the years?

•	How many customers do we have each year?

•	How many of the product sizes are typically in an order? Are there any bestsellers?

•	Are there any product-type or size to take off the market, or any promotions we could leverage?

•	Reasons for the drastic reduction in 2005 sales?
## Data Summary
Initially, the information was stored in one table. Four (4) dimensional tables (DimOrders, DimCustomer DimSales, DimProduct), and one (1) fact (Product_info) table were created from the dataset in Power query editor. 
A date table (DimDate) was also created with CALENDAR function {DimDates = CALENDARAUTO(12)}

![cars table](https://github.com/DeesAnalytics/Shipping-Agency/assets/124782621/e1eac500-bfce-4d7d-bc62-81f56e8d2bf6)

## Data Transformation
### PowerBI
The data set was transformed with Power Query editor in PowerBI. The columns whose data-type did not match with the description of the column were changed. The five (5) null values in Postal-code column was replaced with a unique value (555NP). The relationship between the dimensional tables and fact table were established in the model view through the keys.

The following inconsistencies was noticed;

•	The quantity and price value of some products did not correspond to the values in the Sales column.

•	The days, months and quarter columns are not present.

A custom sales column was created by multiplying the quantity column by price column.

SALES  = [price] * [quantity]

The format of the price and sales column was changed to currency in Dollars($).

A calculation table was created to store all measures


## Data Modelling
It is a star schema type, the dimensional tables were connected to the fact table with their keys. DimDate table on date column, DimOrder table on order_id column, DimSales table on sales_id column, DimCustomer on postal-code column and DimPoduct on Product_code column.

![sparepart modelling](https://github.com/DeesAnalytics/Shipping-Agency/assets/124782621/ee4385ff-ec96-4399-aebb-f19b8cc0ef82)

## Data Analysis
### PowerBI (Data analysis expression (DAX) 

Measures:

•	Same period last year function

•	Total YTD and Total MTD

•	Total sales

•	Calendar function for date table

![sapreparts table](https://github.com/DeesAnalytics/Shipping-Agency/assets/124782621/a796cf42-56a1-4838-9b75-b80f12c0ab11)

### SQL 
•	Statistical evaluation
•	Structured data


![SQL CODE](https://github.com/DeesAnalytics/Shipping-Agency/assets/124782621/f22a5952-e907-4a86-a6dc-20e9885ad2bc)

## DATA VISUALIZATION
![shippingoverview](https://github.com/DeesAnalytics/Shipping-Agency/assets/124782621/d50485e3-790e-4aca-a937-5207e739a532)

![sparepart viz2](https://github.com/DeesAnalytics/Shipping-Agency/assets/124782621/e9499d92-cee0-4819-87f8-db0db72cdf5a)

## INSIGHTS

Sum of sales dropped from $654,841 to $249,530 during its steepest decline in 2005. The following factors contributed to the 28% drop in 2005 sales revenue.

#### •	The company experienced over 25% decrease in sales across all product types because a total of thirty-eight (38) customers including top seven (7) customers stopped operation with the company.
#### •	The loss was also contributed by USA whose sum of sales changed by $137K from $240K because it stopped operations in some cities such as NYC, Cambridge and Brickhaven while UK had a 47% decrease.
#### •	Countries in APAC region did not operate in the 4th quarter of the year while those in Japan region did not operate in the 3rd and 4th quarter.
#### •	The company had a 46% decrease in the 4th quarter because the company did not operate in November which is the month with highest sales over the years, operations in December only occur on Thursdays while four (4) days in October.
#### •	Top order groups (group 1 and 2) experienced a loss of $133k while Order group 8, 15, 16, 17  left the company.

Sales in May, 2005 was the highest for the month of May across the years.

December has the lowest sales across the year.

There were less order for prices above $75 for small size, above $97 for medium and above $130 for large.

Medium size products has the highest sales across the year.

## Recommendation

•	Expansion of the company to have outlets in all the regions will attract more investors, reduce the cost of shipping and also, increase the brand popularity.

•	Promotional campaign should be targeted towards the 3rd quarter offering a discounted price to large and small size products to both old and new customers to attract more sales. It is important to investigate why sales decline in December.

•	The company should operate on a staff shift across all days of the week for smooth operation, efficiency and continuity of the brand.

•	The company should maintain a standard price range for product sizes.

•	The company should conduct a market research on why some companies stopped operation.

•	The company should improve the shipment process, ensure perfect delivery of right products and also reduce days of shipment.

•	The staff should be compensated during it peak months (November, October and May) of sales.


