# Marven-Toys
Tech Stack- Power BI

## Project Description

In here is the Sales & inventory data for a fictitious chain of toy stores in Mexico called Marven Toys, including information about products, stores, daily sales transactions, and current inventory levels at each location.

## Objective Statement

- Which product categories drive the biggest profits? And also are the same across store locations?

- Are there any seasonal trends or patterns in the sales data?

- Are sales being lost with out-of-stock products at certain locations?

- How much money is tied up in inventory at the toy stores? How long will it last?

From the provided analysis gotten,it was discovered that the following insights indicated the following:

a) The toys category generated a profit of $1,079,527 which was slightly bigger than the electronics category($1,001,437). The difference was not much in all locations. 

b) From the sales projectory, the toy category carried the highest sales amount than other category. In the last 21 days electronic had the lowest sales of $72,169.93 than others in all locations.

c) Many products like mini basketball hoop and  Monopoly among other products had low stocks that affected their sales records especially at the airport location.

d) The total amount of stocks in inventory was $410.240 accross all locations. 

Other insights can be seen from the dashboard uploaded to this repository.



## Data Preparation / Cleaning 

- Business and Data Understanding 
- Data Preparation
- Data Analysis
- Recommendation

## Business Understanding

The main goal of this case study is to assist mexico Toys in making business driven decision by analysing key performing aspects of its performance data and answering key questions that speaks to the business needs.  I leverage on Microsoft Power BI for my data analysis and visualization.

On the aspect of data understanding, the data provided to me contained four different worksheet which are inventory, products, sales and stores. The csv provided contain fact table which are base on store, inventory and products while the fact table is a sales data. 


## Data Preparation & Modelling

This stage started by importing the csv file into the power bi for proper data preparation. I ensured the data types were accurate and also ensure colomn quality was 100%. Since the sales and store table had a date column, I had to create a date look up table so as to be a provide a table which help in creating relationship with other tables that have dates column in the data modelling stage. I wrote the following m-code in a blank query to create the rolling calendar  =date(1992,5,10) and then wrote the formular below:

  > list.date(Source,number,From(DateTime.LocalNow())-Number.From(Source),#duration(1,0,0,0))

![roll1](https://user-images.githubusercontent.com/62305424/158252654-a84627f2-c168-4add-a1ba-4c359090e6b5.PNG)

![roll2](https://user-images.githubusercontent.com/62305424/158252672-2c5e14f4-2a38-4bad-8899-67680d2634f4.PNG)


![roll3](https://user-images.githubusercontent.com/62305424/158253040-24be6965-6836-411b-b30d-f44a0dd48bb9.PNG)


 Power bi is optimized to work with data models, as they help to organize tables of data so as to reduce redundancy and optimize efficency. To create the relationship i source for a unique identifier i.e primary key in the look up table which was then connected to the foreign key within the sales table. All relationship cardinality performed during this stage was a one to many relationship. The image below shows the data model view of all tables involve.

![data modelling](https://user-images.githubusercontent.com/62305424/158258316-99e6095b-2320-44ba-adff-d4482460692d.PNG)


## Data Analysis 

To answer key questions that would be beneficial to business decisions, there is need to analyse the data provided to gain insights which can then be transform into visuals for the stakeholders. Firstly to determine revenue, i had to calculate the sumx function of sales units and mutiply them with product price. From the revenue perspective, i determine the profit by just subtracting total cost from total revenue. From here i started calculating the periodical revenue of different stores and their targets.

![reveue](https://user-images.githubusercontent.com/62305424/158261627-3f023c34-6b83-47c0-9f00-023765ec1e0f.PNG)

Further Insights from the analysis
For managenment to make data driven decision on the different products it offers and the location,I have further summarized below other key insights whhich may be of help the management of Mexico Toys.

-	The leading category among product category in Marven Toys is the Toys category which has about $221,227 and slightly bigger than greater than Arts & Crafts ($220,673)

- The total profit of the company base on a revenue generated from different locations is over $4m during the course of its operations. Among all the location in the country, the airport generated the lowest profit of $378,049.

- The total loss of sales as regards stocks on hand is $6,923,164 in total and the bigger contributor to this is Lego Bricks which has a worth of $2,045,489 in stock. 

- Irrespective of electronics having the lowest sale value of $99,025, it has contributed more to the profit coffers of the company with about $1,001,437 which slightly lower than than Toys($1,079,527).

- The top performing product is colorbuds which have a sale of about $72,988. The Downtown location carries the highest amount of profit in this product category(Toy) which is $2,248,728.

- Further analysis into the sales made by different locations hightlights that Cuidad de Mexico had the highest sale in all its location which was $90,725 and was 54.33% higher than the Guanajuato location.


Data Visualization

I created an interactive dashboard to communicate my insights to different stakeholders and also share the different steps and techniques involve in my analysis. 
Also attach here is a picture of the dashboard for your understanding.

![new dash-2](https://user-images.githubusercontent.com/62305424/159177073-df1a19db-63d3-4460-abab-d6f3236c5c6d.PNG)





