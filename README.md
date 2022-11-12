# Customer Segmentation
## Use Case Summary
### Objective Statement
* Get insight about how much customer spend every month on every year
* Get insight about how much customer spend every month on 2011
* Get insight about how much customer spend every month on 2012
* Get insight about how much customer spend every month on 2013
* Get insight about how much customer spend every month on 2014
* Get insight about how big they spend on a transaction
* Get insight about the ratio between customer segment
* Get insight about trend on every year
* Get business insight about how, when and whom to promote business on the right time
* Get insight about marketing strategy or planning based on segmentation

### Challenges
* There is data that has an inappropriate data type

### Methodology / Analytic Technique
* Descriptive analysis
* Graph analysis
* RFM(Recency, Frequency, Monetary) Model

### Business Benefit
* Help Business to make decision about marketing strategy based on customer segmentation
* Help business to focus what customer need

### Expected Outcome
* Get to know how many customer spend every month on every year on our business
* Get to know how many customer spend every month on 2011
* Get to know how many customer spend every month on 2012
* Get to know how many customer spend every month on 2013
* Get to know how many customer spend every month on 2014
* Get to know how big they spend on a transaction
* Get to know the ratio between customer segment
* Get to know trend on every year
* Get to know when, how, and for whom the product will be promote
* Recommendation based on customer segmentation

## Business Understanding
Online retail or as known as online shopping refers to a form of electronic commerce where consumers directly buy goods or services from a seller via the Internet rather. Customers usually visit the company's website, select a product, enter payment information and shipping details, and then order the product. All of these steps are completed entirely online.

This case has some business question using the data : 
* How many customer spend every month on every year ?
* How big they are spend on a transaction ?
* How about Customer segmentation based on customer spend ?
* How about recommendation based customer segmentation ?

## Data Understanding
* Order data is a record of customer purchase data from January 4, 2011 to December 31, 2014
* Source Data :  https://www.kaggle.com/datasets/siddinho/sample-orders-dataset-retail
* The dataset has 4 columns and 5009 rows.
* Data Dictionary :
    * order_date : Date when customer order
    * order_id : ID customer order for each transaction 
    * customer : Name of Customer
    * grand_total : total transaction for each customer

## Data Preparation
Code Used:
* Python Version: 3.7.15
* Packages: Pandas, Numpy, Matplotlib, Seaborn, Datetime, Sklearn,Scipy, Plotly and Feature Engine 

## Data Cleansing
There is 1 column that has an inappropriate data type so it is necessary to adjust the data type.

## EDA
### Grand Total in 2011
![grand total in 2011](https://user-images.githubusercontent.com/61875831/201360009-8133dbe2-0e7b-428b-92c7-4e26e6d44233.png)
Based on the graph above, it can be seen that in 2011, the trend of total customer purchases increased, although in 2011 there was a **significant decrease** in the second month which reached **the lowest point of 4810**, and **reached the peak/all time high 2011** in the 9th month of the year which **reached 81784**. On an annual basis, **Customer spend increased by 398.58%**

### Grand Total in 2012
![grand total in 2012](https://user-images.githubusercontent.com/61875831/201360263-bbd80708-5a0b-42cc-89b2-6f9641a1fe0e.png)
Based on the graph above, it can be seen that in 2012, the trend of total customer purchases increased, although in 2012 there was a **significant decrease** in the second month which reached **the lowest point of 12211**, and **reached the peak/all time high 2012** in the 11th month of the year which **reached 75968**. On an annual basis, **Customer spend increased by 312.23%**

### Grand Total in 2013
![grand total in 2013](https://user-images.githubusercontent.com/61875831/201360470-3150e982-7ee8-4fbe-bfd3-11aaa452b175.png)
Based on the graph above, it can be seen that in 2013, the trend of total customer purchases increased, although in 2013 there was a **significant decrease** in the first month which reached **the lowest point of 18543**, and **reached the peak/all time high 2013** in the last month of the year which **reached 97244**. On an annual basis, **Customer spend increased by 424.42%**

### Grand Total in 2014
![grand total in 2014](https://user-images.githubusercontent.com/61875831/201360698-938ebdae-f63b-4b00-9d38-a2ac1bf90c1b.png)
Based on the graph above, it can be seen that in 2014, the trend of total customer purchases increased, although in 2014 there was a **significant decrease** in the second month which reached **the lowest point of 44708**, and **reached the peak/all time high 2014** in the 11th month of the year which **reached 112329**. On an annual basis, **Customer spend increased by 102.38%**

### Grand Total by Month
![Grand total by Month](https://user-images.githubusercontent.com/61875831/201360905-0768815b-e8e4-4af1-bebb-18bb109bd5dc.png)
From the graph above, Customer purchase data 'order data' from January 2011 to 2014 is fluctuated. In 2011 the highest purchase was in September with a total purchase of **81,784 k** and the lowest was of **4810** in February, in 2012 the highest purchase was in November with a total purchase of **75,968 k** and the lowest was in February with a value of **12,211 k** , in 2013 the highest purchase was worth **97,244 k** in December and the lowest was in January with a value of **18,543 k**, and in 2014 the highest purchase was in November with a total of **112.293 k** and the lowest in February with a value of **20,287 k**. Overall, the highest purchase in the period 2011 to 2014 was in November 2014 with a value of **112.293 k** and the lowest was in February 2011 with a total purchase of **4810**.
From the data above, there is also a visible pattern where in the three-year period the lowest purchases are generally at the beginning of the year,  between January and February, while the highest purchases are at the end of the year between September and December.

## Modeling : RFM Segmentation

* RFM analysis allows you to segment customers by the frequency and value of purchases and identify those customers who spend the most money

* Part of RFM Segmentation Modeling:
  * Recency - How long it's been since a customer bought something from us.
  * Frequency - How often a customer buys from us.
  * Monetary value - The total value of purchases a customer has made.
  
 ![rfm score](https://user-images.githubusercontent.com/99872829/201459324-c9668554-4383-4d42-9abf-8b0a5ce21f01.JPG)
 
 * In this RFM Model assigns a score of 1-4 (from best to worst) for customers in each of the three categories. The best RFM score is the one with the smallest values    for each variable, we use a 1 to 4 scale for recency, frequency, and monetary, with 1 being the highest, then the perfect RFM score is 111.
 
 ## Labeling
 
![labeling](https://user-images.githubusercontent.com/99872829/201459637-ea2e68fd-58e4-49a0-88ca-999aeb97a381.JPG)

From the graph above, it is known that there are 6 categories of customers.
The most customer category is **Loyal Customer** and the least is **Almost lost** customer.
**Loyal customers** are customers who have frequent purchases (F=1) The percentage of loyal customers is 16.27% of all customer.
**Big Spenders** are customers who make purchases with a large amount of price (M = 1), the percentage of Big Spenders customers is 15.76% of all customer.
**Lost Cheap Customers** are customers who have made a purchase for a long time (R = 4), rarely make purchases (low frequency/ F= 4) and the total price of the purchase is small (M= 4), the number of incoming customers in the Lost Cheap Customer category is 8.45% of all customers.
**Best Customer** is a customer who has recently made a purchase (R = 1), frequently makes purchases (high frequency/ F= 1) and the total price of the purchase is large (M= 1), the number of customers who fall into the category This is 3.78% of the total customers.
**Lost Customers**, are customers who haven't made a purchase long enough (R = 3), rarely make purchases (low frequency/ F= 4) and the total price of the purchase is small (M=4), customers who enter in this category amounted to 3.91% of all customers.
**Almost Lost** is a customer who has recently made a purchase (R = 1), rarely makes a purchase (quite low frequency/F= 3) and the total price of the purchase is small (M=4), a customer who is included in the this category is 0.25% of all customers.

## Result

1.   Based on the data above, we can see that the average customer purchases products with a **total price of 458.626672**, the customer with the **lowest purchase is at 1.000000** and **the highest purchase is at 23661.000000**
2.   Based on the graph above, it can be seen that in 2011, the trend of total customer purchases increased, although in 2011 there was a **significant decrease** in the second month which reached **the lowest point of 4810**, and **reached the peak/all time high 2011** in the 9th month of the year which **reached 81784**. On an annual basis, **Customer spend increased by 398.58%**
3. Based on the graph above, it can be seen that in 2012, the trend of total customer purchases increased, although in 2012 there was a **significant decrease** in the second month which reached **the lowest point of 12211**, and **reached the peak/all time high 2012** in the 11th month of the year which **reached 75968**. On an annual basis, **Customer spend increased by 312.23%**
4. Based on the graph above, it can be seen that in 2013, the trend of total customer purchases increased, although in 2013 there was a **significant decrease** in the first month which reached **the lowest point of 18543**, and **reached the peak/all time high 2013** in the last month of the year which **reached 97244**. On an annual basis, **Customer spend increased by 424.42%**
5. Based on the graph above, it can be seen that in 2014, the trend of total customer purchases increased, although in 2014 there was a **significant decrease** in the second month which reached **the lowest point of 44708**, and **reached the peak/all time high 2014** in the 11th month of the year which **reached 112329**. On an annual basis, **Customer spend increased by 102.38%**
6. Customer purchase data 'order data' from January 2011 to 2014 is fluctuated. In 2011 the highest purchase was in September with a total purchase of **81,784 k** and the lowest was of **4810** in February, in 2012 the highest purchase was in November with a total purchase of **75,968 k** and the lowest was in February with a value of **12,211 k** , in 2013 the highest purchase was worth **97,244 k** in December and the lowest was in January with a value of **18,543 k**, and in 2014 the highest purchase was in November with a total of **112.293 k** and the lowest in February with a value of **20,287 k**. Overall, the highest purchase in the period 2011 to 2014 was in November 2014 with a value of **112.293 k** and the lowest was in February 2011 with a total purchase of **4810**.
From the data above, there is also a visible pattern where in the three-year period the lowest purchases are generally at the beginning of the year,  between January and February, while the highest purchases are at the end of the year between September and December.
7. From the graph above, it is known that there are 6 categories of customers.
    * The most customer category is **Loyal Customer** and the least is **Almost lost** customer.
    * **Loyal customers** are customers who have frequent purchases (F=1) The percentage of loyal customers is 16.27% of all customer. 
    * **Big Spenders** are customers who make purchases with a large amount of price (M = 1), the percentage of Big Spenders customers is 15.76% of all customer.
    * **Lost Cheap Customers** are customers who have made a purchase for a long time (R = 4), rarely make purchases (low frequency/ F= 4) and the total price of the purchase is small (M= 4), the number of incoming customers in the Lost Cheap Customer category is 8.45% of all customers. 
    * **Best Customer** is a customer who has recently made a purchase (R = 1), frequently makes purchases (high frequency/ F= 1) and the total price of the purchase is large (M= 1), the number of customers who fall into the category This is 3.78% of the total customers.
    * **Lost Customers**, are customers who haven't made a purchase long enough (R = 3), rarely make purchases (low frequency/ F= 4) and the total price of the purchase is small (M=4), customers who enter in this category amounted to 3.91% of all customers.
    * **Almost Lost** is a customer who has recently made a purchase (R = 1), rarely makes a purchase (quite low frequency/F= 3) and the total price of the purchase is small (M=4), a customer who is included in the this category is 0.25% of all customers.

## Recommendation
*   Recommendation for "Loyal Customers" segment: In order to keep this customer group's loyalty and raise their value, the business team must optimize the budget and timing of both campaigns.
* Recommendation for "Big Spenders" segment : In order to keep and boosting frequency of order, focus on give loyalty and advantages for every order 
*   Recommendation for "Best Customers": Focus on boosting client purchases; as a result, develop an upselling/cross-selling strategy or make bundling strategy.
* Recommendation for "Almost Lost" segment: Since this customer group is more susceptible to churn, concentrate on reactivating consumers and encouraging repeat purchases by developing a reactivation strategy and retention strategy.
* Recommendation for "Lost Cheap Customers" and "Lost Customer" segment: The goal of the campaign is to reactivate the customer by creating a Reactivation strategy because this consumer category has churned.
