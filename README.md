# Mexico-Toys
Tech Stack- Power BI

# Introduction

In here is the Sales & inventory data for a fictitious chain of toy stores in Mexico called Mexico Toys, including information about products, stores, daily sales transactions, and current inventory levels at each location.

Objective Statement

- Which product categories drive the biggest profits? And also are the same across store locations?

- Are there any seasonal trends or patterns in the sales data?

- Are sales being lost with out-of-stock products at certain locations?

From the provided analysis gotten,it was discovered that the following insights indicated the following:

a) The toys category generated a profit of $1,079,527 which was slightly bigger than the electronics category($1,001,437). The difference was not much in all locations. 

b) From the sales projectory, the toy category carried the highest sales amount than other category. In the last 21 days electronic had the lowest sales of $72,169.93 than others in all locations.

c) Many products like mini basketball hoop and  playdoh playset among other products had low stocks which affected their sales records.

d) The total amount of stocks in inventory was $410.240 accross all locations. 

Other insights can be seen from the dashboard uploaded to this repository.



#The Approach

I followed this approach in modelling the solution for this business Challenge:

- Business and Data Understanding 
- Data Preparation
- Data exploration and analysis
- Data Visualization 
- Recommendation

Business Understanding

The main goal of this case study is to assist mexico Toys in making business driven decision by analysing key performing aspects of its performance data and answering key questions that speaks to the business needs.  I leverage ob Microsoft Power BI for my data analysis and visualization.
On the asspect of data understanding, the data provided to me contained four different worksheet which are inventory, products, sales and stores. The inventory worksheet contain store ID, product ID, stock on hand. The product worksheet contains Product ID, Product name, products category, product cost and product price. Below are the images of the worksheets attached.

([Data1](https://user-images.githubusercontent.com/62305424/158242402-ffec39eb-e3b9-4e36-a1a9-8daf5f9f0f88.PNG))
![Data2](https://user-images.githubusercontent.com/62305424/158242578-f2fe7b5b-3eb4-49a6-a791-da416302286e.PNG)
![data3](https://user-images.githubusercontent.com/62305424/158242616-9e4bc601-7bab-4a50-a12c-fd49a3e1b58e.PNG)
![data4](https://user-images.githubusercontent.com/62305424/158242685-f3208e9b-1156-46bd-92a0-748ca903dc5b.PNG)


Data Preparation

This stage started by importing the csv file into the power bi and load into power query editor for proper data preparation. With the help of power query i shaped and all tables accodring to provide an accurate result. I ensured the data types were accurate and also ensure colomn quality was 100%. 

![1](https://user-images.githubusercontent.com/62305424/158252444-0ed8d373-1493-4e70-b398-b33fc3d4a280.PNG)
![2](https://user-images.githubusercontent.com/62305424/158252476-f848b649-04cc-4971-b224-443363705d18.PNG)
![3](https://user-images.githubusercontent.com/62305424/158252499-e86bea2d-fa09-420d-94c3-c8eecd579350.PNG)
![4](https://user-images.githubusercontent.com/62305424/158252518-089a6c7c-98a4-4de2-b5fb-338e274def47.PNG)


Since the sales and store table had a date colmn, I had to create a date look up table so as to be a provide a table which help in creating relationship with other tables that have dates colomn in the data modelling stage. I created a rolling calender that which will not require updating everytime. Firstly i get into Get data function and then navigate to blank query at the bottom then i use M-code to generated a starting date =date(1992,5,10) in the function bar and then click the fx icon to add a new column where i entered the following formula:

list.date(Source,number,From(DateTime.LocalNow())-Number.From(Source),#duration(1,0,0,0))

![roll1](https://user-images.githubusercontent.com/62305424/158252654-a84627f2-c168-4add-a1ba-4c359090e6b5.PNG)

![roll2](https://user-images.githubusercontent.com/62305424/158252672-2c5e14f4-2a38-4bad-8899-67680d2634f4.PNG)



After entering the fomular i click enter to generate a list of date. I then naviagte to top icon and click on 'To table' which i then click okay. After creating the table, i added other columns in the calender table like start of the week, year etc

![roll3](https://user-images.githubusercontent.com/62305424/158253040-24be6965-6836-411b-b30d-f44a0dd48bb9.PNG)


Data Modelling

To create relationship between the tables i have to connect the tables base on a common relationship or key. Power bi is optimized to work with data models, as they help to organize tables of data so as to redure redundancy and optimize efficency. To create the relationship i source for a unique identifier, for example the products table and the sales table share a similar key which is the product_ID. By doing this we can now take a product and segment them into values which will be splited among different products.All relationship cardinality i did during this stage was a one to many. I also performed data normalisation so as to reduce data redundancy and  The image below shows the data model view of all tables involve.

![data modelling](https://user-images.githubusercontent.com/62305424/158258316-99e6095b-2320-44ba-adff-d4482460692d.PNG)

Data Analysis 

To answer key questions that would be beneficial to business decisions, there is need to analyse the data provided to gain insights which can then be transform into visuals for the stakeholders. Firstly to determine revenue i had to calculate the sumx function of sales units and mutiply them with product price. From the revenue insights i then went on to determine the profit by just subtracting total cost from total revenue. From here i started calculating the periodical revenue of different stores and their targets.

![reveue](https://user-images.githubusercontent.com/62305424/158261627-3f023c34-6b83-47c0-9f00-023765ec1e0f.PNG)

Insights from the analysis

For managenment to make data driven decision  on the different products it offers and the location,I have further summarized below other key insights whhich may be of help the management of Mexico Toys.

1. The total profit of the company base on a revenue generated from different locations is over $4m during the course of its operations. Among all the location in the country, the airport generated the lowest profit of $378,049. 
2. Irrespective of electronics having the lowest sale value of $99,025, it has contributed more to the profit coffers of the company with about $1,001,437 which slightly lower than than Toys($1,079,527).
3. The top performing product is colorbuds which have a sale of about $72,988. The Downtown location carries the highest amount of profit in this product category(Toy) which is $2,248,728. 
4. Further analysis into the sales made by different locations hightlights that Cuidad de Mexico had the highest sale in all its location which was $90,725 and was 54.33% higher than the Guanajuato location.

Data Visualization

I created an interactive dashboard to communicate my insights to different stakeholders and also sharing the different steps and techniques involve in my analysis. 
Also attach here is a picture of the dashboard for your understanding.

![dashboard](https://user-images.githubusercontent.com/62305424/158465620-698d50d7-f9af-4dde-98b8-8e4af74278ec.PNG)



