## Brazilian-E-Commerce

### Project Overview

To review and understand best-selling Products through customer Review analysis and do product sales predictions. 
The Dataset has nine (9) different tables : Olist Customer Dataset, Olist geolocation Dataset, Olist Order items Dataset, Olist Order payment, Order review, Orders Dataset, products Dataset, sellers Dataset, and product Category name translation.
 The dataset has information on 100k orders (according to the information given) from 2016 to 2018 made at multiple marketplaces in Brazil. Its features allow viewing orders from multiple dimensions: from order status, price, payment, and freight performance to customer location, product attributes, and finally reviews written by customers. 
There is also a released geolocation dataset that relates Brazilian zip codes to lat/lng coordinates. This is real commercial data. 

### Data Sources

Quantum Analytics

### Data Transformation and Cleaning:

To successfully Analyze these different tables I loaded the different Datasets to Power query editor and merged all with their unique primary keys. Created a Conditional Column to represent Customer Review Category levels; Thus;
5 — Very Good, 4 — Good, 3 — Average, 2 — Poor, and, 1 — Very Poor. 
Created a new custom column to Calculate the days from the purchase date and delivery date — Average Delivery Time: with column name “Delivery Day(s)” and the result was in hours, minutes, and seconds (hms). So, to achieve my goal of how many days (s) it took to deliver the goods to a customer I had to convert the column to Day by highlighting the column then from the “Add Column” pane click on the “Duration” pane and it created another column with the number of days which is named Average Delivery Day(s). Replaceed a lot of ‘null’ values with zero which could hamper data standardization. Cleaning and removing some major errors which brought my Dataset to about 32 Columns and over 10,000 rows. 



### Data Visualization KPIs
 Total Orders = SUM(‘Brazilian_E-Commerce’[order_purchase_Year]) 
 
Total Products = DISTINCTCOUNT(‘Brazilian_E-Commerce’[product_category_name_english])


 Total Sales = SUM(‘Brazilian_E-Commerce’[payment_value]) 




