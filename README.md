# Marven-Toys
Tech Stack- Power BI

## Project Description

In here is the Sales & inventory data for a fictitious chain of toy stores in Mexico called Marven Toys, including information about products, stores, daily sales transactions, and current inventory levels at each location.

## Objective Statement

- Which product categories drive the biggest profits? And also are they the same across all store locations?

- Are there any seasonal trends or patterns in the sales data?

- Are sales being lost with out-of-stock products at certain locations?

- How much money is tied up in inventory at the toy stores? How long will it last?

From the provided analysis,it was discovered that the following insights indicated the following:

a) The toys category generated a profit of $1,079,527 which was slightly bigger than the electronics category($1,001,437). They are not the same accross  in all locations. 

b) From the sales projectory, the toys category carried the highest sales amount than other categories. In the last 21 days electronics had the lowest sales of $72,169.93 than others in all locations.

c) Products like the mini basketball hoop and  Monopoly among other products had low stocks that affected their sales records especially at the airport location.

d) The total amount of stocks in inventory was $410.240 across all locations. 

Other insights can be seen from the dashboard uploaded to this repository.



## Data Preparation / Cleaning 

- Business and Data Understanding 
- Data Preparation
- Data Analysis
- Recommendation

## Business Understanding

The main goal of this case study is to assist Marven Toys in making business driven decisions by analysing key performing aspects of its performance data and answering key questions that speak to the business needs.  I leverage on Microsoft Power BI for my data analysis and visualization.

On the aspect of data understanding, the data provided to me contained four different worksheets which are inventory, products, sales and stores. The csv provided contains fact table(worksheets) which are store, inventory and products while the fact table is the sales worksheet. 


## Data Preparation & Modelling

This stage started by importing the csv file into the power bi for proper data preparation. I ensured the column format and quality were accurate. Since the sales and store table had a date column, I had to create a date look up table so as to provide a table which helps in creating a relationship with other tables that have date column in the data modelling stage. I wrote the following m-code in a blank query to create a rolling calendar  =date(1992,5,10) and then wrote the formular below:

  > list.date(Source,number,From(DateTime.LocalNow())-Number.From(Source),#duration(1,0,0,0))

![roll1](https://user-images.githubusercontent.com/62305424/158252654-a84627f2-c168-4add-a1ba-4c359090e6b5.PNG)

![roll2](https://user-images.githubusercontent.com/62305424/158252672-2c5e14f4-2a38-4bad-8899-67680d2634f4.PNG)


![roll3](https://user-images.githubusercontent.com/62305424/158253040-24be6965-6836-411b-b30d-f44a0dd48bb9.PNG)




 Power bi is optimized to work with data models, as they help organize tables to reduce redundancy and optimize efficency. To create a relationship I navigated to a unique identifier i.e primary key in each look up table which was then connected to the foreign key within the sales table. All relationship cardinality performed during this stage was a one to many relationship. The image below shows the data model view of all tables involve.

![data modelling](https://user-images.githubusercontent.com/62305424/158258316-99e6095b-2320-44ba-adff-d4482460692d.PNG)





## Data Analysis 

To answer key questions that would be beneficial to business decisions, there is a need to analyse the data provided to gain insights which can be transformed into visuals for the stakeholders. Firstly to determine revenue, I had to calculate the sumx function of sales units and mutiply them with product price. From the revenue perspective, I determined the profit by subtracting cost from revenue. From here I started calculating the periodical revenue of different stores and their targets.

![reveue](https://user-images.githubusercontent.com/62305424/158261627-3f023c34-6b83-47c0-9f00-023765ec1e0f.PNG)

### Further insights from the analysis

For managenment to make data driven decision on the different products it offers and the location,I have further summarized below other key insights which may help the management of Marven Toys.

-	The leading category among product category in Marven Toys is the Toys category which has about $221,227 and slightly greater than Arts & Crafts ($220,673)

- The total profit of the company based on a revenue generated from different locations is over $4m during the course of its operations. Among all the location in the country, the airport generated the lowest profit of $378,049.

- The total loss of sales as regards stocks on hand is $6,923,164 in total and the bigger contributor to this is Lego Bricks which has a worth of $2,045,489 in stock. 

- Irrespective of electronics having the lowest sale value of $99,025, it has contributed more to the profit coffers of the company with about $1,001,437 which is slightly lower than Toys($1,079,527).

- The top performing product is colorbuds which have a sale of about $72,988. The Downtown location carries the highest amount of profit in this product category(Toy) which is $2,248,728.

- Further analysis into the sales made by different locations hightlights that Cuidad de Mexico had the highest sales in all its location which was $90,725 and was 54.33% higher than the Guanajuato location.


## Data Visualization

I created an interactive dashboard to communicate my insights to different stakeholders and also share the different steps and techniques involved in my analysis. 


![marven toys](https://user-images.githubusercontent.com/62305424/162070014-f97f5c1e-bbd4-4784-b340-3be05334ec3a.PNG)






